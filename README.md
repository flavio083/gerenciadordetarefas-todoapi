# 📋 Todo API — Spring Boot + Frontend Integrado

A simple task management system developed with Java, Spring Boot, PostgreSQL and a frontend in HTML, CSS and JavaScript.

This project allows you to create, list, update, complete and delete tasks through a REST API integrated with a responsive web interface.

---

# 🚀 Features

✅ Create tasks  
✅ List tasks  
✅ Update tasks  
✅ Delete tasks  
✅ Change status (PENDING, IN_PROGRESS, DONE)  
✅ PostgreSQL persistence  
✅ REST API  
✅ Integrated frontend  
✅ Swagger/OpenAPI  
✅ Docker support  
✅ Render deployment

---

# 🛠 Technologies

- Java 21
- Spring Boot 3
- Spring Data JPA
- PostgreSQL
- Maven
- Lombok
- Docker
- HTML5
- CSS3
- JavaScript
- Swagger/OpenAPI
- Render

---

# 📂 Project Structure

```
todo-api/
├── src/
│   ├── main/
│   │   ├── java/com/flaviano/todo/
│   │   │   ├── TodoApiApplication.java           # Classe principal da aplicação
│   │   │   ├── config/
│   │   │   │   └── WebConfig.java                # Configuração CORS
│   │   │   ├── controller/
│   │   │   │   └── TaskController.java           # REST endpoints (GET, POST, PUT, DELETE)
│   │   │   ├── service/
│   │   │   │   └── TaskService.java              # Lógica de negócio
│   │   │   ├── repository/
│   │   │   │   └── TaskRepository.java           # Camada de acesso a dados
│   │   │   ├── entity/
│   │   │   │   └── Task.java                     # Modelo de domínio
│   │   │   ├── dto/
│   │   │   │   └── TaskRequest.java              # Data Transfer Object
│   │   │   ├── enums/
│   │   │   │   └── TaskStatus.java               # Status da tarefa (PENDING, IN_PROGRESS, DONE)
│   │   │   └── exception/
│   │   │       ├── GlobalExceptionHandler.java   # Tratamento centralizado de exceções
│   │   │       └── TaskNotFoundException.java    # Exceção customizada
│   │   └── resources/
│   │       ├── application.yaml                  # Configuração padrão (H2)
│   │       ├── application-prod.yaml             # Configuração produção (PostgreSQL)
│   │       └── static/                           # Frontend integrado
│   │           ├── index.html
│   │           ├── css/style.css
│   │           └── js/script.js
│   └── test/
│       └── java/com/flaviano/todo/
│           └── TodoApiApplicationTests.java      # Testes de integração
├── frontend/                                     # Frontend em desenvolvimento
│   ├── index.html
│   ├── css/style.css
│   └── js/script.js
├── pom.xml                                       # Dependências Maven
├── Dockerfile                                    # Configuração Docker
└── README.md
```

---

# ⚙️ Configuration

The application uses H2 in development mode and PostgreSQL in production mode.

Example configuration:

```yaml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
    driver-class-name: org.h2.Driver
  jpa:
    database-platform: org.hibernate.dialect.H2Dialect
```

For production, use `application-prod.yaml` with PostgreSQL variables.

---

# 🔧 Installation

Clone the repository:

```bash
git clone https://github.com/flavio083/todo-api.git
cd todo-api
```

Run the project:

```bash
./mvnw spring-boot:run
```

Or on Windows:

```bash
mvnw.cmd spring-boot:run
```

---

# ▶️ Running

The application will start on:

```text
http://localhost:8080
```

Swagger UI:

```text
http://localhost:8080/swagger-ui/index.html
```

---

# 📖 Main Endpoints

```http
GET /tasks
GET /tasks/{id}
POST /tasks
PUT /tasks/{id}
DELETE /tasks/{id}
```

Example JSON:

```json
{
  "title": "Estudar Spring Boot",
  "description": "Criar projeto para portfólio",
  "status": "PENDING"
}
```

---

# 🎯 Learning Outcomes

This project helped me improve in:

- REST API development
- Spring Boot architecture
- JPA and database integration
- Frontend and backend integration
- Docker and deployment basics
- Git and GitHub workflow

---

# 👨‍💻 Author

Flaviano Aguiar Silva Filho

🐙 GitHub: https://github.com/flavio083  
💼 LinkedIn: https://www.linkedin.com/in/flaviano-aguiar-173a93343

---

# 🔗 Useful Links

- Repository: https://github.com/flavio083/todo-api
- Online app: https://todo-api-chfi.onrender.com
- Swagger: https://todo-api-chfi.onrender.com/swagger-ui/index.html

---