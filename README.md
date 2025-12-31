# Sample Flask App

A simple Flask application that demonstrates containerization, orchestration using Docker Compose, and automated CI/CD with GitHub Actions.

---

## Project Overview

This project includes:

- A Flask web application  
- Containerization using Docker  
- Orchestration with Docker Compose  
- Automated build, push, and test via GitHub Actions CI/CD  
- Proper logging and health check endpoints  

---

## Application Details

- **App Name:** Sample Flask App  
- **Container Port:** 5000  
- **Host Port:** 8082 (mapped via Docker Compose)  
- **Environment Variable:** `APP_PORT` (required to run the app)

### Endpoints

| Endpoint    | Description |
|------------|-------------|
| `/`        | Returns the app name and the port it is listening on |
| `/health`  | Returns a simple health status |

---

## Docker & Port Mapping

- The app listens on **port 5000** inside the container.  
- Docker maps **host port 8082** to container port 5000, allowing access via:

## Architecture Diagram

```mermaid
flowchart LR
  User --> Host[Host Machine]
  Host --> Docker[Docker Compose]
  Docker --> Container[Flask App Container]
  Container -->|Port 5000| App[Flask Application]

##Docker yaml


- Pros: Reviewer sees the diagram directly in GitHub without opening a separate file.  
- Cons: Limited styling compared to a full image file.

---



- Create an image (PNG/SVG) using **Draw.io** or **Excalidraw**.
- Save it in your repo, e.g., `docs/architecture.png`
- Reference it in README:

```markdown

![Architecture Diagram](docs/architecture.png)

