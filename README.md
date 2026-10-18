# Azure FastAPI Demo

A minimal Python API built with FastAPI as a learning project for deploying an ASGI application to Microsoft Azure App Service.

## Endpoints

- `GET /` — returns a JSON greeting.
- `GET /health` — returns a JSON health status.

## Stack

Python, FastAPI, Uvicorn and Azure App Service.

## Run locally

Install Python and create a virtual environment:

```bash
git clone https://github.com/sivacs-tech/azure-fastapi-demo.git
cd azure-fastapi-demo
python -m venv .venv
```

Activate it and install dependencies:

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS or Linux
source .venv/bin/activate

pip install -r requirements.txt
uvicorn main:app --reload
```

Open http://127.0.0.1:8000. Interactive API documentation is available at http://127.0.0.1:8000/docs.

## Deploy to Azure App Service

1. Create or select a Python web app in Azure App Service.
2. Configure a Python runtime supported by the project.
3. Deploy the repository using your preferred GitHub Actions or Azure workflow.
4. Configure the ASGI startup command according to the selected App Service runtime.
5. Open the deployed root and `/health` routes to verify the deployment.

## Scope

This is a small deployment demo, not a production-ready service. Add automated tests, logging, monitoring, authentication and pinned dependency versions before using it as a public API. Do not commit credentials or secrets.
