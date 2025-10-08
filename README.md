
# 🧠 Projet d’Intelligence Artificielle Multimodale  
### *Reconnaissance faciale et vocale avec interaction parlée*

---

## 🌀 Description
Ce projet a pour but de concevoir une **intelligence artificielle multimodale** capable d’identifier une personne à la fois par **son visage** et **sa voix**, puis de **lui répondre verbalement**.  
L’objectif final est de permettre à l’IA de reconnaître un individu et de lui adresser un message personnalisé, par exemple :  

> “Bonjour Bruxelles, content de te revoir !”

Le système s’appuie sur plusieurs modules complémentaires :  
- **YOLOv8** pour la détection des visages,  
- **DeepFace** pour l’identification,  
- **Whisper** pour la reconnaissance vocale,  
- **Text-to-Speech (pyttsx3)** pour la réponse vocale.
- **Flask(Python)** pour l'interface graphique (web).  


---

## ⚙️ Fonctionnalités principales
- 🎯 **Reconnaissance faciale en temps réel** via la caméra.  
- 🧬 **Identification précise** des visages enregistrés dans la base de données.  
- 🔊 **Réponse vocale automatique** selon l’identité reconnue.  
- 🗣️ **Reconnaissance vocale (bonus)** : l’IA peut également comprendre la parole de l’utilisateur grâce à Whisper.  
- 💬 **Interaction simple et naturelle** entre l’humain et la machine.

---

## 🧩 Architecture du système

```
[Caméra] ---> [YOLOv8] ---> [DeepFace] ---> [Nom de la personne]
                                        ↓
[Micro] ---> [Whisper] ---> [Texte reconnu]
                                        ↓
           [Text-to-Speech] ---> “Bonjour {Nom}, content de te revoir !”
```

---

## 📁 Structure du projet

```
/AI_Recognition_Project
│
├── /dataset/                  # Base de visages
│     ├── Bruxelles/
│     ├── CherryKath/
│     └── ...
│
├── /models/                   # Poids YOLO / modèles DeepFace
├── /templates/                # Pour Flask(HTML)
├── /Static/                   # CSS, JS, images
│
├── /scripts/
│     ├── face_recognition.py  # YOLO + DeepFace
│     ├── voice_recognition.py # Whisper
│     ├── tts.py               # Text-to-Speech
│     └── main.py              # Script principal (fusion des modules)
│
├── requirements.txt           # Librairies et utilitaires utilisés pour le projet
└── README.md
```

---

## 🧠 Technologies utilisées

| Domaine | Outil / Librairie | Description |
|----------|------------------|--------------|
| **Vision** | YOLOv8 | Détection rapide et précise des visages |
| **Reconnaissance faciale** | DeepFace / FaceNet | Comparaison et identification |
| **Audio → Texte** | Whisper (OpenAI) | Reconnaissance vocale haute précision |
| **Texte → Voix** | pyttsx3 / gTTS | Génération d’une voix naturelle |
| **Base de données** | JSON / SQLite | Stockage des profils et embeddings |
| **Interface** | Flask / Streamlit | Visualisation et interaction utilisateur |

---

## 💬 Exemple d’interaction

```
🧠 [YOLO] : visage détecté.
🧬 [DeepFace] : identité reconnue → Bruxelles.
🔊 [TTS] : “Bonjour Bruxelles, content de te revoir !”
🎙️ [Whisper] : “Salut, comment tu vas ?”
🧠 [Réponse IA] : “Je vais bien, prêt à t’aider sur ton projet d’art numérique.”
```

---

## 🧑‍💻 Auteur
**BEYENE BRUXELLES GAMALIEL MC ILROY**  
Projet d’**Arts Numériques** – Reconnaissance faciale et vocale intelligente.  
Une exploration de la **fusion entre la perception visuelle et sonore** au service de l’interaction homme-machine.
