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

```bash
cd "/home/ubuntu/hello world"
docker compose up -d --build
```
