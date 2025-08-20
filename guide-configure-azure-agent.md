# Configuración de un agente de Azure DevOps
1. Acceder a Azure Devops e iniciar sesión con la cuenta de usuario que desee configurar el agente.
2. Una vez logueado vamos a la sección **settings** y buscamos en la sección de pipelines la que diga **Agent pools**.
3. Clic en la opción "Add Pool" Sí vamos a crear uno nuevo.
4. Seleccionamos el tipo de pool que queremos crear en es caso seria **Self-hosted**.
5. Le brindamos un nombre identificativo al agente pool "Ej. WindowsServerPool" y una descripción (Opcional) y le damos clic en create. 
6. Dentro del nuevo agente creado, damos clic en "New Agent".
7. Seleccionamos el Sistema Operativo y la versión que deseamos usar en este caso Windows.
8. Descargamos el archivo ZIP del agente el cuál puede tener un nombre similar a "vsts-agent-win-x64-2.164.2.zip".
9.  Copiamos dicho archivo al servidor/máquina donde queremos instalar el agente.

# Instalación y configuración del agente
1. Una vez descargado el agente, lo descomprimimos en la carpeta de alojamiento deseada Ej. Descargas/
2. Dentro de la carpeta descomprimida abrimos una ventana de CMD como administrador.
3. Ejecutamos el siguiente comando: ".\config.cmd" y enter.
4. Lo primero que nos solicita es la URL del azure devops que donde queremos configurar el agente, la url es algo similar a "https://dev.azure.com/tu-proyecto"
5. Lo siguiente que solicita es el PAT (Personal Access Token) que se genera dentro del pool creado en los  (3, 4, 5 de la primera sección).
6. Para generar el PAT nos dirigimos a la opción superior derecha al lado del ícono de usuario y seleccionamos "User Settings".
7. Daremos clic en ese ícono y observaremos varias opciones, la importante en este caso es la opción de "Personal Access Tokens".
8. Dentro de esta observaremos todos los tokens que tenemos disponibles, pero necesitamos uno nuevo por ende le daremos clic en "New Token".
9. Le brindamos un nombre significativo Ej **"WindowsServerTkn"**, la organización, tiempo de expiración en (UTC) y todas las opciones que sean apropiadas.
10. En las opciones de permisos seleccionaremos las siguientes:
   * Agents Pools (Read & manage).
   * Deployment groups (Read & manage).
   * Build (Opcional) (Read & manage).
11. Con todo ya configurado le damos clic en "Create".
12. Al darle clic en "create" nos aparecerá un nuevo token que debemos de copiar y guardar en un lugar seguro ya que requeriremos de este en la configuración del agente.
13. Continuando con el paso #4 una vez con el token obtenido nos dirigimos al cmd y le damos enter (Para que reconozca que queremos usar un PAT).
14. Copiamos el token generado y le damos enter. (Aparece en formato de asteriscos).
15. Seguido a esto nos solicitara el nombre del pool que queremos usar, en este caso sería **WindowsServerPool** y le damos enter.
16. Después solicitara el nommbre del agente que queremos usar, en este caso sería **WindowsServerAgent** y le damos enter. (Puede ser cualquier nombre).
17. Casi terminando el proceso lo que nos solicitara es que si deseamos trabajar localmente en la carpeta "_work" u otra carpeta, para fines de guía lo dejaremos como está con _work por defecto y le damos enter. (Enter por defecto es _work).
18. Si deseamos que sea un agente que funcione como un servicio de nuestro equipo tendremos que escribir "Y" y le damos enter.
19. Después nos saldrá esta opción **Enter enable SERVICE_SID_TYPE_UNRESTRICTED for agent service (Y/N) (press enter for N)** que en resumidas cuenta es sí deseamos dar permisos de administrador al servicio, por ende suele quedar a decisión de cada usuario, en este caso como el paso anterior escribimos "Y" y damos enter.
20. Después aparecerá la opción de **Enter User account tio use fot the service (press enter for NT AUTHORITY\NETWORK SERVICE)** en este caso escribiremos un usuario que tenga permisos de administrador o si no deseamos dar ese permiso dejamos vacío el campo y le damos enter. (Por defecto es NT AUTHORITY\NETWORK SERVICE).
21. Nos solicitará la contraseña del usuario que elegimos, en este caso la contraseña de administrador.
22. **Enter whether to prevent service starting immediately after configuration is finished?** Esta opción nos permite que el servicio no se inicie inmediatamente después de que se haya configurado, en este caso la opción por defecto es "N" si le damos enter, pero recae directamente a decisión de cada usuario. (Por funcionamiento de la guía escribiremos "Y" y le damos enter).
# Ejecución del agente (Sí es manual)
1. Abrimos una ventada de CMD como administrador.
2. Realizamos toda la configuración anterior hasta el paso 17. ("N" en todas las opciones mencionadas a partir del paso 18).
3. Navegamos a la carpeta donde se encuentra el agente descargado.
4. Ejecutamos el siguiente comando: ".\run.cmd" y enter.

# Verificar si el agente está funcionando como servicio.
1. Abrimos el la búsqueda de Windows y escribimos "services.msc" y le damos enter.
2. Dentro de la ventana de servicios buscamos algo como lo siguiente **vstsagent.usuario.WindowsServerPool.WindowsServerAgent**.
3. Si no se encuentra iniciado lo iniciamos y configuramos para que funcione de manera automática cada vez que se reinicie el equipo.

# Eliminar el agente y volver a configurarlo.
1. Dentro de la carpeta que se encuentra alojado el agente abrimos una ventana de CMD como administrador.
2. Ejecutamos el siguiente comando: ".config.cmd remove --auth PAT --token "Tkn-generado" y enter.
3. Lo que se ejecutará en el paso anterior es que se define que el tipo de autorización es el PAT y le brindaremos el token de acceso generado en la explicación anterior. (Por eso se recomienda guardarlo en un lugar seguro y accesible).
4. Para saber si se ha eliminado el agente de nuestro equipo, abrimos los servicios de Windows y buscamos el servicio relacionado al agente que acabamos de eliminar.