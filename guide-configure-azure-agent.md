# Configuración de un agente de Azure DevOps
1. Acceder a Azure Devops e iniciar sesión con la cuenta de usuario que desee configurar el agente.
2. Entramos a un proyecto iniciado o generamos uno nuevo.
3. Le damos clic en "Project Settings" (Abajo a la izquierda).
4. Seleccionamos "Agent Pools".
5. Clic en la opción "Add Pool" Sí vamos a crear uno nuevo.
6. Le brindamos un nombre identificativo al agente pool "Ej. WindowsServerPool" y agregar.
7. En Azure DevOps, dentro del "Agent Pool", damos clic en "New Agent".
8. Seleccionamos el Sistema Operativo que deseamos usar en este caso Windows.
9. Descargamos el archivo ZIP del agente el cuál puede tener un nombre similar a "vsts-agent-win-x64-2.164.2.zip".
10. Copiamos dicho archivo al servidor/máquina donde queremos instalar el agente.
# Configuración básica por medio del CMD
1. Después de descargar el archivo, lo descomprimimos y dentro de esa carpeta abrimos una ventana CMD donde ejecutamos el siguiente comando: ".\config.cmd"
## Durante la configuración en el CMD se debe de seguir los siguiente pasos:
1. Introducir la URL de la organización "Ej. https://dev.azure.com/maonly-org/"
2. Introducir el PAT (Personal Access Token) de la cuenta de usuario que deseamos configurar en el agente.
    1. Para generar un PAT nos dirigimos al perfil de la cuenta del usuario y seleccionamos el apartado "Security" y luego "Personal Access Tokens" y le damos clcic en "+ New Token".
    2. Para la configuración del token usaremos como nombre del mismo "Ej. Windows2012AgentTkn".
    3. Seleccionamos la orgnanización en este caso la propia.
    4. Le brindamos una expiración de tiempo al token que se adapte a la necesidad.
    5. Los scopes que se deben de seleccionar de manera directa son "Agent Pools (Read & manage)", "Deployments (Read & manage)" y "Build (Opcional) de (Read & manage) para el uso de pipeline".
 3. Le brindamos un nombre distintivo al agente "Ej. Windows2012Agent".
 4. Usamos el mismo nommbre de pool que creamos con anterioridad "WindowsServerPool".
# Ejecución del agente
1. Abrimos una ventada de CMD como administrador.
2. Navegamos a la carpeta donde se encuentra el agente descargado.
3. Ejecutamos el siguiente comando: ".\run.cmd" y enter.
# Instalación del agente como un servicio propio del sistema (Opcional)
1. En la misma carpeta del agente ejecutamos el siguiente comando: "svc install"
2. Luego iniciamos el servicio con el siguiente comando: "svc start"
# Extras (Opcional)
## Extra 1: Verificación de instalación como servicio en Windows
1. Ejecutamos administrador de servicios "services.msc" y buscamos el servicio que puede tener la siguiente apariencia: "vsts-agent-win-x64-2.164.2".
## Extra 2 Reinicio automático del agente en caso de fallo
1. abrimos menú de inicio y escribimos "services.msc" y buscamos el servicio que puede tener la siguiente apariencia: "vsts-agent-win-x64-2.164.2".
2. Clic derecho sobre el servicio y seleccionamos la opción de "Propiedades".
3. Vamos a la pestaña de "Recuperación".
4. Dentro de la pestaña anterior en las opciones "Fallo al primer intento", "Segundo intento", "Siguientes intentos" seleccionamos "Reiniciar el servicio".
5. Ajustamos el tiempo de espera antes de reiniciar el servicio en caso de fallo, "Ej. 1 minuto".
6. Damos clic en "Aplicar y aceptar".