# Quick Start
```bash
git clone https://github.com/BSlience/dl-deploy.git
```

[install pipenv](https://pipenv.pypa.io/en/latest/)

[install httpie](https://github.com/httpie/httpie)

```bash 
cd dl-deploy
pipenv install
python bin/download_model
uvicorn sentiment_analyzer.api:app
```
```bash
# other console
http POST http://localhost:8000/predict text="OMG. I love how easy it is to stick to my schedule. Would recommend to everyone"```
```json
{
    "confidence": 0.999885082244873,
    "probabilities": {
        "negative": 0.999885082244873,
        "neutral": 8.876612992025912e-05,
        "positive": 2.614063305372838e-05
    },
    "sentiment": "negative"
}
```