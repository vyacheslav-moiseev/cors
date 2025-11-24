# CORS nginx — test assignment
Запускает nginx в Docker с CORS (whitelist через map).
## Запуск
1. Собрать образ и запустить контейнер:
```bash
docker-compose up -d --build

### Пример проверки CORS

**Request**
```bash
curl -H "Origin: https://leads.su" -I http://localhost:8080

Response

HTTP/1.1 200 OK
Server: nginx/1.29.3
Date: Mon, 24 Nov 2025 13:38:18 GMT
Content-Type: text/plain
Content-Length: 8
Connection: keep-alive
Access-Control-Allow-Origin: https://leads.su
Access-Control-Allow-Headers: Authorization, Content-Type, X-Requested-With
Access-Control-Allow-Methods: GET, POST, OPTIONS, PUT, DELETE
Access-Control-Allow-Credentials: true