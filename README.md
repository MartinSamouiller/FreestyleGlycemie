# Freestyle Glycemie optimisation + Fitbit 

Analyse des données de glycémie (Diabète type 1)

data : 
- relevés de glycémie sur capteur - Freestyle libre
- relevés fitbit sur les derniers mois (freq cardiaque, sport)

src : notebook sur l'analyse des données
- FreestyleExtract.ipynb : utilisé pour extraire les données du capteur à partir du fichier .cvs, utilisé par les médecins

# Idées : 

## Analyse : 
- Analyses des taux de sucres journaliers 
- Creation de rapports personnalisés pour le medecin (grossesse USA)
- Determiner quels sont les facteurs qui influent le plus sur la glycemie
- Chercher le rapport entre taux de glucose et rythme cardiaque (sport) - si oui sur combien de jours peut il y avoir un impact entre une séance de sport et le taux de glucose
- Déterminer quels aliments modifies la glycémie de manière annormale (pour l'instant pas de données)


## Prediction : 
- Prediction du taux de sucre 2H après chaque repas (il manque les données les plus importantes : composition du repas)
- Prediciton de ce qu'il faut manger en fonction du taux de sucre précédent 
- Prediciton des unités à faire en fonction du taux de glucose et du repas prévu

# Dossiers code :

## 1_TAUX2H : Déterminer le taux de glycémie à +2H après repas

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

## 2_UNITES_LENTE_RAPIDE  - Le vrai problème : 
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


