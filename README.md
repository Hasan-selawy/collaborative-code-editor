# Collaborative Code Editor

A full-stack code-editor project with a Java/Spring Boot backend and an Angular/TypeScript frontend. The repository includes WebSocket support, authentication dependencies, Monaco Editor integration, and a Docker Compose development setup.

## Technology

| Component | Stack |
| --- | --- |
| Backend | Java 17, Spring Boot 3.3.4, Spring Data JPA |
| Frontend | Angular 18, TypeScript, Monaco Editor |
| Authentication | Spring Security, JWT, OAuth2 dependencies |
| Real-time communication | Spring WebSocket |
| Local database | MariaDB in Docker Compose |
| Development environment | Docker Compose |

## Repository layout

- `editor/`: Spring Boot backend and Maven build.
- `code-editor/`: Angular frontend.
- `db/`: SQL initialization files.
- `docker-compose.yml`: local service configuration.
- [Final project report](FinalProjectReport.pdf): additional project documentation.

## Local development

Install Git, Docker, and Docker Compose, then run:

```bash
git clone https://github.com/Hasan-selawy/collaborative-code-editor.git
cd collaborative-code-editor
docker compose up --build
```

The Compose configuration publishes the frontend on http://localhost:4200 and the backend on port 8002. First startup initializes MariaDB and waits for its health check.

This is the setup declared by the repository; it has not been runtime-tested as part of this documentation update.

## Deployment considerations

The current Compose file contains development database credentials and mounts the host Docker socket into the backend. Review credentials, execution isolation, network exposure, and authentication configuration before deploying to a shared or public environment.

## Author

[Hasan Masoud](https://github.com/Hasan-selawy) · Backend developer based in Amman, Jordan.
