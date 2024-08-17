

---

# 🌟 **Pinou GLB Viewer** 🌟

Bienvenue dans **Pinou GLB Viewer** ! 🎉 Ce visualisateur de fichiers GLB est votre nouvel outil indispensable pour intégrer facilement des modèles 3D sur vos sites web. Il est conçu pour être **simple**, **rapide** et **personnalisable** sans avoir besoin de connaissances techniques avancées. 🚀

## 🎨 **Fonctionnalités**

✨ **Facile à intégrer** : Ajoutez de la 3D à vos pages web en quelques étapes simples.

✨ **Personnalisation illimitée** : Configurez l'affichage de votre modèle 3D avec une large gamme de paramètres.

✨ **Open Source** : Modifiez et utilisez le code comme bon vous semble tant que vous mentionnez l'auteur. Vous êtes libre de l'adapter à vos besoins ! 💡

## 🛠️ **Installation et Configuration**

### ⚠️ **Avertissement Important**

**Notez que Pinou GLB Viewer doit être utilisé sur un serveur réel**. Si vous essayez de l'exécuter localement en ouvrant simplement le fichier `index.html` dans votre navigateur, cela risque de ne pas fonctionner correctement. Pour résoudre ce problème sur Windows, vous pouvez installer l'extension **Go Live** dans Visual Studio Code. Nous vous montrerons comment faire cela dans le tutoriel ci-dessous.

### 📥 **Téléchargement avec Git**

1. **Cloner le dépôt** :
   - Ouvrez une ligne de commande ou terminal.
   - Exécutez la commande suivante pour cloner le dépôt :
     ```
     gh repo clone Pinou007/GLB-Viewer
     ```

2. **Accéder aux fichiers** :
   - Rendez-vous dans le répertoire cloné avec la commande :
     ```
     cd pinou-glb-viewer
     ```

### 📂 **Préparation du Fichier GLB**

Placez votre fichier 3D au format `.glb` dans le même répertoire que votre `index.html` ou votre page intégrée. Ce fichier doit être nommé **`modeles3d.glb`**.

### 🎛️ **Personnalisation**

Une fois le fichier `.glb` en place, personnalisez l'affichage et les options directement via l'URL en suivant les instructions ci-dessous.

## 🌍 **Structure de l'URL**

L'URL est composée de deux parties principales :

1. **Base de l'URL** 🏠 : L'adresse de la page HTML où le visualisateur est intégré.
2. **Paramètres de Configuration** ⚙️ : Ces paramètres suivent le symbole `?` dans l'URL et contrôlent divers aspects de l'affichage.

### Exemple d'URL

Voici un exemple d'URL avec des paramètres de configuration : 

```
http://votre-domaine.com/index.html?x=0.08&y=3.41&z=7.59&far=10000&fov=72.78&shadowEnabled=true
```

Dans cet exemple, plusieurs paramètres sont spécifiés pour définir la position de la caméra, le champ de vision et d'autres options graphiques.

## 📝 **Description des Paramètres**

Voici une liste des principaux paramètres que vous pouvez utiliser dans l'URL :

| 🗂️ **Catégorie**                | 🛠️ **Paramètre**        | 📄 **Description**                                     | 🎯 **Valeurs Exemples** |
|-------------------------------|------------------------|--------------------------------------------------------|----------------------|
| **Position de la Caméra**      | `x`                    | Définit la position de la caméra sur l'axe X. Cela permet de déplacer le point de vue horizontalement par rapport au modèle 3D. | `x=1.0`              |
|                               | `y`                    | Définit la position de la caméra sur l'axe Y. Cela ajuste la hauteur de la caméra par rapport au modèle 3D. | `y=2.0`              |
|                               | `z`                    | Définit la position de la caméra sur l'axe Z. Cela modifie la distance de la caméra par rapport au modèle 3D. | `z=3.0`              |
| **Plan de Clipping**           | `far`                  | Détermine la distance maximale à laquelle les objets seront rendus avant d'être "coupés" par le plan de clipping. Une grande valeur de `far` permet de voir les objets distants. | `far=10000`          |
|                               | `near`                 | Définit la distance minimale à laquelle les objets commencent à être rendus. Utile pour éviter les artefacts de clipping proche de la caméra. | `near=0.1`           |
| **Champ de Vision**            | `fov`                  | Spécifie l'angle de vision de la caméra, exprimé en degrés. Un champ de vision plus large donne une impression de profondeur plus grande mais peut déformer l'image. | `fov=90`             |
| **Effets et Graphismes**       | `shadowEnabled`        | Active ou désactive le rendu des ombres projetées par les objets. Les ombres ajoutent du réalisme mais peuvent réduire les performances si activées. | `true/false`         |
|                               | `shadowType`           | Détermine le type d'ombre utilisé, par exemple, des ombres douces (PCFSoft) qui offrent un rendu plus réaliste. | `shadowType=2`       |
| **Personnalisation de l'UI**   | `guiWidth`             | Contrôle la largeur de l'interface utilisateur graphique (GUI) où vous pouvez ajuster les paramètres en temps réel. | `guiWidth=800px`     |
|                               | `guiPadding`           | Définit l'espacement interne de l'interface utilisateur graphique, ajustant ainsi la distance entre les éléments de l'interface et les bords de la fenêtre. | `guiPadding=30px`    |
|                               | `guiBorderRadius`      | Ajuste l'arrondissement des coins de l'interface utilisateur graphique, donnant un aspect plus moderne et lisse à l'interface. | `guiBorderRadius=30px`|
|                               | `guiFontSize`          | Contrôle la taille de la police utilisée dans l'interface utilisateur graphique, ce qui peut améliorer la lisibilité des options. | `guiFontSize=19px`   |
| **Effets Visuels**             | `filmEnabled`          | Active ou désactive un effet de film granuleux sur l'écran, ajoutant une texture stylisée à l'affichage. | `true/false`         |
|                               | `glitchEnabled`        | Active ou désactive un effet de distorsion numérique, imitant une sorte de glitch visuel pour un effet artistique. | `true/false`         |
|                               | `displacementEnabled`  | Active ou désactive l'effet de déplacement qui modifie la géométrie du modèle en fonction d'une texture de déplacement. | `true/false`         |
|                               | `dotScreenEnabled`     | Active ou désactive un effet de tramage, qui donne à l'image un look pixelisé ou en points, semblable à l'impression d'une bande dessinée. | `true/false`         |
|                               | `asciiArtEnabled`      | Active ou désactive un effet visuel qui transforme l'affichage en art ASCII, rendant l'image en utilisant uniquement des caractères. | `true/false`         |
|                               | `psychedelicEnabled`   | Active ou désactive un effet psychédélique qui applique des couleurs vives et des déformations pour un résultat visuel unique. | `true/false`         |

### 🛠️ **Exemple de Personnalisation**

Supposons que vous souhaitiez désactiver les ombres et utiliser un champ de vision plus large. Vous pourriez configurer votre URL comme suit :

```
http://votre-domaine.com/index.html?x=0.08&y=3.41&z=7.59&far=10000&fov=90&shadowEnabled=false&guiWidth=800px&guiPadding=30px
```

Cette URL configurera l'application avec ces paramètres spécifiques. 🔧

## 🚀 **Tuto : Exécution sur Windows et Serveur**

### 📥 **Téléchargement et Exécution sur Windows**

1. **Télécharger les fichiers** :
   - Clonez ou téléchargez le dépôt GitHub contenant le fichier `index.html` et placez-le dans un répertoire dédié sur votre machine.

2. **Installer Visual Studio Code** (si ce n'est pas déjà fait) :
   - Téléchargez Visual Studio Code depuis [le site officiel](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user).
   - Installez-le en suivant les instructions d'installation.

3. **Installer l'extension Go Live** :
   - Ouvrez Visual Studio Code.
   - Accédez à l'onglet des extensions (icône de carré avec une brique dans la barre latérale gauche).
   - Recherchez **"Live Server"** dans la barre de recherche.
   - Cliquez sur "Installer" pour ajouter l'extension à votre environnement.

4. **Lancer le serveur local** :
   - Ouvrez le répertoire contenant votre fichier `index.html` dans Visual Studio Code.
   - Cliquez sur "Go Live" dans la barre

 d'état en bas de l'écran.
   - Une fenêtre de navigateur s'ouvrira automatiquement, exécutant votre projet sur un serveur local.

### 🌐 **Déploiement sur un Serveur**

1. **Télécharger les fichiers sur le serveur** :
   - Transférez les fichiers de votre projet (incluant `index.html` et `modeles3d.glb`) sur votre serveur via FTP, Git, ou une interface d'administration web.

2. **Configurer les paramètres** :
   - Ajustez les paramètres de votre serveur si nécessaire pour servir les fichiers `.glb` correctement, surtout si vous utilisez un serveur HTTP.

3. **Tester l'accès** :
   - Accédez à votre site via le domaine ou l'adresse IP fournie par votre hébergeur et assurez-vous que tout fonctionne comme prévu.

## 🤝 **Contribuer**

Ce projet a été développé par un jeune développeur passionné. Vous êtes libres de modifier et d'utiliser ce projet pour vos propres besoins. Toutefois, merci de mentionner l'auteur original si vous redistribuez ou utilisez ce code dans un autre projet. 🛠️💻

---

Merci d'utiliser **Pinou GLB Viewer**. Si vous avez des suggestions, des bugs à signaler, ou des améliorations à proposer, n'hésitez pas à ouvrir une issue ou une pull request sur GitHub ! 🚀

---
