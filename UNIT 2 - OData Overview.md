# UNIT 2 - OData Overview

## Después de completar esta unidad, podrá:

* Describir la transferencia de estado representacional (REST)
* Examinar un servicio OData
* Realizar operaciones de lectura de OData
* Realizar consultas de OData

## Contenido

- Explicación de la transferencia de estado representacional (REST)

## REST – Los principios fundamentales de la World Wide Web

Representational State Transfer (REST) ​​es una filosofía de diseño que define seis restricciones arquitectónicas. Estas restricciones rigen el comportamiento a gran escala de los participantes dentro de un sistema de software en red. Las restricciones de diseño REST se implementan completamente mediante el protocolo HTTP. La World Wide Web es un ejemplo de un sistema de software completamente RESTful.

Es importante señalar que el hecho de que un protocolo de aplicación utilice HTTP no garantiza que sea RESTful. Un ejemplo destacado es el Protocolo simple de acceso a objetos (SOAP), que utiliza el protocolo HTTP para enviar mensajes SOAP. Sin embargo, el protocolo SOAP no es RESTful.

### Restricciones de diseño de una arquitectura RESTful

Una arquitectura RESTful debe cumplir:

* Arquitectura cliente-servidor
* Capacidad de almacenamiento en caché
* Sin estado
* Sistema en capas
* Interfaz uniforme
* Código a pedido

1. ### Arquitectura cliente-servidor

Los participantes de una arquitectura RESTful deben implementar el modelo cliente-servidor, que permite que los componentes de software del cliente y del servidor se desarrollen de forma independiente. Supone que el cliente no participará en el almacenamiento de datos a largo plazo y que el servidor no participará en la presentación de los datos que proporciona. Este principio se conoce como separación de preocupaciones.


2. Capacidad de almacenamiento en caché
Para mejorar el rendimiento y la escalabilidad, cada respuesta del servidor debe llevar consigo un indicador que indique si se puede almacenar en caché o no para su uso futuro. Esto es para evitar que el cliente trabaje con datos obsoletos.


3. Sin estado
La comunicación entre los participantes debe ser sin estado. Una interfaz sin estado requiere que el cliente proporcione toda la información necesaria para que el servidor procese la solicitud. La información de la sesión debe mantenerse en el lado del cliente. El servidor puede almacenar información sobre el estado del cliente, sin embargo, el cliente debe conocer dicha información y poder acceder a ella.


4. Sistema en capas
La comunicación entre los participantes debe ser en capas. Cuando el cliente se comunica con un servidor, no debería poder distinguir si se ha comunicado con el servidor de punto final real que proporcionará la información solicitada o con algún servidor intermedio utilizado para la escalabilidad o seguridad del sistema.

5. Interfaz uniforme
Una interfaz uniforme entre los clientes y los servidores desacopla la arquitectura. Una interfaz uniforme tiene las siguientes características:

    5.1 El servidor debe proporcionar al cliente una representación (por ejemplo, una URL) de sus recursos.

    5.2 Se debe proporcionar un medio para que el cliente manipule esos recursos (por ejemplo, proporcionar operaciones como Crear, Leer, Actualizar, Eliminar, etc.).

    5.3 Todas las respuestas enviadas al cliente deben ser autodescriptivas.

    5.4 La manipulación de los recursos del lado del servidor solo puede realizarse mediante hipermedios (es decir, enlaces) proporcionados por el servidor.

6. Código a pedido
El servidor puede entregar código a pedido al cliente. A petición del cliente, el servidor debe poder proporcionar código ejecutable adicional para ampliar las capacidades del cliente. Esto se soluciona en OData mediante el uso de funciones de importación.


### Explicación del protocolo de datos abiertos (OData)

#### Estándar OData

[infraestructura](/img/infraestructura.png)

Un aspecto importante de la arquitectura de la World Wide Web es el uso de interfaces abstractas para la comunicación de componentes. Estas interfaces abstractas se presentan como conectores. Un cliente y un servidor utilizan cada uno un componente conector. Existe un contrato entre ambos conectores que define el protocolo de aplicación. Define los documentos, su formato y el comportamiento. Se puede elegir cualquier protocolo. Al utilizar el concepto de conector, tanto el cliente como el servidor son en gran medida independientes e intercambiables. Cada conector traduce los documentos intercambiados en el canal de comunicación a las representaciones internas tanto en el servidor como en el cliente, y viceversa.

El protocolo OData define dicho contrato especificando un protocolo uniforme que tiene las cualidades necesarias. Por ejemplo, un conector conectado a un sistema back-end de SAP traduce entre API ABAP y entidades OData. SAP Gateway es un conector de este tipo.

Por otro lado, un conector de cliente traduce entre entidades OData y las API de la plataforma del consumidor. El conector se especifica aquí. Como consecuencia, cualquier plataforma de cliente con bibliotecas que admitan el formato OData contratado puede comunicarse con cualquier servidor que admita el mismo contrato.

OData sigue el paradigma de diseño de la arquitectura de transferencia de estado representacional (REST) ​​en el sentido de que el protocolo transfiere representaciones del estado de los recursos. El término recurso denota datos que son direccionables y accesibles. La representación de dirección o recurso estándar es el Identificador uniforme de recursos (URI). Un cliente solicita un recurso a un servidor enviando una solicitud a un URI. El servidor procesa la solicitud traduciendo el URI a datos de dirección internos para acceder o manipular los datos y luego ensamblar la respuesta.

#### Open Data Protocol
Vamos a intentar entender qué es el protocolo de datos abiertos.

OData es un estándar abierto desarrollado originalmente por Microsoft pero que ahora gestiona la Organización Oasis. Se basa en los estándares Atom Publishing y Atom Syndication, que, a su vez, se basan en XML (Extensible Markup Language) y HTTP(S) (HyperText Transfer Protocol (Secure)). JSON (JavaScript Object Notation) es una alternativa a XML para estructurar datos.


### Realización de operaciones OData

### Realización de consultas OData

### Cuestionario