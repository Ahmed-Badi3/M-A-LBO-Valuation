# M-A-LBO-Valuation
Découvrez M-A-LBO-Valuation-Engine, un outil complet de modélisation financière et de valorisation M&amp;A sous Python. Il intègre la projection des flux FCFF, le calcul du WACC, une valorisation DCF, ainsi qu'un module de structuration LBO (Sources &amp; Uses, Cash Sweep, TRI, MoIC) et une matrice de sensibilité avancée pour vos analyses de risque.
# 📊 M&A & LBO Valuation Engine (Alpha Industry Case Study)

Modèle complet de modélisation financière, de valorisation d'entreprise par flux de trésorerie (DCF) et de structuration d'un rachat avec effet de levier (LBO) développé en Python.

---

## 🚀 Aperçu du Projet
Ce projet implémente un cas pratique de finance d'entreprise et de Private Equity appliqué à une PME industrielle fictive (*Alpha Industry*). Il simule l'intégralité du cycle d'investissement, de la projection des états financiers jusqu'à l'analyse de risque multicritère, le tout exécuté via un notebook interactif.

---

## 📂 Architecture & Modules du Modèle

Le projet est structuré en 4 modules majeurs :

1. **Projections Financières (Compte de Résultat & FCFF) :**
   * Trajectoire du Chiffre d'Affaires (base 100 M MAD, CAGR de 6%).
   * Marge d'EBITDA constante (20%), calcul du NOPAT (IS à 30%), des CapEx et de la variation du BFR.
   * Génération dynamique des **Free Cash Flows to Firm (FCFF)** sur un horizon de 5 ans.

2. **Coût du Capital (WACC) & Valorisation DCF :**
   * Calcul du coût des fonds propres via le MEDAF (CAPM) et pondération avec le coût de la dette après impôt (structure cible 60/40).
   * Actualisation des FCFF et calcul de la Valeur Terminale par la méthode de Gordon-Shapiro (croissance perpétuelle à 2%).
   * Détermination de la **Valeur d'Entreprise (Enterprise Value)** fondamentale.

3. **Structuration LBO & Cascade de Dette (*Debt Waterfall*) :**
   * **Sources & Uses :** Acquisition de la cible sur un multiple de 7,5x l'EBITDA + 2% de frais, financée à 55% par de la Dette Senior et à 45% par les Fonds Propres (*Equity*) du fonds de Private Equity.
   * **Cash Sweep :** Allocation de 80% du cash disponible chaque année au désendettement progressif.
   * **KPIs de Rentabilité :** Calcul du Multiple sur les Fonds Propres (**MoIC**) et du Taux de Rendement Interne (**TRI / IRR**).

4. **Analyse de Risque & Visualisation Avancée :**
   * Création d'une matrice de sensibilité croisée évaluant l'impact combiné du niveau d'endettement (levier de 45% à 65%) et du multiple de sortie (6,5x à 8,5x) sur le TRI.
   * Génération d'une **Heatmap** interactive via *Seaborn* pour cartographier les zones de rentabilité et de risque.

---

## 🛠️ Stack Technologique
* **Langage :** Python
* **Manipulation & Calculs :** Pandas, NumPy, NumPy-Financial
* **Visualisation :** Matplotlib, Seaborn
* **Environnement :** Google Colab / Jupyter Notebook

---

## ⚙️ Utilisation / Exécution
1. Ouvrir le notebook sur **Google Colab**.
2. S'assurer que les bibliothèques requises sont installées (`numpy-financial`, `seaborn`).
3. Exécuter les cellules séquentiellement du Module 1 au Module 4 pour générer les tableaux financiers, les résultats LBO et la matrice de sensibilité.
