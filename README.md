# 🏭 Smart Factory — Predictive Maintenance System

![Python](https://img.shields.io/badge/Python-3.9-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0-orange)
![Scikit-learn](https://img.shields.io/badge/ScikitLearn-1.0-green)

## 📋 Description

Système de maintenance prédictive industrielle basé sur 
le Machine Learning et le Deep Learning.
Utilise le dataset NASA C-MAPSS (20 631 relevés réels) 
pour prédire la durée de vie restante (RUL) de moteurs 
avant leur panne.

## 🎯 Objectif

Passer d'une maintenance réactive (on répare après la panne)
à une maintenance prédictive (on anticipe la panne).

## 🛠️ Technologies utilisées

- Python — langage principal
- TensorFlow / Keras — modèle LSTM
- Scikit-learn — Random Forest
- Plotly — dashboard interactif
- Pandas / NumPy — traitement des données

## 📊 Modèles développés

| Modèle | MAE | Amélioration |
|--------|-----|--------------|
| Random Forest | 29.88 cycles | baseline |
| LSTM | 20.50 cycles | +31.4% |

## 🚨 Système d'alerte automatique

| Statut | Seuil RUL | Action |
|--------|-----------|--------|
| Normal | > 100 cycles | Aucune |
| Attention | 50-100 cycles | Surveiller |
| Urgent | < 50 cycles | Intervenir ! |

## 📈 Résultats

- Dataset : 20 631 relevés — 100 moteurs NASA
- Capteurs utiles identifiés : 11 sur 21
- LSTM MAE : 20.50 cycles sur données de test
- Réduction Faux Négatifs grâce à marge de sécurité

## 🔄 Pipeline du projet

1. Chargement données NASA C-MAPSS
2. Sélection capteurs utiles (variance > 0.01)
3. Normalisation MinMaxScaler
4. Création séquences temporelles (30 cycles)
5. Entraînement LSTM (50 epochs max)
6. Système d'alerte automatique
7. Dashboard interactif Plotly

## 🏃 Comment utiliser

pip install -r requirements.txt
jupyter notebook notebooks/AI PROJECT.ipynb

## 👤 Auteur

Othmane Ait Said
Étudiant — Bachelor Technologies pour l'Industrie du Futur
Arts et Métiers — Campus Rabat

## 🔗 Lien avec l'industrie

Ce projet s'inspire directement de mon stage chez Distri Fer
où j'ai appliqué la méthode AMDEC/FMEA sur 3 machines.

La maintenance prédictive avec IoT et IA représente 
l'évolution naturelle de cette approche :
- Réduction des arrêts machines : 30 à 50%
- Réduction des coûts maintenance : 25%
- Augmentation durée de vie équipements : 20%
