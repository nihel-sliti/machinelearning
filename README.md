# Prédiction du diabète avec SVM

## 📝 Description
Ce projet vise à **prédire si un patient est diabétique** en utilisant des **Support Vector Machines (SVM)**. Plusieurs noyaux ont été testés pour identifier celui offrant la meilleure performance.

## 📊 Noyaux testés
- **Linéal** : Accuracy = 78.1%, AUC = 72.09%
- **RBF (Radial Basis Function)** : AUC = 66.5%
- **Polynomial** : AUC = 66.498108
- **Sigmoïde**: AUC = 40.976952

## 🔧 Étapes du projet
1. **Préparation des données** : Lecture du dataset et traitement des valeurs manquantes.
2. **Division en ensemble d’entraînement et de test**.
3. **Entraînement de modèles SVM** avec différents noyaux.
4. **Évaluation des performances** :
   - Matrice de confusion
   - Courbe ROC et AUC

## 🛠️ Outils utilisés
- **Python** : Pandas, Scikit-learn, Matplotlib, Seaborn
- **Modèles SVM** : Noyaux linéaire, RBF, polynomial et sigmoïde

## 📈 Visualisation de la matrice de confusion
![Confusion Matrix](image/matrice_de_confusion.png)

## 📂 Structure du code
- `diabetes_svm_linear` : Modèle avec noyau linéaire
- `diabetes_svm_rbf` : Modèle avec noyau RBF
- `diabetes_svm_poly` : Modèle avec noyau polynomial
- `diabetes_svm_sigmoid` : Modèle avec noyau sigmoïde

#  Modèles SVM avec différents noyaux
# .1 SVM avec noyau linéaire
Objectif : Trouver un hyperplan qui sépare les deux classes avec une marge maximale.

Performance :

Accuracy : 78.1%
Precision, Recall et F1-score :
Classe 0 : Precision = 80%, Recall = 90%
Classe 1 : Precision = 73%, Recall = 54%
AUC (Area Under Curve) : 72.09%
Analyse :

Le modèle a une meilleure précision sur la classe 0 que sur la classe 1.
L’AUC indique que le modèle a des performances raisonnables, mais peut être amélioré.
# .2 SVM avec noyau RBF (Radial Basis Function)
Objectif : Gérer les relations non linéaires entre les caractéristiques.
Performance :
AUC : 66.5%
Le noyau RBF n’a pas surpassé le noyau linéaire ici. Cela suggère que les relations entre les données pourraient être plutôt linéaires.
# .3 SVM avec noyau polynomial
Objectif : Capturer les relations complexes entre les variables en utilisant des polynômes.
Résultat : La performance peut varier en fonction du degré du polynôme utilisé.
# .4 SVM avec noyau sigmoïde
Objectif : Capturer des relations non linéaires semblables à un réseau de neurones.
Performance : Ce noyau est moins courant et peut parfois sous-performer par rapport à RBF ou linéaire.
# Matrice de confusion et évaluation des résultats
Matrice de confusion :

TP (True Positive) : Prédiction correcte que le patient est diabétique.
FP (False Positive) : Erreur, prédit diabétique alors que non.
FN (False Negative) : Erreur, patient réellement diabétique mais non détecté.
TN (True Negative) : Prédiction correcte de non-diabétique.
## Interprétation de l’AUC et des courbes ROC
Courbe ROC : Montre la relation entre taux de vrais positifs (TPR) et taux de faux positifs (FPR).
AUC : L’AUC (Area Under Curve) permet de comparer les noyaux :
Linéaire : 72.09%
RBF : 66.5%
Meilleure performance avec le noyau linéaire dans ce cas.

## 🚀 Résultats et conclusion
Le **noyau linéaire** a montré les meilleures performances, indiquant que les données ont une **relation plutôt linéaire**. Cependant, d'autres optimisations sont possibles avec une **normalisation** et **validation croisée**.

## 💬 Feedback
N'hésitez pas à ouvrir une **issue** ou à me contacter pour toute suggestion d'amélioration !

---

