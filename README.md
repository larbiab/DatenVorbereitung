# Datenvorbereitung mit Python

Vom Rohdatensatz zum trainierbaren Modell – Begleitmaterial zur Vorlesung (Bachelor Informatik).

[![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/larbiab/DatenVorbereitung/blob/main/Emden_Probevorlesung_Datenvorbereitung_Python.ipynb)

## Inhalt

| Datei | Beschreibung |
|---|---|
| `Emden_Probevorlesung_Datenvorbereitung_Python.ipynb` | Notebook zur Vorlesung – jeder Code der Folien steht hier wortgleich |
| `california_housing_dirty.csv` | Übungsdatensatz (California Housing, künstlich verschmutzt) |
| `requirements.txt` | Benötigte Python-Pakete |

## Aufbau des Notebooks

1. **Erkunden** – pandas (`head`, `hist`, `info`, `describe`) und Kontext
2. **Reinigen** – unerwartete Werte, uneinheitliche Kategorien, unerwünschte Zeilen und Spalten
3. **Umwandeln** – erst teilen, dann lernen: kategoriale Werte, fehlende Daten, Normalisierung
4. **Pipeline** – alle Schritte reproduzierbar mit scikit-learn
5. **Fazit und Transfer**

Die Zellen „Versuch 1“ und „Versuch 2“ enden **absichtlich** mit einem Fehler.

## Starten

**Google Colab:** auf den Button oben klicken – keine Installation nötig.

**Lokal:**

```bash
git clone https://github.com/larbiab/DatenVorbereitung.git
cd DatenVorbereitung
pip install -r requirements.txt
jupyter notebook
```

Das Notebook lädt den Datensatz über die Variable `data_url` direkt aus diesem Repository.
Ohne Internetverbindung: `data_url = "california_housing_dirty.csv"` setzen.

## Datensatz

`california_housing_dirty.csv` ist eine Übungsfassung des California-Housing-Datensatzes
(US-Zensus 1990; Pace, R. K. & Barry, R. (1997): *Sparse Spatial Autoregressions*,
Statistics & Probability Letters 33(3), 291–297; in der Fassung `housing.csv` aus Géron,
*Hands-On Machine Learning*). Für die Lehre wurden reproduzierbar (SEED 42) typische Probleme
eingebaut: eine ID-Spalte, Preise mit „$“, uneinheitliche Schreibweisen in `ocean_proximity`
und 250 doppelte Zeilen.

## Literatur

- Aurélien Géron: *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow*, 3. Aufl., O'Reilly, 2022 (Kapitel 2).
- Wes McKinney: *Python for Data Analysis*, 3. Aufl., O'Reilly, 2022.
