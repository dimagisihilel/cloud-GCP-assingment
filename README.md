# 📌 Student-Service Update – MongoDB Integration

## 🚀 New Updates
- **student-service** is now connected to **MongoDB (Docker container)**.
- Added MongoDB configuration in `application.properties`.
- MongoDB runs on **port 16000** (mapped from container’s default 27017).

---

## 🐳 Docker Setup

```bash
docker run --name mongo \
  -v mongo-data:/data/db \
  -e MONGO_INITDB_ROOT_USERNAME=root \
  -e MONGO_INITDB_ROOT_PASSWORD=mongo \
  -p 16000:27017 \
  -d mongo:latest
```

## 🔎 Explanation

`--name mongo`
Names the container mongo.

`-v mongo-data:/data/db`
Persists data in a Docker volume named mongo-data.

`-e MONGO_INITDB_ROOT_USERNAME=root`
Sets the MongoDB root username to root.

`-e MONGO_INITDB_ROOT_PASSWORD=mongo`
Sets the MongoDB root password to mongo.

`-p 16000:27017`
Maps host port 16000 → container port 27017 (default MongoDB port).

`-d`
Runs container in detached (background) mode.

`mongo:latest`
Uses the latest official MongoDB image.