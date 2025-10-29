# Qdrant
1. Installation requirements
   - Đọc kỹ tại đây: **[Click me](https://qdrant.tech/documentation/guides/installation/#installation-requirements)**
2. Docker Compose
   ```
   services:
     qdrant:
       image: qdrant/qdrant:latest
       restart: always
       container_name: qdrant
       ports:
         - 6333:6333
         - 6334:6334
       environment:
         QDRANT_SERVICE__GRPC_PORT: 6334
       volumes:
         - ./qdrant_data:/qdrant/storage
   ```
3. Lưu ý:
    - Check Firewall local port: 6333, 6334