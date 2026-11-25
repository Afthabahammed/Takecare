# Takecare

## About the Project

Takecare is a web-based application developed using Python and Django. It is designed around healthcare-related services and provides a web interface for its application workflows.

The project uses MySQL for database storage. As part of my DevSecOps assignment, I integrated the application into an automated pipeline to practice security testing, containerization, and deployment.

## Technologies Used

- **Python** – Programming language
- **Django** – Backend web framework
- **MySQL** – Database management
- **HTML, CSS and JavaScript** – Frontend technologies
- **Git and GitHub** – Source code management
- **Semgrep** – Static Application Security Testing (SAST)
- **Trivy** – Dependency vulnerability scanning
- **OWASP ZAP** – Dynamic Application Security Testing (DAST)
- **Jenkins** – CI/CD pipeline automation
- **Docker** – Application containerization
- **Amazon ECR** – Docker image storage
- **Kubernetes (K3s)** – Container orchestration
- **Argo CD** – GitOps-based deployment management

## Running the Application Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Afthabahammed/Takecare.git
cd Takecare
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Set the required Django and MySQL configuration:

- `DJANGO_SECRET_KEY`
- `DB_NAME`
- `DB_HOST`
- `DB_USER`
- `DB_PASSWORD`
- `DB_PORT`

### 4. Apply Database Migrations

```bash
python manage.py migrate
```

### 5. Start the Development Server

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000` in your browser.

## DevSecOps Implementation

I used this application to implement and understand a complete DevSecOps workflow.

The pipeline follows these stages:

1. **Source Code Management:** The application code is maintained in GitHub.
2. **SAST:** Semgrep scans the source code for potential security issues.
3. **Dependency Scanning:** Trivy checks project dependencies for known vulnerabilities.
4. **CI/CD Automation:** Jenkins runs the pipeline stages automatically.
5. **Containerization:** Docker packages the application into a container image.
6. **Image Storage:** The image is pushed to Amazon ECR.
7. **Deployment:** Kubernetes manages the running application.
8. **GitOps:** Argo CD synchronizes deployment configurations from a Git repository.
9. **DAST:** OWASP ZAP tests the running application for potential web security issues.

## Deployment

The application is containerized using Docker and deployed to a Kubernetes cluster. Docker images are stored in Amazon ECR, while Argo CD manages the deployment through a separate GitOps repository.

## Project Goal

This project helped me gain practical experience in integrating application security testing with CI/CD automation and Kubernetes deployment. It also gave me an opportunity to work with tools commonly used in modern DevSecOps environments.
