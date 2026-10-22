# Livrable — Modélisation de la probabilité de défaut

| Fichier | Contenu |
|---|---|
| `credit_risk.ipynb` | **Notebook unique** : tout le code (17 modules), toutes les analyses (parties 1 à 8, sujet 1.1 à 1.5.3), les 59 tests unitaires (partie 9). Déjà exécuté. |
| `rapport.tex` / `rapport.pdf` | Rapport : méthodologie, résultats, analyse, démonstrations mathématiques (annexe A). |
| `documentation.tex` / `documentation.pdf` | Documentation technique et fonctionnelle du code. |
| `data/LoanDetails.csv` | Données sources. |
| `resultats/` | Sorties du notebook : données traitées, tableaux (CSV et LaTeX), figures. |
| `requirements.txt` | Dépendances Python. |

## Réexécuter le notebook

Depuis ce dossier :

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute --inplace credit_risk.ipynb
```

L'exécution dure quelques minutes et régénère `resultats/` à l'identique (graine 42).

## Compiler les documents LaTeX

Prérequis : une distribution LaTeX (MiKTeX ou TeX Live). Depuis ce dossier, car les figures sont
lues dans `resultats/figures/` :

```bash
latexmk -pdf rapport.tex
latexmk -pdf documentation.tex
```
