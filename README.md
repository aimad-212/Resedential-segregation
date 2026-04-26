# 🏙️ UrbanDynamics Simulator : Socio-Economic & Segregation Model

[![NetLogo](https://img.shields.io/badge/NetLogo-7.0.2-orange.svg)](https://ccl.northwestern.edu/netlogo/)
[![Project Status](https://img.shields.io/badge/Status-Expert--Final-green.svg)]()

## 📌 Présentation du Projet
Ce simulateur urbain avancé, développé sous **NetLogo 7.0.2**, explore les dynamiques complexes de la ségrégation résidentielle en intégrant des facteurs socio-économiques réels. Contrairement au modèle classique de Schelling, ce projet couple la **préférence sociale** avec des **contraintes économiques** (loyer, budget) et des **besoins géographiques** (proximité du lieu de travail).

Le modèle illustre comment la gentrification, les disparités de revenus et les préférences de voisinage façonnent la structure spatiale d'une ville moderne.

---

## 🚀 Fonctionnalités Clés
- **Système Multi-Agents (SMA) :** 4 classes sociales distinctes (Précaires, Modestes, Moyens, Aisés) avec des revenus et des seuils de tolérance spécifiques.
- **Marché Immobilier Dynamique :** Les loyers fluctuent en temps réel selon la loi de l'offre et de la demande et la "gentrification" (la présence d'agents aisés fait monter les prix locaux).
- **Prise de Décision Multi-Critères :** Les agents déménagent en évaluant un score d'utilité pondéré :
  - **Social :** Ratio de voisins du même groupe.
  - **Économique :** Accessibilité financière (Loyer vs Budget).
  - **Géographique :** Distance au lieu de travail (CBD).
  - **Attractivité :** Qualité de vie intrinsèque du quartier.
- **Analyse Statistique :** Calcul en temps réel de l'**Indice de Dissimilarité (Ségrégation)** et du taux de satisfaction globale.

---

## 🛠️ Configuration de l'Interface
Pour un fonctionnement optimal, l'interface NetLogo doit comporter les éléments suivants :

| Type | Nom de la Variable | Description |
| :--- | :--- | :--- |
| **Boutons** | `setup`, `go` | Initialisation et exécution. |
| **Sliders** | `nb-groupe1..4` | Population par classe sociale. |
| **Sliders** | `seuil-tolerance` | Niveau d'exigence sociale des agents. |
| **Sliders** | `poids-prix` | Importance du budget dans le choix. |
| **Chooser** | `visualisation` | Modes : "Groupes", "Prix", "Satisfaction". |

---

## 🧪 Logique Algorithmique
### 1. Satisfaction Complexe
L'agent n'est pas seulement "heureux" ou "malheureux". Il calcule une fonction d'utilité $U$ :
$$U = (w_s \cdot S) + (w_e \cdot E) + (w_t \cdot T)$$
Où $w$ représente les poids (sliders) pour le Social ($S$), l'Économique ($E$) et le Transport ($T$).

### 2. Marché du Logement
Le prix des patchs évolue à chaque tick :
- **Augmentation :** Si des agents à haut revenu occupent la zone.
- **Diffusion :** Les prix se lissent entre voisins pour créer des quartiers cohérents.

---

## 📊 Indicateurs de Performance (Plots)
Le projet intègre des graphiques pour analyser :
1. **Évolution Sociale :** Comparaison entre le taux de satisfaction (%) et l'indice de ségrégation.
2. **Dynamique Foncière :** Corrélation entre l'augmentation des loyers et le déplacement des populations précaires.

---

## 📦 Installation
1. Télécharger et installer [NetLogo 7.0.2](https://ccl.northwestern.edu/netlogo/).
2. Copier le code source dans l'onglet **Code**.
3. Créer les éléments d'interface listés ci-dessus.
4. Cliquer sur `setup` puis `go`.

---

## 📝 Licence
Ce projet est sous licence MIT. Libre à vous de l'adapter pour vos recherches en sociologie urbaine ou en économie spatiale.