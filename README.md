# Template ML Engineering
This is my personal template for my Machine learning Engineering projects.
## Goal
My goal with it is to have a reproducible architecture for my futur Machine learning projects.
## Organization
Organized as follow : 
```
template_mle/
|--- backend/               # Contains the business logic
|   --- api/                # FastAPI inference service
|   --- data/               # Data for Data Analysis & experimentation and Pre-prod training
|   --- exploration/        # Exploratory Data Analysis & experimentation notebooks
|   --- model               # Contains the model artefact
|   --- src/                # Python Scripts
|      --- ingestion.py     # Extract data from multiple sources in raw Parquet format for exploratory data analysis (EDA).
|      --- processing.py    # Prepare the Final Parquet for the pre-prod training
|      --- train.py         # Prepare a Model artifact ready for production
|--- frontend/              # Minimal UI with vuejs for testing predictions
```
## Requirements
- **Python 3.12+**
- **uv** : Package manager for Python. ([Install uv](https://docs.astral.sh/uv/getting-started/installation/))
- **Node.js (^20.19.0 || >=22.12.0)** & **npm** : For the frontend Vue.js.

## How to use it ?
- Create a new repo based on this template
- Clone the new repo and configure:
```bash
# Clone the new repo
git clone <repo-url>
cd <project-name>

# Backend configuration
cd backend
uv sync # create .venv and install all the dependencies

# Frontend configuration
cd ../frontend
npm install
```
- Exploration data and coding the backend : navigate to the `/backend` folder in the terminal.
    - EDA : ``uv run jupyter notebook`` to run the jupyter notebook server
    - Coding in fastapi: ``uv run uvicorn api.main:app --reload``
- Code the frontend part navigate to the `/frontend` folder in the terminal.
    - ``npm run dev``
