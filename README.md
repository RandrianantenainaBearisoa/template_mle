# Template ML Engineering
This is my personal template for my Machine learning Engineering projects.
## Goal
My goal with it is to have a reproducible architecture for my futur Machine learning projects.
## Organization
Organized as follow : 
```
template_mle/
|--- backend/               # Contains the notebooks,the data and the api
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
