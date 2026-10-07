# Exploitation des données d'un ballon-sonde

Traitement et visualisation de la télémétrie relevée pendant un vol de ballon-sonde
atmosphérique, à partir du relevé brut `Donnees.csv`.

**BUT Réseaux & Télécommunications - IUT d'Auxerre**
Binôme : Dorian Ripoche et Oumar Ali Mahamat

## Les données

Le fichier source est un CSV à séparateur `;`, au format français (virgule décimale),
contenant pour chaque point de mesure : horodatage, altitude, vitesse, température
intérieure et température extérieure de la nacelle.

Le parsing gère ces deux particularités : conversion de l'heure `HH:MM:SS` en secondes
écoulées, et remplacement des virgules décimales par des points avant conversion en
flottant.

## Les scripts

| Script | Tracé |
|--------|-------|
| `courbe1.py` | Vitesse et température en fonction du temps |
| `courbe2.py` | Altitude et température extérieure dans le temps - lecture via le module `csv` |
| `courbe3.py` | Températures intérieure et extérieure en fonction de l'altitude |

`courbe3.py` est le plus parlant : il montre l'écart croissant entre l'intérieur et
l'extérieur de la nacelle à mesure que le ballon monte et que la température ambiante
chute.

## Dépendances

```
pip install matplotlib
```

Puis placer `Donnees.csv` dans le même dossier et lancer le script voulu.

## Compte rendu

`TP2-MAHAMAT-DorianV2.pdf` - analyse des courbes et interprétation des résultats.
