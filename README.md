# flask-cicd-pipeline
End-to-End CI/CD pipeline for a Python Flask application with Docker, GitHub Actions, and automated deployment

## Architecture
1. **App**: Python Flask app with healthcheck endpoint.
2. **CI (Continuous Integration)**: GitHub Actions runs tests on every push.
3. **Build & Push**: If tests pass, Docker image is built and pushed to GitHub Container Registry (GHCR).
4. **CD (Continuous Delivery)**: `docker-compose.yml` pulls the latest image from GHCR and runs it alongside a Redis cache.

## Tech Stack
- Python 3.12 / Flask
- Pytest
- Docker / Docker Compose
- GitHub Actions
- GitHub Container Registry (GHCR)
