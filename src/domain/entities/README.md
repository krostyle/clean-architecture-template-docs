Capa de Dominio: Entidades/Modelos
Las entidades, también conocidas como modelos de dominio, son parte fundamental en DDD. Estas son las representaciones de los conceptos y operaciones de alto nivel que existen en el dominio del problema que estás tratando de resolver. En términos sencillos, podríamos decir que son los "objetos" del mundo real que tu aplicación manipulará.

Características de las Entidades en DDD:
Identidad: Las entidades tienen una identidad que no cambia aunque sus atributos sí lo hagan. Por ejemplo, un usuario de una aplicación sigue siendo el mismo usuario aunque cambie su dirección de correo electrónico.

Comportamiento: Las entidades encapsulan tanto el estado (datos) como el comportamiento (lógica del dominio). Esto significa que los métodos y operaciones que las entidades contienen no son simplemente para obtener o establecer datos, sino que también implementan las reglas de negocio del dominio.

Consistencia: Las entidades son responsables de mantener la consistencia de sus estados. Por ejemplo, si un objeto "Pedido" tiene una lista de "Artículos", debería haber métodos para añadir o eliminar "Artículos" de esa lista, y estas operaciones deberían garantizar que la lista de "Artículos" siempre esté en un estado válido.

Las entidades son el núcleo de tu modelo de dominio y deben ser diseñadas cuidadosamente para reflejar con precisión el dominio del problema que estás intentando resolver.