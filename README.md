# Simple TODO Application

A clean, modern TODO app built with **Spring Boot**, **Thymeleaf**, and **Bootstrap 5**.

---

## Features

- Add new tasks
- Toggle tasks as complete / incomplete
- Delete tasks
- Responsive layout with a polished dark UI

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Spring Boot |
| Template Engine | Thymeleaf |
| Frontend | Bootstrap 5.3 |
| Icons | Tabler Icons |
| Fonts | Playfair Display, DM Sans (Google Fonts) |

---

## Getting Started

### Prerequisites

- Java 17+
- Maven or Gradle
- MySQL installed and running

---

### Step 1 — Set Up the Database

The SQL file is provided in the `db/` folder. Import it into MySQL:

```bash
mysql -u root -p < db/todo.sql
```

This will create the database and all required tables automatically.

---

### Step 2 — Configure Database Password

Open `src/main/resources/application.properties` and enter your MySQL password:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/todo_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD_HERE

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Replace `YOUR_PASSWORD_HERE` with your actual MySQL password.

> If your MySQL username is not `root`, update `spring.datasource.username` as well.

---

### Step 3 — Run the Application

```bash
# Clone the repository
git clone https://github.com/your-username/simple-todo-app.git
cd simple-todo-app

# Run with Maven
./mvnw spring-boot:run

# Or with Gradle
./gradlew bootRun
```

Then open your browser at:

```
http://localhost:8080
```

---

## Project Structure

```
simple-todo-app/
├── db/
│   └── todo.sql                          # Database dump — import this first
├── src/
│   └── main/
│       ├── java/
│       │   └── com/example/todo/
│       │       ├── TodoApplication.java
│       │       ├── controller/
│       │       │   └── TodoController.java
│       │       └── model/
│       │           └── Task.java
│       └── resources/
│           ├── application.properties    # Add your DB password here
│           └── templates/
│               └── index.html
```

---

## Routes

| Method | URL | Description |
|--------|-----|-------------|
| GET | `/` | Show all tasks |
| POST | `/` | Add a new task |
| GET | `/{id}/toggle` | Toggle task completion |
| GET | `/{id}/delete` | Delete a task |

---

## Screenshots

> Add your screenshots here.

---

## License

This project is open source and available under the [MIT License](LICENSE).
