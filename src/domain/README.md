Capa de Dominio
La capa de dominio es el corazón de la aplicación y contiene la lógica de negocio. Esta es la capa más importante y es donde reside el modelo de dominio, que es una abstracción del negocio. En el diseño orientado al dominio (DDD), el dominio se divide en varios componentes clave que trabajan juntos para modelar el comportamiento y las reglas del negocio.



Componentes clave de la capa de dominio:
Entities (Entidades): Son objetos que tienen una identidad que se mantiene constante a lo largo del tiempo (incluso si sus atributos cambian). Las entidades suelen tener un identificador único y encapsulan tanto el estado como el comportamiento que es relevante para su identidad.

Value Objects: Los Value Objects, o Objetos de Valor, son una de las construcciones fundamentales en DDD. Son objetos pequeños que no tienen una identidad y se comparan únicamente en función de sus atributos, no su identidad. Los Value Objects suelen ser inmutables y se utilizan para describir aspectos del dominio que no requieren identidad, como una dirección de correo electrónico, una cantidad de dinero o un rango de fechas.

Aggregates: Los Aggregates, o Agregados, son un patrón de DDD que proporciona un límite claro y garantías de consistencia para un grupo de entidades y Value Objects. Un Agregate es una entidad o grupo de entidades y Value Objects que se consideran una sola unidad con respecto a la persistencia de datos, y cualquier regla de consistencia se aplica al Agregate como un todo.

Domain Services (Puertos primarios): Los Domain Services, o Servicios de Dominio, son operaciones de nivel superior que coordinan varias entidades y Aggregates, o encapsulan ciertas operaciones que no pertenecen naturalmente a ninguna entidad o Agregate. Los Servicios de Dominio se utilizan para expresar comportamientos del dominio que son una secuencia de operaciones pero que no pertenecen a ningún objeto en particular.

Domain Events: Los Domain Events, o Eventos de Dominio, son un patrón de DDD que ayuda a desacoplar distintas partes del sistema y a registrar los cambios de estado que tienen un significado de negocio. Un Evento de Dominio es algo que sucede en el sistema que es importante para los usuarios o para el negocio en sí, como un pedido completado, un usuario registrado, etc.

Repositories (Puertos secundarios): Los Repositories, o Repositorios, son un patrón de DDD que proporciona una abstracción para la persistencia de datos. Un Repositorio se comporta como una colección de Aggregates, y permite guardar y recuperar Aggregates sin tener que conocer los detalles de cómo se realiza la persistencia de datos.

Otros Componentes que pueden existir en la capa de dominio:

Factories: Las Factories son un concepto común en la programación orientada a objetos y se utilizan tanto en DDD como en la Arquitectura Limpia. Una Factory es un componente cuya responsabilidad es la creación de objetos. En el contexto del dominio de negocio, las Factories pueden ser utilizadas para encapsular la lógica de creación de entidades o de objetos de valor, especialmente cuando este proceso es complejo o requiere algún tipo de validación.
Por ejemplo, podrías tener una Factory para crear pedidos en un sistema de comercio electrónico. Esta Factory se encargaría de validar los datos del pedido, crear el objeto Pedido, asignarle un ID único, y quizás realizar otras operaciones como verificar la disponibilidad del inventario.

Builders: Los Builders, como las Factories, son un patrón de diseño comúnmente utilizado en la programación orientada a objetos y pueden ser utilizados en ambos enfoques, DDD y Arquitectura Limpia. El patrón Builder es útil cuando necesitas crear un objeto complejo que requiere múltiples pasos para su creación o cuando la construcción de un objeto puede tener muchas representaciones posibles.
Un ejemplo podría ser la creación de un objeto "Menu" en un sistema de restaurante, donde un Menu podría tener varias opciones y cada opción podría tener varios ingredientes. Un Builder podría proporcionar una interfaz fluida para construir este objeto paso a paso.

Specifications: Las Specifications, o Especificaciones, son un patrón de DDD que se utiliza para encapsular las reglas de negocio que se pueden utilizar para comprobar si un Aggregate o entidad cumple con ciertos criterios. Las Specifications se utilizan para comprobar si un Aggregate o entidad cumple con ciertos criterios, y se pueden utilizar para validar Aggregates y entidades, o para filtrar Aggregates y entidades de una colección.

