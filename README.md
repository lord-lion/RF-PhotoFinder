Welcome to the RF_PhotoFinder wiki!
# RF_PhotoFinder
Searching pictures or a particular person in a dataset using Natural Language processing and SQL #ComputerVision #NLP #GeminiAPI #YOLOExplorer #YOLOV8.1 #LanceDB #Pytorch #SQL

# Etape 1 : Création d'un environnement
```
python -m venv env
```

# Etape 2 : Installation des lirairies
```
pip install -r requirements.txt
```

# Etape 3 : Création d'un dossier input à la racine du projet
```
RF_PhotoFinder 
            |- assets
             - src
             - input
```

# Etape 4 : Téléchargement de la dataset au lien suivant : 
 https://www.kaggle.com/datasets/hiteshsuthar101/myntra-fashion-product-dataset/data

# Etape 5 : Extraction de la dataset et positionnement du conteneu de la dataset sur le format suivant :
```
input
     |-Images
     |   |-0.jpg
     |   |-2.jpg
     |   ..
     |   ..
     |- Fashion Dataset.csv
```

# Etape 6 : Creation de la table de notre dataset dans notre base de donnée LanceDB

```
python src/make_table.py --database "~/.lancedb" --table_name "myntra" --data_path "input/Images" 
```

# Etape 7 : Lancement de l'application 

```
streamlit run src/app.py -- --table_name myntra
```
