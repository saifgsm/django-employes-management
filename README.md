# Gestion des employés (Django)

**Auteur : Gouasmia Sifeddine**

## Description

Application web développée avec **Django** pour gérer une liste d'employés. Elle permet de faire les opérations de base (CRUD) sur les employés : nom, email, poste et salaire.

## Fonctionnalités

- Afficher la liste des employés.
- Ajouter un employé via un formulaire.
- Modifier les informations d'un employé.
- Supprimer un employé (avec page de confirmation).
- Gérer les données depuis l'interface d'administration Django.

## Technologies utilisées

- **Python 3**
- **Django 6.1**
- **SQLite** (base de données par défaut)
- **python-dotenv** pour les variables d'environnement
- **Gunicorn** pour le déploiement

## Structure du projet

```
gestion/      # configuration du projet (settings, urls)
employe/      # application : modèle, vues, formulaires, templates
manage.py
requirements.txt
.env.example  # modèle du fichier de configuration
```

## Installation

### 1. Cloner le dépôt

```bash
git clone https://github.com/saifgsm/django-employes-management.git
cd django-employes-management
```

### 2. Créer et activer un environnement virtuel

```bash
python -m venv env
# Windows
env\Scripts\activate
# macOS / Linux
source env/bin/activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

### 4. Configurer les variables d'environnement

Copie le fichier `.env.example` en `.env`, puis remplace `DJANGO_SECRET_KEY` par une clé secrète. Tu peux en générer une avec :

```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

### 5. Créer la base de données et lancer le serveur

```bash
python manage.py migrate
python manage.py runserver
```

L'application est ensuite disponible sur http://127.0.0.1:8000/.

## Routes principales

| URL | Action |
|---|---|
| `/` | Liste des employés |
| `/ajouter/` | Ajouter un employé |
| `/modifier/<id>/` | Modifier un employé |
| `/supprimer/<id>/` | Supprimer un employé |
| `/admin/` | Interface d'administration |
