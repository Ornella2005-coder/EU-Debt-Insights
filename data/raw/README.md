# Données brutes (Eurostat)

Ce dossier contient les fichiers CSV sources utilisés par le modèle Power BI.

| Fichier attendu | Jeu Eurostat | Lien |
|---|---|---|
| `gov_10dd_edpt1.csv` | Déficit/excédent, dette publique et données associées (PDE) | https://ec.europa.eu/eurostat/databrowser/view/gov_10dd_edpt1/default/table |
| `gov_10a_main.csv` | Principaux agrégats des administrations publiques | https://ec.europa.eu/eurostat/databrowser/view/gov_10a_main/default/table |
| `lib_geo.csv` | Codes pays → noms en français (colonnes `EUR`, `Europe`) | référentiel personnel |

## Paramètres d'extraction

- **Fréquence** : annuelle · **Période** : 2005–2025 · **Secteur** : S13 (administrations publiques)
- `gov_10dd_edpt1` — indicateurs `B1GQ` (PIB), `B9` (solde), `D41PAY` (intérêts), `GD` (dette) ; unités `MIO_EUR` et `PC_GDP`
- `gov_10a_main` — indicateurs `TE` (dépenses totales), `TR` (recettes totales) ; unités `MIO_EUR` et `PC_GDP`
- **Format** : téléchargement CSV « format large » (une colonne par année), comme attendu par les requêtes Power Query

Téléchargement direct via l'API Eurostat (format TSV) :

```
https://ec.europa.eu/eurostat/api/dissemination/sdmx/2.1/data/gov_10dd_edpt1?format=TSV
https://ec.europa.eu/eurostat/api/dissemination/sdmx/2.1/data/gov_10a_main?format=TSV
```

Données © Union européenne, Eurostat — licence CC BY 4.0.
