# 📌 Course-Service Update – MySQL Integration

## 🚀 New Updates
- **course-service** is now connected to **MySQL (Docker container)**.
- Added database configuration in `application.properties`.
- MySQL runs on **port 15000** (mapped from container’s default 3306).

---

## 🐳 Docker Setup

```bash
docker run --name mysql \
  -v mysql-data:/var/lib/mysql \
  -e MYSQL_ROOT_PASSWORD=mysql \
  -p 15000:3306 \
  -d mysql:lts
```

## 🔎 Explanation

- `-- name mysql`   → Names the container mysql.

- `-v mysql-data:/var/lib/mysql`   → Persists data in a Docker volume named mysql-data.

- `-e MYSQL_ROOT_PASSWORD=mysql`   → Sets MySQL root password to mysql.

- `-p 15000:3306`   → Maps host port 15000 -> container port 3306.

- `-d`  → Runs container in detached (background) mode.

- `mysql:lts`  → Uses the MySQL LTS image.