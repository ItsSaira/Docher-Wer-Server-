# 🐳 Docker Web Server — Control Center

Interactive CodeAlpha internship project demonstrating a real web server running inside Docker.

## Features
- Live dashboard backed by Express APIs
- Health endpoint `/health`
- Dockerfile `HEALTHCHECK`
- Healthy → Unhealthy → Healthy demonstration
- Runtime, memory, CPU, hostname and request metrics
- Live application logs
- Connectivity test
- Copyable lifecycle commands
- Troubleshooting section
- Docker Compose
- Alpine-based image
- Non-root `node` user
- Restart policy

## Run
Start Docker Desktop, then in PowerShell/CMD/VS Code terminal:

```powershell
docker compose up -d --build
```

Open `http://localhost:3000`.

## Demonstrate health monitoring
Click **Simulate health failure**. `/health` returns HTTP 503 and the Docker healthcheck will begin failing. Click **Restore health** to recover.

Check status with:

```powershell
docker compose ps
```

## Lifecycle
```powershell
docker compose up -d --build
docker compose ps
docker compose logs -f web
docker compose restart
docker compose stop
docker compose start
docker compose down
docker stats docker-web-server-pro
docker inspect docker-web-server-pro
```

## Where commands run
Commands are run in **Windows PowerShell, Command Prompt, or VS Code terminal**. The webpage intentionally does not get unrestricted access to the host Docker engine; its buttons copy safe commands for you.

## Structure
```text
docker-web-server-pro/
├── public/index.html
├── server.js
├── package.json
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
├── .gitignore
└── README.md
```

## GitHub
```powershell
git init
git add .
git commit -m "Build interactive Docker web server"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```
