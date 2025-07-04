
vProfile – Dockerized Setup

This is a Dockerized version of the vProfile web application, which is a multi-tier Java app using technologies like Spring MVC, MySQL, RabbitMQ, and Memcached.

📌 Note

The original vProfile application was created by hkhcoder and other contributors. 
I've only worked on writing the Dockerfiles and the docker-compose.yml to containerize the application for local setup and testing.

This was part of my DevOps learning and practice.

🛠 Technologies Used

- Java, Spring MVC, JSP
- Spring Security, Spring Data JPA
- Apache Tomcat
- MySQL
- RabbitMQ
- Memcached
- ElasticSearch
- Docker & Docker Compose
- Maven

✅ Prerequisites

Make sure you have the following installed:

- JDK 17 or 21  
- Maven 3.9+  
- Docker and Docker Compose  
- MySQL 8 (if not using the containerized DB)

🗃️ Database Setup

You can find the MySQL dump file at:

/src/main/resources/db_backup.sql

To import the database:

mysql -u <your_username> -p accounts < db_backup.sql

Alternatively, if you're running the MySQL container through Docker Compose, the database will be auto-initialized.

🚀 How to Run with Docker Compose

1. Clone the repo:

git clone https://github.com/sahjebkhan/vprofile-docker.git
cd vprofile-docker

2. Run the containers:

docker-compose up --build

3. Once up, the application should be accessible at:

http://localhost

📂 Project Structure

.
├── Docker-files/
│   ├── app/        -> Dockerfile for Tomcat App
│   ├── db/         -> Dockerfile for MySQL
│   └── web/        -> Dockerfile for Web Frontend
├── docker-compose.yml
├── Jenkinsfile
├── pom.xml
└── README.md

✍️ Author

Sahjeb Khan  
I'm learning DevOps and using this project to practice containerization using Docker.

- GitHub: @sahjebkhan
- LinkedIn: thesahjebkhan

🙏 Credits

Thanks again to hkhcoder for the original project codebase.
