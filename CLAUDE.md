# Instruccions per a Claude

Repo del tauler "Economia familiar" (GitHub Pages). Repo PÚBLIC: només s'hi pot pujar `index.html` xifrat, `README.md`, `CLAUDE.md` i `.gitignore`.

## Regles
- MAI pujar res de `privat/` (dades en clar, scripts amb noms, `.clau`). Abans de cada commit, comprova `git status` i que no hi hagi cap fitxer de `privat/`, `.xls`, `.csv` ni `.clau`.
- `index.html` sempre s'ha de generar amb `python privat/encrypt.py`; mai copiar-hi el tauler en clar.

## Actualització mensual
1. Deixar els nous extractes .xls de Santander a `privat/extractes/`.
2. Regenerar `privat/economia-familiar.html` a partir de `privat/template.html` i els moviments (scripts `parse.py` → `cat.py` → `prep.py`; actualitzar `CFG` amb saldos de tancament, estat dels mesos, saldos de comptes, targetes i hipoteca).
3. `python privat/encrypt.py` (requereix `pip install cryptography`).
4. Commit només d'`index.html` i push a `main`.
