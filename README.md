# Task 4: Web Server Containerization using Docker

This repository contains the architecture, configuration steps, and static assets used to deploy a containerized Nginx web server. The project demonstrates container lifecycle management, cross-platform port bindings, and stateless storage mapping via volume mounts.

## 📊 Project Objectives & Solutions Covered

*   **Task 1: Containerization Basics** ── Pulled and validated isolated system blueprints utilizing the lightweight `nginx:alpine` image distribution.
*   **Task 2 & 5: Stateless Server Deployment** ── Avoided container configuration mutation by implementing a live local volume mount (`-v`), anchoring host assets directly to the container runtime path.
*   **Task 3: Lifecycle Mastery** ── Practiced isolated state operations handling active initialization, background execution tracking (`-d`), and cluster teardowns.
*   **Task 4: Systems Troubleshooting** ── Actively debugged and resolved host networking port resource blockages (`Port 8080 already allocated`) and daemon naming registry conflicts.

---

## 🛠️ Technology Stack & Requirements

*   **Container Platform Engine:** Docker Desktop for Windows
*   **Base Layer Image Node:** Nginx (Alpine Linux distribution tag)
*   **Runtime Network Configuration:** Port Mapping `8080:80`
*   **Storage Infrastructure Architecture:** Dynamic Host-to-Container Bind Mounts

---

## 📦 File Architecture

```text
├── index.html          # Custom webpage template injected into the web server
└── README.md           # Professional system architecture documentation
```

---

## 🚀 How to Deploy This Infrastructure Instantly

To spin up this identical, cross-platform web server environment on any machine equipped with Docker:

1. **Clone this repository:**
   ```bash
   git clone https://github.com
   cd my-docker-web-server
   ```

2. **Execute the Isolated Container Launcher:**
   Run the following deployment command inside your terminal (ensure you change the host path segment to match your local repository directory structure):
   ```bash
   docker run --name alpha-custom-server -d -p 8080:80 -v C:\Users\DELL\my-docker-web:/usr/share/nginx/html nginx:alpine
   ```

3. **Verify Health Validation:**
   Open your browser interface and map traffic queries to **`http://localhost:8080`**.
