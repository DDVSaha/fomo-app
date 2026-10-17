# FOMO / Reverse Calendar

Full-stack hackathon prototype: a Flask-RESTX scheduling API plus a React + TypeScript
front end (the FOMO design).

```text
backend/    Flask-RESTX API (schedule, opportunities, users) + deterministic scheduler
frontend/   Vite + React + TypeScript app
openapi.yml API contract
```

## Run (development, two terminals)

```bash
pip install -r requirements.txt
python -m backend.app            # API on http://localhost:8000 (Swagger: /api/v1/swagger)

cd frontend && npm install && npm run dev   # UI on http://localhost:5173 (proxies /api to :8000)
```

## Run (single server)

```bash
cd frontend && npm install && npm run build && cd ..
python -m backend.app            # UI + API on http://localhost:8000
```

## Tests

```bash
python -m unittest discover -s tests -t .
```
