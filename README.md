# README.md
"""
# Web UI Generator API

Cette API permet de générer du code HTML/CSS à partir d'images de maquettes web en utilisant un modèle de deep learning.

## Installation

1. Cloner le repository
2. Créer et activer un environnement virtuel ou anaconda
3. Installer les dépendances : `pip install -r requirements.txt`
4. Placer votre modèle SavedModel dans le dossier `model`

## Utilisation

1. Lancer le serveur : `uvicorn app.main:app --reload`
2. Visualiser l'interface app : `interface_app.html`

## Points de terminaison

- POST /generate-code : Générer du code à partir d'une image

## Exemple d'utilisation

```python
import requests

url = "http://localhost:8000/generate-code"
image = {"image": open("maquette.png", "rb")}
response = requests.post(url, image=image)
print(response.json())
```

## Structure du projet

```
projet_fastAPI/
├── app/
│   ├── __pycache__/
│   ├── static/
│   ├   ├──detected_images/
│   ├── __init__.py
│   ├── main.py
│   ├── utils.py
│   ├── config.py
│   
├── model/
    ├── faster_rcnn_resnet50_v1_640x640
├── interface_app.html
├── requirements.txt
└── README.md
```
"""