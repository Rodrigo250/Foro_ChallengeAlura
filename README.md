# 📌 Foro Hub - Challenge Back-End

Este es un proyecto de **API REST** desarrollado como parte del **"Challenge Back-End - Foro Hub"** de **Alura Latam** y **Oracle One**.  
La aplicación permite a los usuarios crear, leer, actualizar y eliminar tópicos de discusión, así como interactuar con respuestas y gestionar su perfil.

---

## 🚀 Tecnologías Utilizadas
- **Java 17**: Lenguaje de programación principal.  
- **Spring Boot 3**: Framework para la construcción de la aplicación.  
- **Spring Security**: Autenticación y autorización con tokens JWT.  
- **Spring Data JPA**: Persistencia de datos e interacción con la base de datos.  
- **MySQL**: Sistema de gestión de base de datos relacional.  
- **JWT (JSON Web Tokens)**: Autenticación segura sin estado.  
- **Maven**: Gestión de dependencias.  
- **Lombok**: Eliminación de código repetitivo (getters, setters, etc.).  
- **Flyway**: Gestión de migraciones de base de datos.  

---

## ✨ Funcionalidades

### 🔐 Autenticación y Autorización
- Registro y login de usuarios.  
- Uso de JWT para proteger los endpoints.  

### 📑 Gestión de Tópicos
- **Crear**: Un usuario autenticado puede crear un nuevo tópico.  
- **Listar**: Obtener todos los tópicos con paginación.  
- **Ver**: Consultar un tópico específico.  
- **Actualizar**: El autor del tópico puede modificarlo.  
- **Eliminar**: El autor del tópico puede eliminarlo.  

### 💬 Gestión de Respuestas
- **Crear**: Un usuario puede responder a un tópico.  
- **Actualizar**: El autor de la respuesta puede modificarla.  
- **Marcar como Solución**: El autor del tópico puede marcar una respuesta como solución.  

### ✅ Validaciones
- No se permiten tópicos duplicados (mismo título y mensaje).  

---

## 💻 Requisitos del Sistema
- **JDK 17** o superior.  
- **Maven**.  
- **MySQL 8.0** o superior.  

---

## ⚙️ Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone <url-del-repositorio>

Configurar la base de datos:

Crear una base de datos en MySQL con el nombre forohub.

Abrir el archivo src/main/resources/application.properties y configurar las credenciales:

spring.datasource.url=jdbc:mysql://localhost:3306/forohub
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña

Ejecutar la aplicación:

Desde un IDE (IntelliJ, VS Code, etc.) o usando Maven:

mvn spring-boot:run

La aplicación correrá por defecto en:
👉 http://localhost:8080

## 📝 Endpoints de la API

Se puede probar con **Postman** o **Insomnia**.

| Endpoint                   | Método | Descripción |
|----------------------------|--------|-------------|
| `/login`                   | POST   | Autenticación de usuario. Retorna un token JWT. |
| `/topicos`                 | GET    | Lista todos los tópicos (paginación con `?page=0&size=10`). |
| `/topicos`                 | POST   | Crea un nuevo tópico (requiere autenticación). |
| `/topicos/{id}`            | GET    | Obtiene un tópico por su ID. |
| `/topicos/{id}`            | PUT    | Actualiza un tópico por su ID (requiere autenticación). |
| `/topicos/{id}`            | DELETE | Elimina un tópico por su ID (requiere autenticación). |
| `/topicos/{id}/respuestas` | POST   | Crea una respuesta en un tópico (requiere autenticación). |


👨‍💻 Autor
Rodrigo Linares

