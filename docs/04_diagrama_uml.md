ConectaPyme: Diagrama UML

1.Descripción

El diagrama UML representa la estructura propuesta para el sistema de comunicación interna ConectaPyme. Se muestran las clases principales, sus atributos, métodos y las relaciones entre los componentes del cliente y del servidor.

El diseño utiliza composición para representar que una conversación contiene mensajes. También se incluye una interfaz para separar la lógica del sistema del mecanismo de almacenamiento.

2.Diagrama de clases

classDiagram
direction TB

namespace Cliente {
    class ClienteChat {
        -string usuarioId
        +enviarMensaje(string conversacionId, string texto) error
        +consultarMensajes(string conversacionId) Mensaje[]
    }
}

namespace Servidor {
    class Usuario {
        -string id
        -string nombre
        -string correo
        +validarDatos() bool
    }

    class Conversacion {
        -string id
        -string nombre
        +agregarMensaje(Mensaje mensaje) error
        +listarMensajes() Mensaje[]
    }

    class Mensaje {
        -string id
        -string texto
        -string fechaHora
        +validar() bool
    }

    class ChatHandler {
        +enviarMensaje(Request request) Response
        +consultarMensajes(Request request) Response
    }

    class ChatService {
        +enviarMensaje(string conversacionId, string texto) error
        +obtenerMensajes(string conversacionId) Mensaje[]
    }

    class MensajeRepository {
        <<interface>>
        +guardar(Mensaje mensaje) error
        +listar(string conversacionId) Mensaje[]
    }

    class MemoriaMensajes {
        -map mensajes
        +guardar(Mensaje mensaje) error
        +listar(string conversacionId) Mensaje[]
    }
}

ClienteChat ..> ChatHandler : solicitudes HTTP
ChatHandler ..> ChatService : utiliza
ChatService ..> MensajeRepository : depende de
MemoriaMensajes ..|> MensajeRepository : implementa

Usuario "0..*" -- "0..*" Conversacion : participa
Conversacion "1" *-- "0..*" Mensaje : contiene

3.Descripción de las clases

ClienteChat

Representa el componente utilizado por el trabajador para enviar mensajes y consultar conversaciones.

Usuario

Representa a una persona registrada en el sistema. Contiene su identificador, nombre y correo electrónico.

Conversacion

Representa una conversación individual o grupal. Permite agregar mensajes y consultar los mensajes que contiene.

Mensaje

Representa un mensaje enviado dentro de una conversación. Guarda su identificador, texto y fecha y hora.

ChatHandler

Se encarga de recibir las solicitudes HTTP y dirigirlas a los servicios correspondientes.

ChatService

Contiene la lógica principal del chat y coordina las operaciones de envío y consulta de mensajes.

MensajeRepository

Es una interfaz que define las operaciones necesarias para guardar y consultar mensajes sin depender de un sistema de almacenamiento específico.

MemoriaMensajes

Es una implementación inicial de la interfaz que puede almacenar mensajes temporalmente en memoria. Para conservarlos después de reiniciar el servidor será necesario implementar un almacenamiento persistente.

4.Relaciones entre las clases

ClienteChat y ChatHandler: el cliente envía solicitudes HTTP al servidor.

ChatHandler y ChatService: el manejador utiliza los servicios para procesar las solicitudes.

ChatService y MensajeRepository: el servicio depende de una interfaz para guardar y consultar mensajes.

MemoriaMensajes y MensajeRepository: la clase MemoriaMensajes implementa las operaciones definidas por la interfaz.

Usuario y Conversacion: varios usuarios pueden participar en diferentes conversaciones.

Conversacion y Mensaje: una conversación puede contener cero o muchos mensajes. La composición indica que los mensajes forman parte de la conversación en este modelo.

5.Visibilidad de los elementos

En UML se utilizan símbolos para indicar el acceso a los atributos y métodos:

significa público: puede utilizarse desde otros componentes.

significa privado: pertenece a la implementación interna de la clase.

6.Relación con Go

Las clases del diagrama se pueden representar en Go mediante estructuras (struct), métodos y una interfaz (interface).

Por ejemplo, Usuario, Mensaje y Conversacion pueden representarse mediante estructuras. MensajeRepository puede definirse como una interfaz con los métodos Guardar y Listar.

Go no necesita utilizar herencia para este diseño. La relación entre los componentes se organiza mediante composición y el uso de interfaces.

7.Conclusión

El diagrama propone una estructura modular que separa el cliente, el procesamiento de solicitudes, la lógica del chat y el almacenamiento. Esto facilita mantener el código organizado y permite cambiar la implementación del almacenamiento sin modificar toda la lógica del sistema.

El diagrama representa el diseño propuesto y deberá actualizarse si la implementación final cambia.