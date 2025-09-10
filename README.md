# Cloud Assignment with GCP

## Project Structure

- **course-service** (Spring Boot + MySQL)
  - Port: 8081
  - CRUD for Courses (id, name, duration)

- **student-service** (Spring Boot + MongoDB)
  - Port: 8082
  - CRUD for Students (registrationNumber, fullName, address, contact, email)

- **media-service** (Spring Boot + Local storage / S3-ready)
  - Port: 8083
  - File upload, fetch, list, delete (`./data/media` by default)

- **frontend-app** (React + TypeScript + MUI + Vite)
  - Sections: Courses, Students, Media
  - Scripts: `npm run dev`, `npm run build`, `npm run preview`  
