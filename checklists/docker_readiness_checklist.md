# Docker Readiness Checklist

## Dockerfile

- [x] Co base image hop ly.
- [x] Co `WORKDIR`.
- [x] Co copy dependency truoc source de tan dung cache.
- [x] Co `EXPOSE`.
- [x] Co `CMD` hoac `ENTRYPOINT`.
- [x] Co `HEALTHCHECK`.
- [x] Co user non-root.
- [x] Khong chua secret that.

## Runtime

- [x] Container chay duoc.
- [x] Port map dung.
- [x] `/health` tra `200`.
- [x] Log khoi dong ro rang.
- [x] Cau hinh qua ENV.

## Testing

- [x] Chay lai Postman Collection tu Lab 03/Lab 04.
- [x] Newman report sinh ra trong `reports/`.
- [x] Functional test pass.
- [x] Auth test pass tren local/container.
- [x] Negative test pass tren local/container.
- [x] Boundary test pass hoac co giai thich hop dong.

## Evidence

- [x] Co anh/log `docker build`.
- [x] Co anh/log `docker run`.
- [x] Co anh/log `curl /health`.
- [x] Co Newman HTML/XML report.
- [x] Co tag image dung quy uoc.
