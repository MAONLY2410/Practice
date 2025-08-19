# Breve introducción sobre lo que posee la pantalla de inicio
Esta pantalla tiene como objetivo mostrar cierta información relevante sobre el PLS **(Port Logistic System)** que es el sistema de gestión portuaria en desarrollo. Dicha pantalla se subdivide de forma visual en tres secciones prinicipales:
1. Header (Información varia).
2. Body (Información relevante). Que se subdivide en tres secciones:
   1. Arribos Programados.
   2. Mis Procesos.
   3. Arribos Planificados.
3. Footer (Información varia legal).
# Header (Información varia)
Esta sección tiene como objetivo reflejar ciertas configuraciones e información relevante tanto del sistema como del usuario que se encuentra en el sistema de gestión portuaria. Mostrando lo siguiente:
* **Menú de navegación (Oculto):** Este menú se encuentra en la parte superior izquierda de la pantalla reflejado mediante un ícono de 3 líneas que se muestra solamente cuando el usuario le da clic en él, pero que se puede mostrar o ocultar en cualquier momento. Además de que cumple la misión de reflejar los diferentes menús que se puede acceder a través del sistema dependiendo del rol que posea el usuario y la información que tiene disponible en el sistema.
* **Home:** Ícono que permite el acceder desde cualquier punto del sistema a la pantalla de inicio. (Se refleja como un botón con el diseño de una casa al lado del menú de navegación).
* **Nombre del sistema:** Es el nombre del sistema de gestión portuaria en siglas que se encuentra en el sistema.
* **Ampliar:** Ícono ubicado de lado derecho superior que permite tener una percepción más amplia de la información presente en la pantalla. (Se refleja como un botón con el diseño de un cuadrado seccionado).
* **Cambiar modo oscuro:** Ícono ubicado de lado derecho superior que permite cambiar la tonalidad del sistema de forma clara o oscura para comodidad visual. (Se refleja como un botón de acción directa con el diseño de un círculo con una línea horizontal además de un ícono guía que indica el modo en el cual se encuentra el sistema).
* **Usuario actual logueado:** Muestra el correo electrónico del usuario brindado por la empresa con el cual posee ciertas acciones en el sistema.
* **Cerrar sesión:** Ícono ubicado de lado derecho superior que permite cerrar la sesión del usuario actual. (Se refleja como un botón de acción directa con el diseño de una puerta y una flecha).
# Body
## Body Parte 1 (Arribos Programados)
Esta sección tiene como objetivo mostrar cierta información relevante sobre los arribos programados en el sistema de gestión portuaria. Mostrando lo siguiente:
* **Arribos programados:** Leyenda que indica que se encuentran arribos programados en el sistema.
* **Campo año:** Campo de tipo obligatorio que permite ingresar solamente caracteres numéricos y algunos especiales (, . - +) permitiendo anexar el año en el que se desea ver los arribos programados y la información relevante de ellos.
* **Campo semana:** Campo no obligatorio que permite ingresar solamente caracteres numéricos y algunos especiales (, . - +) permitiendo anexar la semana en la que se desea ver los arribos programados y la información relevante de ellos.
* **Símbolo filtrar:** Funciona de manera conjunta con los campos año y semana para así permitir el filtrado de los arribos programados por el año y la semana en el que se desea ver. (Se refleja como un botón de acción directa de color azul con el diseño clásico de un símbol de filtro).
* **Campo de filtro:** Permite filtrar los arribos programados por el # de arribo, nave, identificador y los otros diversos campos que se encuentran en la tabla de arribos programados.
* **Símbolo que guía al programa operativo:** Funciona como un botón de acción directa que tiene configurado de forma interna el redirigir al programa operativo actual del sistema de gestión portuaria. (Se refleja como un símbolo especial de una cuadrado con una flecha).
* **Símbolo de colapso:** Funciona como un botón de acción que permite ocultar o mostrar toda la información del apartado de arribos programados. (Se refleja como un símbolo especial de una flecha que se mueve hacía abajo o hacía arriba).
* **Simbolo refrescar:** Funciona como un botón de acción que permite refrescar todo la información del apartado de arribos programados con la información en tiempo real. (Se refleja como un símbolo de una flecha circular que gira hacia la derecha).
* **Datos en pantalla:** En este apartado en especial se refleja toda la información en tiempo real de los arribos programados desde el nombre del navio hasta la fecha de finalización de trabajo de cada uno de ellos entre otros datos más que se explicaran a continuación.
  1. **# de arribo:**: Número de arribo brindado por la empresa con el cual se puede manejar todo lo relacionado con el navio. Este número se confecciona con el año y un número de consecutivo. Ej --> **20250016**.
  2. **Nave:** Nombre del navio que se encuentra tanto en sistema portuario como a nivel internacional.
  3. **Identificador:** Identificador del barco valido a nivel internacional como el número IMO, número de registro o número brindado por lae empresa.
  4. **Hora llegada:** A nivel portuario esto se reconoce como la E.T.A (Estimated Time of Arrival) y su función es reflejar la hora estimada de llegada del barco a la terminal de carga. Además de que se refleja en el formato de 24 horas. Luego se compara con la A.T.A (Actual Time of Arrival) que es la hora real en que el barco llega a la terminal de carga.
  5. **Hora en puesto:** A nivel portuario esto se reconoce como la E.T.B (Estimated Time of Boarding) y la función principal de este apartado es reflejar la hora estimada de ubicación del barco en el puestod de carga.
  6. **Hora fin operación:** A nivel portuario este apartado se reconoce como la E.T.C (Estimated Time of Completion) y su función en el sistema es reflejar la hora estimada de finalización de la operación del barco.
  7. **Hora salida:** A nivel portuario este apartado se reconoce como la E.T.D (Estimated Time of Disembarkment) y su función es reflejar la hora estimada de salida del barco de la terminal de carga.
  8. **Estadía en horas:** De manera muy sencilla se refleja el tiempo aproximado en horas en el que el barco se encontrara en el puesto de carga desde la hora de llegada hasta la hora de salida.
  9. **Calado proyectado:** El calado proyectado se refiere a la cantidad de agua que el barco necesita para poder navegar de manera segura sin tocar el fondo marino. Este dato es proporcionado por el capitán del barco y es crucial para garantizar la seguridad durante las operaciones portuarias.
  10. **Estado**: Este apartado refleja de manera directa el estado de la operación del barco (Confirmado o cancelado).

**Observación:** Todos los datos mencionados con anterioridad poseen la chance de ser ordenados de forma ascendente o descendente o dejarlos como se están reflejando por defecto.
* **Items por página:** Permite cambiar el número de elementos que se muestran en cada página del apartado de arribos programados. Yendo desde 5 a 15 por ejemplo.
* **Símbolo siguiente:** Permite ir a la siguiente página del apartado de arribos programados. Reflejado como una flecha que apunta hacía la derecha.
* **Símbolo anterior:** Permite ir a la página anterior del apartado de arribos programados. Reflejado como una flecha que apunta hacía la izquierda.
* **Símbolo saltar a la primera página:** Permite ir a la primera página del apartado de arribos programados. Reflejado mediante una flecha y una línea apuntando hacía la derecha
* **Símbolo saltar a la última página:** Permite ir a la última página del apartado de arribos programados. Reflejado mediante una flecha y una línea apuntando hacía la izquierda.
## Body Parte 2 (Mis procesos)
Esta sección tiene como función mostrar toda la información relevante generada por parte del usuario logueado en el sistema de gestión portuaria. Mostrando lo siguiente:
* **Mis procesos:** Leyenda que indica que se encuentran procesos en el sistema.
* **Símbolo que guía a mis procesos:** Funciona como un botón de acción directa que tiene configurado de forma interna el redirigir a la sección de mis procesos del sistema de gestión portuaria. (Se refleja como un símbolo especial de una cuadrado con una flecha).
* **Símbolo de colapso:** Funciona como un botón de acción que permite ocultar o mostrar toda la información del apartado de arribos programados. (Se refleja como un símbolo especial de una flecha que se mueve hacía abajo o hacía arriba).
* **Campo de filtro:** Permite filtrar los procesos por los diversos campos que se encuentran en la tabla de procesos.
* **Simbolo refrescar:** Funciona como un botón de acción que permite refrescar todo la información del apartado de arribos programados con la información en tiempo real. (Se refleja como un símbolo de una flecha circular que gira hacia la derecha).
* **Código:**: (Me falta información).
* **Tipo:** (Me falta información).
* **Descripción:** Describe brevemente el proceso ligado al código.
* **Fecha de registro:** Fecha en la que se registró el proceso en el sistema.
* **Estado:** Estado del proceso en el sistema. (Me falta información).
* **Items por página:** Permite cambiar el número de elementos que se muestran en cada página del apartado de arribos programados. Yendo desde 5 a 15 por ejemplo.
* **Símbolo siguiente:** Permite ir a la siguiente página del apartado de arribos programados. Reflejado como una flecha que apunta hacía la derecha.
* **Símbolo anterior:** Permite ir a la página anterior del apartado de arribos programados. Reflejado como una flecha que apunta hacía la izquierda.
* **Símbolo saltar a la primera página:** Permite ir a la primera página del apartado de arribos programados. Reflejado mediante una flecha y una línea apuntando hacía la derecha
* **Símbolo saltar a la última página:** Permite ir a la última página del apartado de arribos programados. Reflejado mediante una flecha y una línea apuntando hacía la izquierda.
## Body Parte 3 (Arribos Planificados)
Sección dirigida a mostrar de manera más visual mediante gráfico de barras los arribos programados en el sistema e información relevante sobre ellos.
* **Arribos planificados:** Leyenda que indica que se encuentran arribos planificados en el sistema.
* **Símbolo refrescar:** Funciona como un botón de acción que permite refrescar todo la información del apartado de arribos programados con la información en tiempo real. (Se refleja como un símbolo de una flecha circular que gira hacia la derecha).
* **Ícono de zoom +:** Funciona como un botón de acción que permite aumentar el zoom del gráfico de arribos planificados. Reflejado como un símbol de + que cada vez que se le presiona aumenta el tamaño del gráfico.
* **Ícono de zoom -:** Funciona como un botón de acción que permite disminuir el zoom del gráfico de arribos planificados. Reflejado como un símbol de - que cada vez que se le presiona disminuye el tamaño del gráfico.
* **Ícono de panning:** Funciona como un botón de acción que permite mover el gráfico de arribos planificados. Reflejado en el sistema como un ícono de una mano.
* **Ícono resetear vista:** Funciona como un botón de acción que permite de manera directa resetear la vista del gráfico a su estado original. Reflejado como un símbolo de una casa.
* **Ícono de descarga de gráfico:** Ícono que como su nombre indica permite la descarga del gráfico en formato SVG o PNG. Reflejado como un símbolo de tres líneas horizontales.
### Campos en el gráfico
* **# arribo:** Ubicado de lado izquierdo como una columna.
* **Gráfico de barras horizontales:** Proyectado como una columna la cual muestra en diversos colores los navios planificados. además de que el tamaño de las mismas refleja la duración del barco en estadía. Sumado a eso si se coloca sobre la barra el número del # arribo, nombre de la nave, naviera, hora en puesto, hora salida entre otros datos.
* **Día/Mes/Año:** En la parte inferior al gráfico se encontraron las fechas guía que permite una comprensión más cercana a la estadía del barco en el puesto de carga.
* **Guía del color:** En una posición inferior a la anterior se encuentra la guía de color la cual tiene como objetivo relacionar el nombre del barco con la barra que representa su estadía con un círculo del mismo color de esta barra.
# Footer (Información varia legal)
Sección que tiene como objetivo reflejar ciertas información relevante del sistema de gestión portuaria. Mostrando lo siguiente:
* **Nombre del sistema:** Es el nombre del sistema de gestión portuaria en siglas que se encuentra en el sistema.
* **Copyright:** Muestra el copyright del sistema y el año de su creación.