# 📸 Redimensionner Automatiquement des Images avec Python  

🎯 **Gagnez du temps en redimensionnant toutes vos images en un clic !**  
Ce script permet de **sélectionner des images**, de les **redimensionner automatiquement**, puis de **les télécharger en `.zip`** en quelques secondes.  

---

## 🚀 Fonctionnalités  
✅ **Sélectionner facilement tes images** via une interface Google Colab 📂  
✅ **Redimensionner automatiquement toutes les images**  
✅ **Téléchargement automatique des images modifiées au format `.zip`**  

---

## 📥 Exécuter sur Google Colab (Aucune Installation Requise)  
🔗 **[Cliquez ici pour exécuter directement sur Google Colab](https://colab.research.google.com/github/Mcarre027/Resize-pictures-/blob/main/Redimensionner_des_Images_Automatiquement_.ipynb)**  

📌 **Instructions :**  
1️⃣ **Clique sur le lien Colab ci-dessus.**  
2️⃣ **Téléverse tes images via l'interface.**  
3️⃣ **Le script les redimensionne et télécharge automatiquement un `.zip` avec les images modifiées.**  

---

## 📂 Utilisation en Local (Optionnel)  
Si tu veux exécuter le script sur ton propre PC, voici comment faire :  

📌 **1️⃣ Installe Pillow (si ce n'est pas déjà fait) :**  
```bash
pip install pillow
📌 2️⃣ Exécute le script en Python :

python
Copier
Modifier
from PIL import Image
import os
import glob

# Définir la nouvelle taille des images
NEW_SIZE = (800, 600)

# Créer un dossier "resized" pour stocker les images modifiées
os.makedirs("resized", exist_ok=True)

# Parcourir et redimensionner toutes les images
for fichier in glob.glob("images/*.jpg"):
    img = Image.open(fichier)
    img.resize(NEW_SIZE).save(f"resized/{os.path.basename(fichier)}")

print("✅ Images redimensionnées avec succès !")
```
📩 Contact
📬 Besoin d’aide ? Ouvrez une issue sur GitHub ou contactez-moi sur LinkedIn !
