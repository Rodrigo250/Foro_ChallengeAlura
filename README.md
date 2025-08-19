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
