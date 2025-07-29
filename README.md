# 📐 Bipartite graph - VHS

Cette visualisation permet de représenter les liens existants entre les différentes region pairs de la table region_pairs de l'application AIKON.
Ici, nous prendrons comme exemple les regions de trois witnesses de la base de données du projet VHS : le witness 75, le witness 76 et le witness 116. 
Le but sera d'opérer les comparaison suivantes : 
- witness 75 / witness 116
- witness 76 / witness 116



## 📷 Aperçu

![Aperçu de la visualisation](images/aperçu.png)

## 💻 Fonctionnalités : 

- Affichage des regions issues de chaque witness
- Comparaison visuelle facilitée grâce à l'alignement des colonnes 
- Liens entre régions similaires représentés par des arêtes colorées en rouge 
- Interaction dynamique : en cliquant sur une region, les liens la connectent aux autres
- Possibilité d'afficher le score de similarité 
- Epaisseur des liens varie en fonction du score de similarité 
- Chargement progressif : un bouton "Afficher plus" permet d'afficher davantage de regions pour éviter de surcharger l'ordinateur

## ⚙️ Installation et utilisation

### Lancer la visualisation sur son ordinateur 

1. Clone ce dépôt Github : 

```bash
git clone https://github.com/Cateatspython/bipartite_graph
cd bipartite_graph

```

2. Lancer le fichier bipartite_graph.html sur un serveur local (par exemple en utilisant Live Server)

### Réutiliser le code sur un autre projet de l'application AIKON 

⚠️ Il s'agit d'une preuve-de-concept qui n'a pas pour vocation d'intégrer l'application AIKON dans sa forme actuelle !

Néanmoins, il est possible de tester cette visualisation avec un autre export provenant d'une base de données d'un projet utilisant AIKON.

1. Exporter le contenu de la table region_pairs d'un witness que l'on veut comparer avec un autre witness.

2. Exporter les regions des deux witnesses que l'on veut comparer directement sur l'application AIKON dans la rubrique All regions en cliquant sur `Download` en haut à gauche. Il est nécessaire de les ranger dans un dossier \regions dans le répertoire contenant le fichier `bipartite_graph.html`

3. Utiliser le Jupyter Notebook `nettoyage_donnees_vhs.ipynb` en suivant les instructions pour nettoyer le fichier csv afin qu'il ne reste plus que les regions des deux witnesses que l'on veut comparer.

4. Dans le fichier `bipartite_graph.html`, modifier le nom du fichier dans la partie JavaScript.
```javascript 
    const file = "csv_files/wit75.csv";
```

5. Si votre dossier contenant les images n'est pas au même endroit ou qu'il ne porte pas le même nom, modifier le chemin vers les images des regions dans le fichier `bipartite_graph.html`
```javascript
    const imagePath = "regions/";
```

6. Ouvrir le fichier `bipartite_graph.html` sur un serveur local (par exemple en utilisant Live Server)


Visualisation réalisée dans le cadre d'un stage de fin d'étude du master TNAH à l'Observatoire de Paris d'avril à août 2025.