Foro Hub - Challenge Back-End
Este es un proyecto de API REST desarrollado como parte del "Challenge Back-End - Foro Hub" de Alura Latam y Oracle One. La aplicación permite a los usuarios crear, leer, actualizar y eliminar tópicos de discusión, así como interactuar con respuestas y gestionar su perfil.

🚀 Tecnologías Utilizadas
Java 17: El lenguaje de programación principal.
Spring Boot 3: Framework para la construcción de la aplicación.
Spring Security: Para la autenticación y autorización de usuarios con tokens JWT.
Spring Data JPA: Para la persistencia de datos y la interacción con la base de datos.
MySQL: Sistema de gestión de base de datos relacional.
JWT (JSON Web Tokens): Para la autenticación segura sin estado.
Maven: Herramienta para la gestión de dependencias del proyecto.
Lombok: Librería para reducir el código repetitivo (getters, setters, etc.).
Flyway: Para gestionar las migraciones de la base de datos.
✨ Funcionalidades
La API ofrece las siguientes funcionalidades:

Autenticación y Autorización: Registro y login de usuarios con JWT para proteger los endpoints.
Gestión de Tópicos:
Crear: Un usuario autenticado puede crear un nuevo tópico.
Listar: Obtener todos los tópicos con paginación.
Ver: Consultar un tópico específico.
Actualizar: El autor del tópico puede modificarlo.
Eliminar: El autor del tópico puede eliminarlo.
Gestión de Respuestas:
Crear: Un usuario puede responder a un tópico.
Actualizar: El autor de la respuesta puede modificarla.
Marcar como Solución: El autor del tópico puede marcar una respuesta como la solución.
Validaciones: Se implementaron validaciones de reglas de negocio, como no permitir tópicos duplicados (mismo título y mensaje) en la base de datos.
💻 Requisitos del Sistema
JDK 17 o superior.
Maven.
MySQL 8.0 o superior.
⚙️ Instalación y Configuración
Clonar el repositorio:
git clone
Configurar la base de datos:
Crea una base de datos en MySQL con el nombre forohub.
Abre el archivo src/main/resources/application.properties y configura las credenciales de tu base de datos:
spring.datasource.url=jdbc:mysql://localhost:3306/forohub
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
Ejecutar la aplicación:
Puedes ejecutarla desde tu IDE (IntelliJ, VS Code, etc.) o desde la terminal usando Maven:
mvn spring-boot:run
La aplicación se ejecutará en el puerto 8080 por defecto.

📝 Endpoints de la API
La API se puede probar con herramientas como Postman o Insomnia. Los endpoints principales son:

Endpoint	Método HTTP	Descripción
/login	POST	Autenticación del usuario. Retorna un token JWT.
/topicos	GET	Lista todos los tópicos. Acepta paginación (?page=0&size=10).
/topicos	POST	Crea un nuevo tópico. Requiere autenticación.
/topicos/{id}	GET	Obtiene un tópico por su ID.
/topicos/{id}	PUT	Actualiza un tópico por su ID. Requiere autenticación.
/topicos/{id}	DELETE	Elimina un tópico por su ID. Requiere autenticación.
/topicos/{id}/respuestas	POST	Crea una respuesta para un tópico. Requiere autenticación.

👨‍💻 Autor
Rodrigo Linares
