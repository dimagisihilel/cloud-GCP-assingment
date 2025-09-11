
# ☁️ Cloud Deployment - Integrating with GCP

This assignment outlines the steps to connect **course-service** Spring Boot application to a MySQL database hosted on Google Cloud Platform (GCP).

Here is the screen recording of the project's demonstration.

### ▶️ **[Click Here to Watch the Video Demonstration](https://drive.google.com/file/d/your-google-drive-file-id/view?usp=sharing)**

---

## 📂 Project Structure

- `course-service` (Spring Boot + MySQL)
- `student-service` (Spring Boot + MongoDB)
- `media-service` (Spring Boot + Local file storage, can be extended to S3/MinIO)
- `frontend-app` (React + TypeScript)

---

## 📋 Prerequisites

Before setting up the `course-service`, ensure you have:

- **GCP Account**: A Google Cloud Platform account with a project created.
- **MySQL Instance**: A Cloud SQL MySQL instance set up in GCP.

---

## 🚀 Steps to Set Up course-service with GCP MySQL

### 1. Clone the Repository
Clone the repository to your local machine:

```bash
git clone https://github.com/dimagisihilel/cloud-GCP-assingment
```

### 2. Create a Cloud SQL Instance
Set up a MySQL database instance on GCP Cloud SQL for the course-service.

### 3. Authorize Network Access
Allow your application’s IP to connect to the GCP MySQL instance.

### 4. Configure application-gcp.properties
Define MySQL connection details in application-gcp.properties for course-service.

```bash
spring.application.name=course-service

# GCP MySQL Configurations
spring.datasource.host= {YOUR IP}
spring.datasource.port=3306
spring.datasource.url=jdbc:mysql://${spring.datasource.host}:${spring.datasource.port}/eca_courses?createDatabaseIfNotExist=true
spring.datasource.username=root
spring.datasource.password=  {YOUR PASSWORD}
```

### 5. Change Active Profile to GCP
Activate the gcp profile to load the GCP MySQL configuration.

```bash
spring.profiles.active= {gcp}
```

### 6. Run the Frontend and Backend
Start the course-service backend and frontend-app to enable interaction.

### 7. Add Courses from Frontend and Check
Add courses via the frontend and verify storage in the `eca_courses` database.

---

## 📜 License

This project is licensed under the [MIT License](https://drive.google.com/file/d/your-google-drive-file-id/view?usp=sharing). See the LICENSE.md file for details.

---

## 📚 Additional Google Cloud Resources

[Google cloud documentation](https://cloud.google.com/docs)

[Cloud SQL for MySQL ](https://cloud.google.com/sql/docs/mysql)

[Connect using a MySQL client](https://cloud.google.com/sql/docs/mysql/connect-admin-ip)