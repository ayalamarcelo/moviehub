<h1 align="center">🎬 Movie Hub</h1>

<p>This project is a backend application developed in Java using Servlet, Apache Tomcat and MySQL. The purpose of the project is to provide an API for managing movies, including CRUD operations with Postman.</p>


## 📁 Project Structure
```
backend/
├── .idea/
├── cmarttomcat/
├── src/
│   └── main/
│       ├── java/
│       │   └── org/
│       │       ├── application/
│       │       │   └── services/
│       │       │       ├── adapters/
│       │       │       │   └── IRepository.java
│       │       │       └── services/
│       │       │           └── IRepository.java
│       │       ├── domain/
│       │       │   └── models/
│       │       │       └── MovieService.java
│       │       └── infrastructure/
│       │           └── repository/
│       │               ├── controllers/
│       │               │   └── MovieController.java
│       │               └── database/
│       │                   ├── DatabaseConnection.java
│       │                   └── MySqlRepositoryImpl.java
│       ├── resources/
│       │   └── movies_db.sql
│       └── webapp/
│           └── WEB-INF/
│               └── index.jsp
├── .gitignore
├── backend.iml
├── pom.xml
└── README.md
```

## ⚙️ Requirements

- [x] JDK 17
- [x] Apache Tomcat 9.0
- [x] MySQL
- [x] Maven

## 🛠️ Environment Configuration
Database

1. Create a database in MySQL (Copy the one from the resource folder `movies_db.sql`)
2. Clone repository (It is recommended to do a FORK)
``` bash
git clone https://github.com/tu-usuario/movie-hub.git
```
   
3. Configure Apache Tomcat to deploy the application.

> [!NOTE]
> Change port in Apache Tomcat

```dtd
Connector port=”8090″ protocol=”HTTP/1.1″ connectionTimeout=”20000″ redirectPort=”8443″
```

## Use
Use your IDE (like IntelliJ IDEA or Eclipse) or Tomcat Manager to deploy the project.
Verify that the root path (index.jsp) is working properly.

*Endpoints*:

* GET /movies/{id}: Gets a movie by ID.
* POST /movies Create a new movie.
* PUT /movies/{id}: Update an existing movie.
* DELETE /movies/{id}: Delete a movie by ID.

> [!TIP]
> For PUTs on postman: 
> 1. Select: Body
> 2. Select: Rows
> 3. Paste a JSON on rows:
```
{
  "id":1,
  "title":"The Lord of the Rings",
  "director": "Peter Jackson",
  "genre": "Fantasy"
}
```

### 📌 Final Notes

- Make sure your MySQL and Tomcat services are up and properly configured.
- Check and update database credentials in DatabaseConnection.java if needed.
