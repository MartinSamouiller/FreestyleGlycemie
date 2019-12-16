# Freestyle Glycemie optimisation

Analyse des données de glycémie (Diabète type 1)

data : relevé de glycémie sur capteur - Freestyle libre
descriptif : 

src : notebook sur l'analyse des données
- FreestyleExtract.ipynb : utilisé pour extraire les données du capteur à partir du fichier .cvs, utilisé par les médecins

### 1_TAUX2H : Déterminer le taux de glycémie à +2H après repas

Données d'entrée : 
- Heure du repas
- Type de repas (dej, lunch, dinner)
- Unité Lente (Insuline)
- Unité Rapide (Insuline)
- Taux de glycémie (T0)
- Taux de glycémie (T-1H)
- Taux de glycémie (T-2H)
- Taux de glycémie (T-3H)
- Taux de glycémie (T-4H)
- Actions entre T0 et T-4H (données non disponibles dans les relevés du capteur) - exemples : sport, travail, marche, canapé TV
- Contenut du repas (données non disponibles)

Données de sortie : 
- Taux de glycémie à T+2H

### 2_UNITES_LENTE_RAPIDE  - Le vrai problème : 
Le taux de glycémie doit rester entre 90mg/dL et 120mg/dL
Connaitre le nombre d'unités de Lente et Rapide à faire pour chaque repas pour rester dans l'intervale 90-120mg/dL

Données d'entrée : 
- Heure du repas
- Type de repas (dej, lunch, dinner)
- Taux de glycémie (T0)
- Taux de glycémie (T-1H)
- Taux de glycémie (T-2H)
- Taux de glycémie (T-3H)
- Taux de glycémie (T-4H)
- Actions entre T0 et T-4H (données non disponibles dans les relevés du capteur) - exemples : sport, travail, marche, canapé TV
- Contenut du repas (données non disponibles)

Données de sortie : 
- Unité Lente (Insuline)
- Unité Rapide (Insuline)


