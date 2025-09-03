
# Smart Attendance MVP (Face + Voice + Anti-Spoofing — placeholders)

This is a **minimal working prototype**:
- FastAPI backend with enroll/verify endpoints
- Deterministic placeholder embeddings (replace with real models later)
- Simple HTML frontend for camera/mic capture

## Run (no Docker)
```bash
cd backend
python -m pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```
Then open `frontend/index.html` in a browser (served via any static server, or open directly).

## Run with Docker
```bash
docker compose up --build
```
Backend will be on `http://localhost:8000`.

## Next Steps
- Replace placeholder embeddings with **InsightFace** (face) and **ECAPA-TDNN** (voice)
- Implement real **liveness** and **voice spoof** models
- Add proper Auth (JWT) and a DB (Postgres + pgvector)
- Build a React/Next.js frontend with guided enrollment
