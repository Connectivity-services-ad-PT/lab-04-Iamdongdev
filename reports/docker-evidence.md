# Docker Evidence - Lab 04

## Team

- Team name: team-iot
- Service: iot-ingestion
- Image tags:
  - `fit4110/iot-ingestion:lab04`
  - `fit4110/iot-ingestion:v0.1.0-team-iot`

## 1. Build Evidence

Command:

```bash
docker build -t fit4110/iot-ingestion:lab04 .
```

Result:

```text
Build completed successfully.
Image: fit4110/iot-ingestion:lab04
Image ID: 40ee63027758
Size: 268MB
```

## 2. Run Evidence

Command:

```powershell
docker run -d --rm --name fit4110-iot-lab04 -p 8000:8000 --env-file .env.example fit4110/iot-ingestion:lab04
```

Result:

```text
Container started successfully.
Container name: fit4110-iot-lab04
Port mapping: 0.0.0.0:8000->8000/tcp
Docker health status: healthy
```

## 3. Healthcheck Evidence

Command:

```bash
curl http://localhost:8000/health
```

Result:

```json
{"status":"ok","service":"iot-ingestion","version":"0.4.0"}
```

## 4. Newman Evidence

Command:

```bash
npm run test:local
```

Result:

```text
Collection: FIT4110 Lab04 IoT Docker Verification
Requests executed: 11
Assertions executed: 19
Failures: 0
Average response time: 22ms
```

Report paths:

```text
reports/newman-lab04-local.xml
reports/newman-lab04-local.html
```

## 5. Contract Lint Evidence

Command:

```bash
npm run lint:openapi
```

Result:

```text
No results with a severity of 'error' found.
```

## 6. Notes

- The container runs as non-root user `appuser`.
- Runtime configuration is loaded from `.env.example`.
- Dockerfile includes `HEALTHCHECK` against `GET /health`.
- Known limitation: this Lab 04 version uses in-memory readings only; persistent storage and multi-service composition are planned for Lab 05.
