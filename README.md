Sentinel Upload API

Minimal FastAPI app for secure file upload handling.

Docs index

- PLAN.md
- SECURITY.md
- GITHUB-BEST-PRACTICE.md
- docs/architecture.md
- docs/shared-responsibility.md
- sre/sli-slo.md
- runbooks/upload-api-unavailable.md
- sre/postmortem-template.md

Run locally (Docker)

```powershell
docker build -f docker/Dockerfile -t sentinel-upload-api:dev .
docker run --rm -p 8000:8000 sentinel-upload-api:dev
```

Health check

```powershell
curl http://localhost:8000/health
```

Upload (PowerShell)

```powershell
curl -F "file=@README.md;type=text/markdown" http://localhost:8000/upload
```

Expected response

Optional: Run locally (venv)

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r app/requirements.txt
uvicorn app.main:app --reload
```

```json
{"filename":"README.md","content_type":"text/markdown","status":"accepted"}
```
