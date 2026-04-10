# Hello World Website

This website was created in `/home/ubuntu/hello world`.

## What Was Used

- Frontend language: JavaScript
- Frontend structure: HTML + CSS + JavaScript
- Backend language: Python
- Backend framework: Flask
- Python virtual environment: `.venv`
- Service port: `13333`

## Project Files

- `app.py`: Flask application entry
- `templates/index.html`: homepage template
- `static/styles.css`: page styles
- `static/app.js`: frontend JavaScript
- `requirements.txt`: Python dependencies
- `Dockerfile`: image build definition
- `docker-compose.yml`: pull-and-run compose file for published image

## Run

### Python

```bash
cd "/home/ubuntu/hello world"
source .venv/bin/activate
python app.py
```

Then open:

```bash
http://127.0.0.1:13333
```

### Docker

Build the image:

```bash
cd "/home/ubuntu/hello world"
docker build -t hw .
```

Run the container:

```bash
docker run -d --name hw -p 13333:13333 hw
```

### Docker Compose

Pull the published image:

```bash
cd "/home/ubuntu/hello world"
docker compose pull
docker compose up -d
```

Published image:

```bash
ghcr.io/ryzechen88/hw:latest
```

### 1Panel

In 1Panel Compose, you can use:

```yaml
services:
  hw:
    image: ghcr.io/ryzechen88/hw:latest
    container_name: hw
    ports:
      - "13333:13333"
    restart: unless-stopped
```

### Publish Image

This repository includes a GitHub Actions workflow that publishes the Docker image to GHCR when you push to `main`.
