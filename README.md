README - Versions FR & EN
🇫🇷 Version Française

# 🎯 Système de Reconnaissance Faciale avec Alertes SMS

Un système de surveillance intelligent permettant la **reconnaissance faciale en temps réel** et l’**envoi automatique d’alertes SMS** lorsqu’un visage non autorisé est détecté.  Ce projet combine vision par ordinateur, apprentissage automatique et services cloud pour offrir une solution **moderne, sécurisée et performante**.

---

## 📑 Table des matières

* ✨ Fonctionnalités
* 🛠️ Technologies
* 📋 Prérequis
* ⚙️ Installation
* 🔧 Configuration
* ▶️ Utilisation
* 🏗️ Architecture du projet
* 📸 Démonstration
* 👤 Auteur

---

## ✨ Fonctionnalités

* 📷 Capture vidéo en temps réel via webcam ou caméra Raspberry Pi
* 🧠 Reconnaissance faciale basée sur des encodages pré‑enregistrés
* 📩 Envoi automatique d’alertes SMS via **Twilio API** en cas d’intrus
* 📝 Enregistrement des événements dans un fichier **CSV (logs)**
* ⚡ Traitement rapide et optimisé pour des résultats en temps réel
* 👀 Interface visuelle avec **OpenCV**

---

## 🛠️ Technologies

| Technologie      | Rôle                             |
| ---------------- | -------------------------------- |
| Python           | Langage principal                |
| OpenCV           | Capture & affichage vidéo        |
| face_recognition | Détection & encodage des visages |
| dlib             | Traitement d’images              |
| Twilio API       | Envoi d’alertes SMS              |
| Pickle           | Sauvegarde des encodages         |

---

## 📋 Prérequis

* Python **3.7+**
* Caméra (webcam ou Raspberry Pi Camera)
* Compte **Twilio**
* Système : Windows / Linux / macOS

---

## ⚙️ Installation

```bash
git clone https://github.com/WafaeBouajaja/Reconnaissance-Faciale.git
cd Reconnaissance-Faciale
pip install -r requirements.txt
```

---

## 🔧 Configuration

### 🔑 Identifiants Twilio

Créer un fichier **.env** à la racine :

```env
TWILIO_ACCOUNT_SID=xxxxxxxxxxxxxxxxxxxx
TWILIO_AUTH_TOKEN=xxxxxxxxxxxxxxxxxxxx
TWILIO_PHONE_NUMBER=+212XXXXXXXXX
ALERT_PHONE_NUMBER=+212XXXXXXXXX
```

### 🖼️ Encodage des visages autorisés

1. Créer le dossier `authorized_faces/`
2. Ajouter les images des personnes autorisées (`.jpg` / `.png`)
3. Générer les encodages :

```bash
python encode_faces.py
```

---

## ▶️ Utilisation

```bash
python main.py
```

Le programme :

* Active la caméra
* Affiche les visages reconnus (**vert + nom**)
* Affiche les visages inconnus (**rouge + "Inconnu"**)
* Envoie un **SMS d’alerte** en cas d’intrusion
* Enregistre les événements dans `logs.csv`

👉 Pour quitter : **Appuyer sur la touche `q`**

---

## 🏗️ Architecture du projet

```
📂 Face-Recognition-Alert
 ├── authorized_faces/
 ├── encodings.pickle
 ├── encode_faces.py
 ├── main.py
 ├── test_camera.py
 ├── requirements.txt
 └── logs.csv
```

---

## 📸 Démonstration

* 🟢 Visage reconnu → encadré en vert + nom
* 🔴 Visage inconnu → encadré en rouge + « Inconnu »
* 📲 Alertes SMS instantanées
* 📑 Enregistrement automatique des événements

---

## 👤 Auteur

Projet réalisé dans un cadre académique et éducatif.
**Auteur : SOUKAINA AIT -LBACH**

---

---

# 🇬🇧 English Version — Facial Recognition System with SMS Alerts

An intelligent surveillance system enabling **real‑time facial recognition** and **automatic SMS alerts** when an unauthorized face is detected. This project combines computer vision, machine learning and cloud services to provide a **modern, secure and high‑performance solution**.

---

## 📑 Table of Contents

* ✨ Features
* 🛠️ Technologies
* 📋 Requirements
* ⚙️ Installation
* 🔧 Configuration
* ▶️ Usage
* 🏗️ Project Structure
* 📸 Demonstration
* 👤 Author

---

## ✨ Features

* 📷 Real‑time video capture via webcam or Raspberry Pi Camera
* 🧠 Facial recognition using pre‑encoded authorized faces
* 📩 **Automatic SMS alerts** via **Twilio API** upon intruder detection
* 📝 Event recording in a **CSV log file**
* ⚡ Optimized for real‑time performance
* 👀 Visual monitoring interface using **OpenCV**

---

## 🛠️ Technologies

| Technology       | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Main programming language |
| OpenCV           | Video capture & display   |
| face_recognition | Face detection & encoding |
| dlib             | Image processing          |
| Twilio API       | SMS notifications         |
| Pickle           | Encoding storage          |

---

## 📋 Requirements

* Python **3.7+**
* Camera (webcam or Raspberry Pi Camera)
* **Twilio account**
* OS: Windows / Linux / macOS

---

## ⚙️ Installation

```bash
git clone https://github.com/WafaeBouajaja/Reconnaissance-Faciale.git
cd Reconnaissance-Faciale
pip install -r requirements.txt
```

---

## 🔧 Configuration

### 🔑 Twilio Credentials

Create a **.env** file :

```env
TWILIO_ACCOUNT_SID=xxxxxxxxxxxxxxxxxxxx
TWILIO_AUTH_TOKEN=xxxxxxxxxxxxxxxxxxxx
TWILIO_PHONE_NUMBER=+123456789
ALERT_PHONE_NUMBER=+987654321
```

### 🖼️ Authorized face encoding

```bash
Add images → authorized_faces/
Run → python encode_faces.py
```

---

## ▶️ Usage

```bash
python main.py
```

The system will:

* Activate the camera
* Display recognized faces (**green + name**)
* Display unknown faces (**red + "Unknown"**)
* Send an **SMS alert** in case of intrusion
* Log events in `logs.csv`

👉 Quit: **Press `q`**

---

## 🏗️ Project Structure

```
📂 Face-Recognition-Alert
 ├── authorized_faces/
 ├── encodings.pickle
 ├── encode_faces.py
 ├── main.py
 ├── test_camera.py
 ├── requirements.txt
 └── logs.csv
```

---

## 📸 Demonstration

* 🟢 Green box + name → recognized face
* 🔴 Red box + “Unknown” → intruder
* 📲 Instant SMS notifications
* 📑 Automatic CSV logging

---

## 👤 Author

Project created for academic and educational purposes.
**Author: SOUKAINA AIT-LBACH**
