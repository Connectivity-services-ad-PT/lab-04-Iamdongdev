# TEAM_TASKS.md - Viec can lam theo nhom

Moi nhom bat dau tu repo mau nay va thay phan IoT bang service cua minh.

---

## Viec chung cho moi nhom

- [x] Copy contract tu Lab 03 vao thu muc `contracts/`.
- [x] Dam bao service co `GET /health`.
- [x] Viet hoac cap nhat `Dockerfile`.
- [x] Viet `.dockerignore`.
- [x] Viet `.env.example`.
- [x] Viet `RUN_LOCAL.md`.
- [x] Build image.
- [x] Run container.
- [x] Chay Postman Collection tu Lab 03/Lab 04 tren container.
- [x] Xuat Newman report.
- [x] Ghi bang chung `/health` va log container trong `reports/docker-evidence.md`.
- [x] Ghi tag image: `fit4110/iot-ingestion:v0.1.0-team-iot`.

---

## Goi y theo service

| Service | Diem can chu y |
|---|---|
| IoT Ingestion | API nhan telemetry, auth token, `/health`, test boundary nhiet do |
| Camera Stream | Dung `opencv-python-headless`, chuan bi 1 anh mau, chua can RTSP that |
| Access Gate | Neu chua co DB trong Lab 04, dung in-memory hoac DB ngoai; Compose de Buoi 5 |
| AI Vision | Co the dung mock model hoac YOLOv8n nho; kiem soat dung luong image |
| Analytics | Nhan event JSON gia; TimescaleDB de Buoi 5 |
| Core Business | Policy evaluation chay bang config/env |
| Notification | Channel mock la du; khong commit Telegram/email token that |
