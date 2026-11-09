# API REST de Series - Spring Boot

Proyecto desarrollado para la práctica de Desarrollo Back-End (PUCE). Consiste en una API REST para gestionar un catálogo de series de televisión implementando operaciones CRUD, utilizando Spring Boot, Spring Data JPA y base de datos H2.

## Tecnologías utilizadas
- Java 21
- Spring Boot
- Spring Data JPA
- Base de datos en memoria H2
- Lombok
- Maven

## Estructura del proyecto
El proyecto sigue una arquitectura en capas:
- `controller/`: Controladores REST (`SerieController.java`).
- `service/`: Lógica de negocio y servicios (`SerieService.java`).
- `repository/`: Repositorios JPA (`SerieRepository.java`).
- `models/`: Entidad `Serie.java` mapeada a base de datos.

## Endpoints de la API
| Método | Endpoint | Descripción |
| :--- | :--- | :--- |
| `GET` | `/api/series` | Listar todas las series |
| `GET` | `/api/series/{id}` | Buscar una serie por su ID |
| `POST` | `/api/series` | Crear una nueva serie |
| `PUT` | `/api/series/{id}` | Actualizar una serie existente |
| `DELETE` | `/api/series/{id}` | Eliminar una serie |

### Formato de ejemplo (JSON) para POST / PUT:
```json
{
  "titulo": "Breaking Bad",
  "plataforma": "Netflix",
  "calificacion": 9.5
}
```

## Instrucciones de ejecución
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/aomaldonado/Restcontroller.git
   ```
2. Abrir el proyecto en IntelliJ IDEA o cualquier IDE compatible.
3. Ejecutar la clase principal `SeriesApiApplication.java`.
4. El servidor se iniciará en el puerto `8080`.

## Base de datos (H2 Console)
La base de datos en memoria está habilitada para verificar los registros:
- **URL:** http://localhost:8080/h2-console/
- **JDBC URL:** `jdbc:h2:mem:seriesdb`
- **User Name:** `sa`
- **Password:** *(dejar vacío)*