# tp-devops-equipe

TP DevOps en équipe — EIGSICA, filière IABD.

Dépôt de travail collaboratif : l'équipe applique un workflow Git avec branches de fonctionnalités et pull requests autour d'une petite application Python, répartie entre une partie **données** (`feat-data`) et une partie **interface** (`feat-interface`).

> État actuel : le code est encore au stade de squelette (voir « Contenu du dépôt »).

## Contenu du dépôt

| Fichier | Description |
|---|---|
| `app.py` | Point d'entrée de l'application. Ne contient pour l'instant que le texte `Bonjour`, qui n'est pas du Python valide : `python app.py` échoue tant qu'il n'est pas remplacé (par exemple par `print("Bonjour")`) |
| `database.py` | Module prévu pour la base de données. Contient pour l'instant un simple `input()` demandant un entier |
| `settings.conf` | Configuration : `DB_URL=localhost` et `THEME=DARK` |
| `settings.onf` | Copie incomplète de `settings.conf` (seulement `DB_URL`). Le nom est probablement une faute de frappe : à supprimer ou à renommer |

## Prérequis

- Git
- Python 3.9 ou plus récent

## Installation

```bash
git clone https://github.com/ibralearn/tp-devops-equipe.git
cd tp-devops-equipe
```

## Workflow d'équipe

Les contributions passent par des branches de fonctionnalité fusionnées dans `main` via pull request :

1. Récupérer la dernière version : `git pull origin main`
2. Créer ou rejoindre la branche de sa partie : `feat-data` ou `feat-interface`
3. Committer par petites étapes, avec des messages au format `feat: ...` ou `fix: ...`
4. Pousser la branche : `git push origin feat-data`
5. Ouvrir une pull request vers `main`, relue par un coéquipier avant fusion

## Équipe

| Contributeur | Contributions |
|---|---|
| IbrahimCisse (`ibralearn`) | Dépôt initial, relecture et fusion des pull requests |
| Daryl | Interface graphique (`feat-interface`) |
| Contributeur de `feat-data` | Configuration de la base de données (commits signés « Your Name » : nom d'auteur Git à configurer, voir ci-dessous) |

Pour que vos commits portent le bon nom :

```bash
git config --global user.name "Votre Nom"
git config --global user.email "vous@exemple.com"
```

## Pistes d'amélioration

- Remplacer les fichiers squelettes par une vraie application
- Ajouter un `requirements.txt` et un `.gitignore`
- Mettre en place des tests automatisés
- Ajouter un pipeline d'intégration continue (GitHub Actions)
- Conteneuriser l'application avec un `Dockerfile`
