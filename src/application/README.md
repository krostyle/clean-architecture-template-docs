Capa de Aplicación

La capa de aplicación en la arquitectura limpia se sitúa entre la capa de dominio y la capa de infraestructura. Su objetivo principal es orquestar el flujo de operaciones de la aplicación y coordinar la interacción entre la capa de dominio y la capa de infraestructura.

En esta capa, encontraremos la lógica de los casos de uso de la aplicación, también conocida como interactores. Los casos de uso definen todas las posibles acciones que un usuario (o un agente externo) puede realizar en la aplicación. Cada caso de uso es un camino único que el usuario puede tomar a través de la aplicación, lo que incluye la interacción con varias entidades de negocio y la coordinación de diversos servicios del dominio.

Esta capa no debe contener lógica de negocio (que pertenece a la capa de dominio) ni detalles de implementación tecnológica (que pertenecen a la capa de infraestructura). En cambio, su objetivo es capturar las intenciones del usuario y coordinar la interacción entre las otras capas para cumplir con esas intenciones.