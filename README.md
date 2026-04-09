
# 🍰 Blush Bakery Website (Dockerized)

A beautiful, aesthetic bakery website built using **HTML & CSS** and containerized using **Docker with Nginx**.
This project is perfect for beginners learning **Docker, static website hosting, and DevOps basics**.

---

## ✨ Features

* 🎨 Elegant blush themed UI
* 🍰 Menu sections: Cakes, Pastries, Cookies, Coffee
* 📱 Fully responsive design
* ⚡ Lightweight and fast (served via Nginx)
* 🐳 Dockerized for easy deployment

---

## 📂 Project Structure

```
.
├── index.html
├── Dockerfile
└── README.md
```

---

## 🐳 Docker Setup

### 1. Build Docker Image

```bash
docker build -t blush-bakery .
```

### 2. Run Docker Container

```bash
docker run -d -p 8080:80 blush-bakery
```

### 3. Access the Website

Open your browser and go to:

```
http://localhost:8080
```

---

## 📦 Dockerfile Explanation

```dockerfile
FROM nginx:alpine
```

* Uses lightweight Nginx image

```dockerfile
RUN rm -rf /usr/share/nginx/html/*
```

* Removes default Nginx files

```dockerfile
COPY . /usr/share/nginx/html
```

* Copies your website files into Nginx directory

```dockerfile
EXPOSE 80
```

* Exposes port 80 inside container

```dockerfile
CMD ["nginx", "-g", "daemon off;"]
```

* Starts Nginx server

---

## 🌐 Deployment Idea (For Students / Workshop)

Students can:

1. Fork your GitHub repo
2. Clone their fork
3. Modify `index.html` (customize bakery items 💡)
4. Build Docker image
5. Run locally or deploy on AWS EC2

---

## 🚀 Future Enhancements

* Add CI/CD using GitHub Actions
* Deploy on AWS EC2 / ECS / S3
* Add backend (Node.js / API)
* Add payment integration

---

## 💖 About the Project

This project demonstrates how a simple static website like your bakery page  can be:

* Containerized
* Easily deployed
* Scaled using cloud platforms

---

## 👩‍💻 Author

**Varsha Verma**
Senior Cloud Engineer | DevOps Enthusiast | Speaker

