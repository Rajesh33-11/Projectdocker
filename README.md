# AWS 3-Tier App (Dockerized)

Frontend (nginx) + Backend (Node.js) + Database (MySQL), anni Docker Compose tho run avutayi.

## Structure
```
aws-3tier-app/
├── frontend/        # Dockerfile, nginx.conf
├── backend/         # Dockerfile
├── database/        # init.sql
├── docker-compose.yml
└── .env.example
```

## Run cheyyadam
```bash
cp .env.example .env        # passwords marchukondi
docker compose up --build -d
```
App: http://localhost

## Useful commands
```bash
docker compose ps              # running containers
docker compose logs -f backend # backend logs
docker compose down            # stop
docker compose down -v         # stop + DB data delete
```

## Note
- Backend lo DB host = `db`, port = `3306`, env variables nunchi teesukovali.
- Frontend nunchi API calls `/api/...` ki cheyyali (nginx backend ki proxy chestundi).
