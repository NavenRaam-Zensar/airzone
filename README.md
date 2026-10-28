# Airzone

Local learning project: React + Leaflet frontend, FastAPI + SQLite backend, OpenSky `/states/all` with OAuth2.

## Run
Backend (PowerShell):  cd backend; python -m venv venv; .\venv\Scripts\Activate.ps1; pip install -r requirements.txt; copy .env.example .env  (then edit .env); uvicorn main:app --reload
Frontend (new terminal): cd frontend; npm install; npm run dev

Open http://localhost:5173 (map) and http://127.0.0.1:8000/docs (Swagger).

## Saving OpenSky credits
Zones are 4x4 degrees (1 credit per fetch). Results are cached 60 s per zone, there is no polling,
and DAILY_CREDIT_LIMIT in backend/.env stops the backend before your daily allowance is gone.
