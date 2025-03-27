# Práctica 4 - API REST con Spring Boot

**Autor:** Paula Bonet  
**Asignatura:** Programación de Aplicaciones Telemáticas  
**Objetivo:** Crear una API REST con Spring Boot conectada a una base de datos H2 en memoria.

---

## 🧩 Descripción del proyecto

Esta API permite gestionar una lista de películas de Pedro Almodóvar.  
Incluye operaciones de creación, lectura, actualización y borrado (CRUD).

---

## 🔗 Endpoints

| Método | Ruta                         | Cuerpo (JSON)                                       | Descripción                                 | Respuesta esperada                      |
|--------|------------------------------|-----------------------------------------------------|---------------------------------------------|-----------------------------------------|
| GET    | `/api/peliculas`             | -                                                   | Devuelve la lista de todas las películas     | 200 OK - Lista de películas             |
| GET    | `/api/peliculas/{id}`        | -                                                   | Devuelve una película por su ID              | 200 OK / 404 Not Found                  |
| POST   | `/api/peliculas`             | `{ "titulo": "...", "anio": ..., ... }`             | Crea una nueva película                      | 201 Created - Película creada           |
| PUT    | `/api/peliculas/{id}`        | `{ "titulo": "...", "anio": ..., ... }`             | Actualiza una película existente             | 200 OK / 404 Not Found                  |
| DELETE | `/api/peliculas/{id}`        | -                                                   | Elimina una película por su ID               | 204 No Content / 404 Not Found          |

---

## 🛠 Tecnologías utilizadas

- Java 21
- Spring Boot 3.1.3
- Spring Web
- Spring Data JPA
- H2 Database
- Postman (para probar los endpoints)
- HTML/CSS/JS (interfaz de la práctica 2 reutilizada)

---

## 🚀 Cómo ejecutar el proyecto

1. Clonar o abrir el proyecto en IntelliJ / Eclipse
2. Asegurarse de tener Java 17 o superior
3. Ejecutar la clase `PeliculasApiApplication`
4. Abrir el navegador en `http://localhost:8080/api/peliculas`
