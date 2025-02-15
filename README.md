# 📄 Get Next Line

## 📝 Présentation

**Get Next Line** est un projet visant à implémenter une fonction permettant de lire **une ligne à la fois** depuis un **descripteur de fichier** (`fd`).  
Ce projet permet d’explorer la gestion **des buffers, de la mémoire dynamique et des variables statiques**.

L'objectif est de **lire un fichier sans en stocker tout le contenu en mémoire**, en retournant chaque ligne lue au fur et à mesure.

---

## 🛠️ Fonctionnalités

### ✅ Partie Obligatoire :
- **Lecture ligne par ligne depuis un fichier**.
- **Utilisation de `read()` et gestion dynamique de la mémoire** (`malloc`, `free`).
- **Retourne `NULL` en cas d'erreur ou si la fin du fichier est atteinte**.
- **Gestion correcte du `BUFFER_SIZE`**, défini au moment de la compilation :
  - `cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c`
- **Utilisation d’une seule variable statique** pour stocker les lectures incomplètes.
- **Aucune fuite mémoire autorisée**.

### 🎯 Bonus (si implémenté) :
- **Gestion de plusieurs fichiers ouverts simultanément (`fd`)** sans confusion des contenus lus.
- **Optimisation de la mémoire et réduction du nombre d’appels à `read()`**.

---

## 📌 Technologies Utilisées

- **C (Norminette respectée)**
- **Gestion des fichiers (`open`, `read`, `close`)**
- **Allocation dynamique (`malloc`, `free`)**
- **Manipulation de buffers et gestion des chaînes**
- **Utilisation de variables statiques pour le stockage intermédiaire**

---

## 🏗️ Structure du Projet

📜 get_next_line.h  
📜 get_next_line.c  
📜 get_next_line_utils.c  
📜 main.c  
📜 testty.txt  
📜 .gitignore  

---

## 🔥 Difficultés Rencontrées

- **Gestion efficace des lectures partielles** sans surcharge mémoire.  
- **Implémentation correcte de la lecture ligne par ligne** même si `\n` est absent en fin de fichier.  
- **Stockage et manipulation optimisés des buffers pour éviter les fuites mémoire**.  
- **Compatibilité avec différentes tailles de `BUFFER_SIZE`** (1, 42, 9999, 10 000 000).  
- **Gestion de plusieurs fichiers simultanément dans la version bonus**.  

---

## 🏗️ Mise en place

1. **Cloner le dépôt** :  
   ```bash
   git clone https://github.com/ton-repo/get_next_line.git
   cd get_next_line

2. **Compiler le projet** :
   ```bash
   make
3. **Compiler et exécuter un test** :
   ```bash
   gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 main.c get_next_line.c get_next_line_utils.c -o gnl_test
   ./gnl_test testty.txt
4. **Nettoyer les fichiers compilés** :
   ```bash
   make clean
   make fclean

---

## 👨‍💻 Équipe  

👤 Grégoire Chamorel (Gchamore)  

---

## 📜 Projet réalisé dans le cadre du cursus 42.  

Tu peux bien sûr modifier ce README selon tes besoins, ajouter plus de détails sur ton approche et des instructions d’installation précises. 🚀  
