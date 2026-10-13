# conectapyme-go
1.Descripción del proyecto

ConectaPyme es una propuesta de sistema de comunicación interna para una empresa que cuenta con dos sedes y necesita mejorar la comunicación entre sus trabajadores.

La idea del proyecto es tener una plataforma donde los empleados puedan enviar mensajes, crear conversaciones y compartir información relacionada con sus actividades laborales. De esta manera, se busca reducir los problemas que pueden aparecer cuando se utilizan diferentes medios de comunicación.

El proyecto se desarrolla como parte de una actividad universitaria de la carrera de Ingeniería en Sistemas de la Información.

2.Objetivo general

Desarrollar un sistema de comunicación interna utilizando el lenguaje Go, con una arquitectura cliente-servidor que permita organizar la comunicación entre los trabajadores de una empresa.

3.Objetivos específicos

Identificar las necesidades de comunicación de la empresa.

Diseñar la estructura del sistema mediante un diagrama UML.

Definir los actores, roles y responsabilidades del equipo.

Organizar el código fuente utilizando Git y GitHub.

Desarrollar las funciones principales del sistema.

Realizar pruebas para comprobar el funcionamiento de las operaciones implementadas.

4.Problema identificado

La empresa ha abierto una segunda sede y necesita mejorar la comunicación entre sus trabajadores. Cuando la información se comparte mediante diferentes aplicaciones o correos electrónicos, algunos mensajes pueden pasar desapercibidos y las respuestas pueden tardar más de lo esperado.

Por esta razón, se propone centralizar la comunicación en una plataforma que permita organizar los mensajes y facilitar el intercambio de información entre las dos sedes.

5.Tecnologías utilizadas

Go: lenguaje de programación para desarrollar el servidor.

Git: herramienta para controlar las versiones del código.

GitHub: plataforma para almacenar el repositorio y colaborar en equipo.

UML: herramienta de modelado para representar las clases y relaciones del sistema.

HTTP: protocolo propuesto para la comunicación entre el cliente y el servidor.

6.Arquitectura del sistema

ConectaPyme utilizará una arquitectura cliente-servidor.

El cliente enviará solicitudes al servidor para realizar operaciones, como consultar usuarios o enviar mensajes. El servidor procesará las solicitudes, validará los datos y devolverá una respuesta.

La arquitectura se organizará en los siguientes componentes:

Cliente: interfaz utilizada por los trabajadores.

Servidor: recibe y procesa las solicitudes.

Modelos: representan los usuarios, mensajes y conversaciones.

Servicios: contienen la lógica de las operaciones.

Almacenamiento: se encargará de guardar y recuperar los datos.

La comunicación en tiempo real mediante WebSocket y el almacenamiento permanente podrán incorporarse según el alcance de la implementación.

7.Funcionalidades propuestas

Las principales funcionalidades del sistema son:

Registro de usuarios.

Inicio de sesión.

Creación de conversaciones individuales y grupales.

Envío y consulta de mensajes.

Registro de fechas y horas.

Consulta de estadísticas básicas de uso.

Administración de usuarios y permisos.

Estas funcionalidades representan el alcance previsto del proyecto. Su estado de implementación deberá actualizarse a medida que avance el desarrollo.

8.Estructura del repositorio

conectapyme-go/
├── cmd/
│   └── server/
│       └── main.go
├── internal/
│   ├── models/
│   ├── services/
│   ├── handlers/
│   └── storage/
├── docs/
│   ├── 01_contexto_y_seleccion.pdf
│   ├── 02_actores_y_responsabilidades.pdf
│   ├── 03_contrato_comunicacion.pdf
│   ├── 04_diagrama_uml.pdf
│   ├── 05_cronograma.pdf
│   └── 06_guion_video.pdf
├── tests/
├── README.md
├── LICENSE
├── TASKS.md
└── go.mod

La estructura puede cambiar durante el desarrollo, dependiendo de las necesidades del proyecto.

9.Documentación

En la carpeta docs/ se encuentra la documentación del proyecto:

Archivo

Descripción

01_contexto_y_seleccion.pdf

Descripción del problema, objetivos y solución seleccionada.

02_actores_y_responsabilidades.pdf

Matriz de actores, roles y responsabilidades.

03_contrato_comunicacion.pdf

Acuerdos de comunicación y organización del equipo.

04_diagrama_uml.pdf

Diseño de clases y relaciones del sistema.

05_cronograma.pdf

Planificación de las actividades.

06_guion_video.pdf

Guion para la presentación del proyecto.

Los nombres deben coincidir con los archivos que realmente se hayan subido al repositorio.

10.Requisitos para ejecutar el proyecto

Para ejecutar el código se necesita:

Tener instalado Go.

Tener Git instalado si se desea clonar el repositorio.

Contar con una terminal o editor de código, como Visual Studio Code.

11.Instalación y ejecución

Primero, clonar el repositorio:

git clone https://github.com/TU-USUARIO/conectapyme-go.git

Ingresar a la carpeta:

cd conectapyme-go

Descargar las dependencias del proyecto:

go mod tidy

Ejecutar el servidor:

go run ./cmd/server

Importante: el comando de ejecución depende de la implementación actual de main.go. Si el servidor todavía no tiene todas las funciones del chat, estas instrucciones solo ejecutarán las operaciones que estén desarrolladas hasta el momento.

12.Organización del equipo

El proyecto será desarrollado por tres integrantes:

Integrante

Responsabilidad principal

Jose Vaca

Coordinación y documentación.

Dehivid Salgado

Desarrollo del servidor y lógica del sistema.

Mateo Cañar

Diseño UML, pruebas y revisión técnica.

Los nombres y las responsabilidades deberán actualizarse de acuerdo con la distribución real del trabajo.

13.Seguimiento de tareas

Las actividades del proyecto se registrarán en el archivo TASKS.md o en el tablero de tareas de GitHub.

Cada tarea tendrá una descripción, un responsable y un estado para facilitar el seguimiento del avance.

Los estados que se utilizarán serán:

Pendiente.

En progreso.

En revisión.

Completada.

14.Seguridad y privacidad

El sistema deberá proteger la información de los trabajadores y limitar el acceso a las conversaciones según los permisos establecidos.

Se propone implementar autenticación, validación de datos, protección de credenciales y conexiones cifradas. Estas medidas deberán desarrollarse y probarse antes de considerar completa la solución.

15.Licencia

El proyecto propone utilizar la licencia MIT. La licencia definitiva se encuentra en el archivo LICENSE del repositorio y deberá revisarse antes de publicar el código.


16.Estado del proyecto

Estado actual: desarrollo inicial y documentación del proyecto.

El proyecto se irá actualizando conforme se implementen y prueben las funcionalidades. No se considerará terminada una función hasta comprobar que funciona correctamente.

17.Integridad académica

Los integrantes del grupo son responsables de revisar y comprender el contenido entregado. Las herramientas digitales y de inteligencia artificial podrán utilizarse como apoyo, respetando las indicaciones del docente y las normas académicas de la universidad.

Las funciones, pruebas y resultados descritos en este repositorio deberán corresponder al trabajo realmente realizado por el equipo.