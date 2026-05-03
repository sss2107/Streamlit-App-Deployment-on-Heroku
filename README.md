# Streamlit App Deployment on Heroku

A banknote authentication machine learning demo served through Streamlit, with supporting Flask API examples and Heroku deployment files. The model predicts whether a banknote is authentic based on numeric image-derived features.

## What This Project Shows

- Training a banknote authentication classifier
- Loading a serialized `classifier.pkl` model
- Building a Streamlit prediction UI
- Serving a Flask prediction API with Swagger-style docstrings
- Packaging a small ML app for Heroku-style deployment

## Tech Stack

- Python
- Streamlit
- Flask
- scikit-learn
- pandas
- Docker
- Heroku `Procfile`

## Repository Structure

```text
.
├── app.py                  # Streamlit prediction app
├── flask_api.py            # Flask API variant
├── ModelTraining.ipynb     # Model training notebook
├── classifier.pkl          # Serialized classifier
├── BankNote_Authentication.csv
├── TestFile.csv
├── Dockerfile
├── Procfile
├── setup.sh
└── requirements.txt
```

## Run Locally

```bash
git clone https://github.com/sss2107/Streamlit-App-Deployment-on-Heroku.git
cd Streamlit-App-Deployment-on-Heroku
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

## Flask API Variant

To run the Flask API example:

```bash
python flask_api.py
```

The API exposes:

- `GET /`
- `GET /predict`
- `POST /predict_file`

## Deployment Notes

The repository includes Heroku-oriented files (`Procfile`, `setup.sh`) and a `Dockerfile`. Heroku's free tier has changed since this demo was originally created, so you may need to adapt deployment to a current platform such as Render, Railway, Fly.io, AWS App Runner, or a container service.

## License

This project is licensed under the terms in [LICENSE](LICENSE).
