# Práctica 4 - API REST con Spring Boot

**Autor:** Paula Bonet Sánchez

**Objetivo:** Crear una API REST con Spring Boot.

---

## Descripción del proyecto

Esta API permite gestionar una lista de películas, basandonos en mi práctica 2. 
En mi caso, la api pertenece a la sección de Clásicas de la web. He dejado 3 fijas para que al cargar la pagina no este vacía.
Incluye operaciones de creación, lectura, actualización y borrado (CRUD).

---
## Cómo ejecutar el proyecto

1. Abrir el proyecto en IntelliJ
2. Ejecutar la clase `PeliculasApiApplication`
4. Abrir el navegador en `http://localhost:8080/api/peliculas`
   
---

## Descripción de cada Endpoint

| Método | Ruta                         | Cuerpo (JSON)                                       | Descripción                                 | Respuesta esperada                      |
|--------|------------------------------|-----------------------------------------------------|---------------------------------------------|-----------------------------------------|
| GET    | `/api/peliculas`             | -                                                   | Devuelve la lista de todas las películas     | 200 OK - Lista de películas             |
| GET    | `/api/peliculas/{id}`        | -                                                   | Devuelve una película por su ID              | 200 OK / 404 Not Found                  |
| POST   | `/api/peliculas`             | `{ "titulo": "...", "anio": ..., ... }`             | Crea una nueva película                      | 201 Created - Película creada           |
| PUT    | `/api/peliculas/{id}`        | `{ "titulo": "...", "anio": ..., ... }`             | Actualiza una película existente             | 200 OK / 404 Not Found                  |
| DELETE | `/api/peliculas/{id}`        | -                                                   | Elimina una película por su ID               | 204 No Content / 404 Not Found          |

---
## Ejemplo de uso

### GET `/api/peliculas`
Para comprobar que funciona, hay que abrir Postman y pegar lo siguiente:
```json
{
  "titulo": "Pulp Fiction",
  "anio": 1994,
  "director": "Tarantino",
  "sinopsis": "Dos matones, envueltos en una violencia espectacular e irónica",
  "imagenUrl": "https://static.posters.cz/image/750/posters/pulp-fiction-cover-i1288.jpg"
}

---

La pelicula de Pulp Fiction debe aparecer en la web, en la seccion de clásicas. A parte de esta acción, se puede aplicar el ejemplo con cualquiera de los métodos indicados en la tabla.
Adunto aquí imagenes de la web y de la api con la nueva película cargada:
<img width="956" alt="image" src="https://github.com/user-attachments/assets/92531304-557a-457d-b0c3-a504e720335b" />
<img width="959" alt="image" src="https://github.com/user-attachments/assets/0da77765-1f99-43b7-8a93-ae6b0fca6f98" />

