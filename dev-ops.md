# Docker stages

DEV:
  - prepatativo:
    - npm install
    - npm run db:migrate

  - execução:
    - npm dev

PRD:
  - prepatativo:
    - npm install
    - npm run db:migrate
    - npm run build
    - npm prune --prod

  - execucao:
    - npm run start

---

# comandos Docker
```sh
podman build -t passin:v1 .

podman run -p 3001:3333 passin:v1

podman run -p 3001:3333 -d passin:v1
```

# comandos Docker Compose
```sh
podman-compose up --build -d

podman-compose down

podman-compose up -d
```