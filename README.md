# GPT-2 FastAPI Text Generator

A lightweight FastAPI application that loads the Hugging Face GPT-2 model and exposes a simple text-generation API. The app is containerized with Docker and published to GitHub Container Registry (GHCR) for quick deployment and local use.

## Suggested repository name

`gpt2-fastapi-ghcr`

This name better reflects the actual project purpose:
- GPT-2 model
- FastAPI service
- GitHub Container Registry deployment

## Features

- FastAPI server with a minimal web UI
- GPT-2 text generation endpoint
- Dockerized deployment
- GHCR image publishing

## API

### Root endpoint

GET `/`

Returns a simple HTML page describing the service.

### Text generation endpoint

POST `/generate`

Request body:

```json
{
  "text": "Once upon a time"
}
```

Response:

```json
{
  "generated_text": "Once upon a time, in a faraway land..."
}
```

## Run locally

```bash
pip install -r requirements.txt
python main.py
```

Then open:

```text
http://localhost:8000
```

## Pull the container from GHCR

```bash
docker pull ghcr.io/muhammadyousafrana/gpt2-fastapi-ghcr:latest
```

## Example Docker run

```bash
docker run -p 8000:80 ghcr.io/muhammadyousafrana/gpt2-fastapi-ghcr:latest
```

## Project structure

```text
.
├── Dockerfile
├── main.py
├── requirements.txt
├── README.md
└── LICENSE
```

## License

This project is licensed under the Creative Commons Zero v1.0 Universal License.
