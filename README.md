# 🧠 Deep Learning – Génération d’Images à Partir de Classes Cibles

Ce projet explore une approche inverse de la classification : **plutôt que de prédire une classe à partir d’une image, nous cherchons à générer une image qui maximise la probabilité d’appartenance à une classe cible donnée**. Cela permet d’interpréter ce que le modèle a réellement appris.

---

## 📁 Contenu du dépôt

- `notebook_classificateur_generateur.ipynb` : Notebook Jupyter complet et commenté, incluant :
  - Entraînement d’un CNN sur MNIST
  - Étude d’ablation
  - Comparaison avec k-NN et régression logistique
  - Analyse des scores de confiance et des quantiles
  - Optimisation inversée d’images (CNN et k-NN)

- `rapport_projet_classificateur_generateur.pdf` : Rapport de synthèse détaillé avec explications théoriques, résultats expérimentaux, et pistes d’amélioration.

---

## 🎯 Objectifs 

- Comprendre l’architecture d’un CNN et son fonctionnement sur le dataset MNIST
- Visualiser les décisions du modèle à travers l’optimisation d’entrées
- Comparer la qualité des prédictions et la calibration des probabilités
- Tester la robustesse du modèle avec des méthodes alternatives

---

## 📊 Modèles comparés

| Modèle                  | Accuracy | Observations |
|------------------------|----------|--------------|
| CNN                    | 99.00 %  | Très confiant et précis |
| k-NN                   | 96.88 %  | Probabilités discrètes, moins nuancé |
| Régression Logistique  | 92.58 %  | Moins précis mais meilleure gestion des incertitudes |

---

## 💡 Optimisation Inversée

Nous cherchons une image \( x \) telle que \( p_i(x) \) soit maximal, via gradient ascent dans le cas du CNN, ou approximation heuristique dans le cas du k-NN.

Cela permet de **visualiser la représentation interne du modèle** pour une classe cible, et d’évaluer ses biais potentiels.

---

## 📌 Auteurs

Projet réalisé en binôme dans le cadre du cours de Deep Learning 2024-2025 :
- Arnaud Chéridi
- Wayan Crain
- Yanis Aoudjit

---

## 🧭 Pistes d’amélioration

- Étendre à d’autres datasets (CIFAR-10, F-MNIST)
- Étudier d’autres modèles (SVM, Random Forest)
- Évaluer la robustesse face au bruit et aux perturbations adversariales
- Applications potentielles : reconnaissance d’écriture manuscrite universitaire
