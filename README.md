# IBM SkillsBuild Progress Tracker

A full-stack web application for tracking learning progress across IBM SkillsBuild courses. Users can manage courses, record completion progress, earn achievement badges, build learning streaks, compare leaderboard positions and connect with friends.

## Features

- Account registration and secure login
- BCrypt password hashing and Spring Security authentication
- Course search, enrolment and progress tracking
- Points, learning streaks and achievement badges
- Friends, friend requests and user search
- Leaderboard and customisable profile borders
- Profile-picture upload and account management

## Technology

- Java 21
- Spring Boot 3.4
- Spring MVC and Thymeleaf
- Spring Security
- Spring Data JPA and Hibernate
- MySQL
- Gradle
- JUnit 5, Mockito and Spring Security Test

## Running locally

### Prerequisites

- Java Development Kit 21
- MySQL 8 or later

### Setup

1. Clone the repository and enter the project directory:

   ```bash
   cd IBM-Skillsbuild-Tracker-Website
   ```

2. Create the local database:

   ```sql
   CREATE DATABASE group34;
   ```

3. Configure the database using environment variables:

   | Variable | Example |
   | --- | --- |
   | `DB_URL` | `jdbc:mysql://localhost:3306/group34` |
   | `DB_USERNAME` | `root` |
   | `DB_PASSWORD` | Your local MySQL password |

   Alternatively, create `src/main/resources/application-local.properties`. This file is ignored by Git:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/group34
   spring.datasource.username=root
   spring.datasource.password=your-password
   ```

4. Start the application:

   macOS/Linux:

   ```bash
   ./gradlew bootRun
   ```

   Windows:

   ```powershell
   .\gradlew.bat bootRun
   ```

5. Open `http://localhost:8080` in a browser.

Hibernate creates and updates the required tables on startup. Initial achievement-badge records are added automatically when the database is empty.

## Tests

Run the automated test suite with:

```bash
./gradlew test
```

On Windows, use `gradlew.bat test`.

## Project context

This application was developed as a University of Leicester Agile group project. I served as the team's Scrum Master while also contributing to the delivery of the application. The repository is retained as a portfolio example of our work with Java, Spring Boot, relational data, authentication and collaborative software development.

The included `User_Manuals.docx` contains further guidance on using the application.

## Disclaimer

This is an educational project and is not an official IBM product. IBM and IBM SkillsBuild are trademarks of IBM Corporation.
