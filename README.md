# Cloud Enabled Deployment In Action with AWS


👋 Hi, this is **Fahim’s submission** for the Cloud Deployment assignment.  
The project includes **four services** (3 backends + 1 frontend) with proper commit history and a short demo video.

---

## 🎬 Demo Video

👉 **Demo Video Link (Google Drive, public view):**  
[Click here to watch the demo](https://drive.google.com/file/d/1vusONuzUnYMoy9qTLsQ-3ZS_hwq414E-/view?usp=sharing)

*(Accessible to anyone with the link. Length: under 3 minutes.)*


This repository contains four projects:

- course-service (Spring Boot + MySQL)
- student-service (Spring Boot + MongoDB)
- media-service (Spring Boot + Local file storage, can be extended to S3/MinIO)
- frontend-app (React + TypeScript)

## Backend Services

### 1. course-service
- Entity: Course(id, name, duration)
- Endpoints:
  - GET /courses
  - GET /courses/{id}
  - POST /courses
  - DELETE /courses/{id}
- Default port: 8081
- Configure MySQL settings

### 2. student-service
- Document: Student(registrationNumber, fullName, address, contact, email)
- Endpoints:
  - GET /students
  - GET /students/{id}
  - POST /students
  - DELETE /students/{id}
- Default port: 8082
- Configure MongoDB settings

### 3. media-service
- Resource: files
- Endpoints:
  - POST /files (multipart/form-data: file)
  - GET /files (list)
  - GET /files/{id} (fetch)
  - DELETE /files/{id} (delete)
- Default port: 8083
- Uses local disk storage at `./data/media` by default (override with env var `MEDIA_STORAGE_DIR`).

## Frontend (frontend-app)
- React + TypeScript + MUI + Axios + Vite app with 3 sections: Courses, Students, Media
- Scripts:
  - npm run dev (Vite dev server)
  - npm run build (TypeScript build + Vite build)
  - npm run preview (Preview built app)

## Build

- Backend: run `mvn -q -e -DskipTests package` at repo root to build services.
- Frontend: run `npm install` then `npm run dev` inside `frontend-app`.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
Copyright (c) 2025 Fahim 
Licensed under MIT License
```

---

##  What I Learned

Through this project, I gained hands-on experience with:

- **Microservices Architecture:** Building independent, scalable services
- **Spring Boot Development:** Creating REST APIs with different databases
- **React & TypeScript:** Modern frontend development practices
- **AWS Cloud Services:** RDS, EC2, S3, DocumentDB deployment
- **DevOps Practices:** Docker containerization, CI/CD pipelines
- **Database Integration:** Working with both SQL and NoSQL databases
- **API Design:** RESTful services with proper HTTP methods
- **Error Handling:** Comprehensive error management and logging

---

##  Future Enhancements

- [ ] Implement JWT authentication
- [ ] Add API rate limiting
- [ ] Set up monitoring with CloudWatch
- [ ] Add automated testing pipeline
- [ ] Implement caching with Redis
- [ ] Add API documentation with Swagger
- [ ] Set up log aggregation
- [ ] Implement service discovery

---

## 📞 Contact

**Mohammed Fahim**  
📧 Email: fahim1998108@gmail.com  
🐙 GitHub: [@fahim](https://github.com/fahimHexClan)  
🎓 Student ID: 2301671032

---

**Thank you for reviewing my project! 🙏**

*Submitted: [15-09-2025] | Course: Cloud Computing | Assignment: Practical Deployment*