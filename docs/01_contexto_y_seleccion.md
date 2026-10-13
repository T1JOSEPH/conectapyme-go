ConectaPyme: Contexto y selección del sistema

1.Contexto del problema

La empresa ha abierto una segunda sede y necesita mejorar la comunicación entre sus trabajadores. Al utilizar diferentes medios para compartir información, algunos mensajes pueden perderse o las respuestas pueden tardar más de lo esperado.

Por esta razón, se propone crear ConectaPyme, un sistema de comunicación interna que permita centralizar los mensajes y facilitar el trabajo entre las dos sedes.

2.Sistema seleccionado

Se seleccionó un sistema de chat interno para empresas. La plataforma permitirá que los trabajadores puedan comunicarse mediante conversaciones individuales y grupales.

3.Objetivo general

Desarrollar una propuesta de sistema de comunicación interna utilizando Go, con una arquitectura cliente-servidor que facilite la comunicación entre los trabajadores.

4.Objetivos específicos

Identificar las necesidades de comunicación de la empresa.

Diseñar la estructura del sistema mediante UML.

Organizar el código utilizando Git y GitHub.

Desarrollar las funciones principales del servidor.

Realizar pruebas para comprobar el funcionamiento del sistema.

5.Funcionamiento cliente-servidor

El cliente enviará solicitudes al servidor para realizar operaciones, como enviar mensajes o consultar conversaciones. El servidor procesará las solicitudes, validará los datos y devolverá una respuesta.

Se propone utilizar HTTP para las solicitudes iniciales. La comunicación en tiempo real podrá incorporarse mediante WebSocket en una etapa posterior.

6.Estadísticas del sistema

El sistema podrá registrar información como la cantidad de usuarios activos, mensajes enviados, conversaciones creadas, tiempo de respuesta y errores del servidor.

Estos indicadores permitirán evaluar el funcionamiento de la plataforma sin exponer innecesariamente la información privada de los trabajadores.

7.Seguridad

Se propone implementar autenticación, validación de permisos, protección de credenciales y conexiones cifradas. Estas funciones deberán desarrollarse y probarse durante la implementación.

8.Conclusión

ConectaPyme busca mejorar la comunicación entre los trabajadores de una empresa con dos sedes. La propuesta permitirá organizar los mensajes en una plataforma centralizada y establecer una base para futuras mejoras.

El desarrollo se realizará por etapas, comenzando con el diseño y continuando con la implementación y las pruebas.