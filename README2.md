FetyMada v2.1.1

**FetyMada** est une application mobile Flutter permettant de découvrir, créer et gérer des événements à Madagascar en temps réel.

Elle intègre une carte interactive basée sur **OpenStreetMap**, un système de chat, des événements géolocalisés et une synchronisation en temps réel avec Supabase.

---

#  Fonctionnalités principales

##  Carte interactive (OpenStreetMap)

* Affichage des événements sur une carte
* Position GPS de l’utilisateur
* Mode satellite (via tuiles externes)
* Marqueurs personnalisés

##  Géolocalisation

* Détection automatique de la position utilisateur
* Calcul de distance vers les événements
* Événements proches

##  Système social

* Chat de groupe par événement
* Messagerie privée avec organisateurs
* Notifications en temps réel

##  Média

* Partage de photos et vidéos après événements
* Likes et commentaires

##  Avis

* Système de notation 1 à 5 étoiles
* Commentaires des participants

##  Engagement

* Favoris d’événements
* Liste personnalisée

##  Temps réel

* Synchronisation Supabase
* Messages instantanés
* Mise à jour des événements live

---

#  Stack technique

* Flutter (Mobile App)
* OpenStreetMap (flutter_map)
* Supabase (Backend + Realtime)
* Provider (State Management)
* Go Router (Navigation)
* Geolocator (GPS)
* Geocoding (adresses)

---

#  Installation

## 1. Cloner le projet

```bash
git clone https://github.com/TON_USERNAME/fetymada.git
cd fetymada
```

---

## 2. Installer les dépendances

```bash
flutter pub get
```

---

## 3. Lancer l’application

```bash
flutter run
```

---

#  Build APK (Release)

## Générer APK release

```bash
flutter build apk --release
```

 Fichier généré :

```
build/app/outputs/flutter-apk/app-release.apk
```

---

## Version optimisée

```bash
flutter build apk --release --split-per-abi
```

---

#  Configuration Supabase

Créer un projet sur :

 https://supabase.com/

Ajouter dans ton projet Flutter :

```dart
Supabase.initialize(
  url: "YOUR_SUPABASE_URL",
  anonKey: "YOUR_SUPABASE_ANON_KEY",
);
```

---

#  Base de données (Supabase)

Tables principales :

* events
* messages
* event_chats
* event_media
* event_reviews
* favorites
* participants
* notifications

---

#  Carte OpenStreetMap

Utilise flutter_map :

```yaml
urlTemplate: "https://tile.openstreetmap.org/{z}/{x}/{y}.png"
```

---

#  Structure du projet

```
lib/
├── core/
│   ├── services/
├── features/
│   ├── map/
│   ├── chat/
│   ├── events/
│   ├── media/
│   ├── reviews/
├── models/
├── providers/
├── screens/
├── widgets/
```

---

# Aperçu des fonctionnalités

* Carte des événements en temps réel
* Chat entre utilisateurs et organisateurs
* Publication de photos et vidéos
* Événements proches selon GPS
* Système de favoris

---

#  Roadmap

## V1 (Actuelle)

* Carte OpenStreetMap
* Événements
* GPS utilisateur
* Chat basique

## V2

* Assistant IA
* Itinéraire navigation
* Mode satellite

## V3

* Paiement billets
* QR Code entrée
* Streaming live événements

---

#  Contribution

Pull requests sont les bienvenues.

```bash
git checkout -b feature/new-feature
git commit -m "Add new feature"
git push origin feature/new-feature
```

---

#  Licence

MIT License

---

#  Développeur

FetyMada Team 🇲🇬

Application événementielle moderne pour Madagascar.
