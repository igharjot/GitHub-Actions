# GitHub-Actions

A comprehensive collection of GitHub Actions workflows demonstrating CI/CD, DevSecOps, and automated deployment patterns. This repository serves as a practical guide for implementing modern automation workflows using GitHub's native automation platform.

## 🚀 Overview

This repository contains a Flask-based web application and a variety of GitHub Actions workflows designed to showcase different automation scenarios, including:
- **Continuous Integration (CI)**: Automated testing and code quality checks.
- **Continuous Deployment (CD)**: Automated deployment to servers and cloud platforms.
- **DevSecOps**: Security scanning, dependency checks, and image vulnerability analysis.
- **Docker Integration**: Building, linting, and pushing Docker images to registries.

## 📂 Project Structure

| File/Directory | Description |
| :--- | :--- |
| `app.py` | Core Flask application script. |
| `Dockerfile` | Configuration for containerizing the Flask application. |
| `docker-compose.yml` | Multi-container orchestration setup. |
| `templates/` | HTML templates for the web interface. |
| `.github/workflows/` | The heart of the repository, containing all YAML workflow definitions. |

## 🛠️ Workflows Breakdown

The following workflows are included in the `.github/workflows/` directory:

### CI/CD & Deployment
- **`cicd.yml`**: Standard Continuous Integration and Deployment pipeline.
- **`deploy-to-server.yml`**: Automated deployment to a remote server.
- **`portfolio-deploy.yml`**: Specific workflow for deploying a portfolio site.

### Security & Quality
- **`code-quality.yml`**: Runs linters and static analysis to ensure code standards.
- **`devsecops-pipeline.yml`**: An integrated pipeline focusing on security at every stage.
- **`dependency-scan.yml`**: Scans project dependencies for known vulnerabilities.
- **`image-scan.yml`**: Performs security scanning on built Docker images.
- **`secrets-scan.yml`**: Checks for accidentally committed secrets or API keys.

### Docker & Containerization
- **`docker-app.yml`**: Main workflow for Docker-related operations.
- **`docker-build-push.yml`**: Builds Docker images and pushes them to a registry (e.g., Docker Hub).
- **`docker-lint.yml`**: Lints the Dockerfile to follow best practices.

### Advanced Patterns
- **`python-matrix.yml`**: Demonstrates testing against multiple Python versions using a build matrix.
- **`hello.yml`**: A simple "Hello World" workflow to test action triggers.

## 🚦 Getting Started

### Prerequisites
- Python 3.x
- Docker and Docker Compose (optional, for containerized execution)
- GitHub account with Actions enabled

### Local Development
1. Clone the repository:
   ```bash
   git clone https://github.com/igharjot/GitHub-Actions.git
   cd GitHub-Actions
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   python app.py
   ```

## 🔧 Configuration

To use the deployment workflows, you will need to configure the following **GitHub Secrets** in your repository settings:
- `DOCKER_USERNAME`: Your Docker Hub username.
- `DOCKER_PASSWORD`: Your Docker Hub password/token.
- `SERVER_IP`: The IP address of your deployment server.
- `SERVER_SSH_KEY`: Private SSH key for server access.

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
