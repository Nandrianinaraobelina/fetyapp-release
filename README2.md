Voici les commandes à exécuter dans votre terminal (à la racine du projet) :
────────────────────────────────────────────────────────────────────────────────


 1. Changer l'icône (logo)
Étape 1 — Préparer votre logo
Placez votre nouveau fichier image dans le dossier  assets/ , par exemple :
assets/mon_logo.png
> Format recommandé : PNG, 1024×1024 px minimum, fond transparent.



Étape 2 — Mettre à jour  pubspec.yaml 
// yaml
flutter_launcher_icons:
  android: true
  ios: false
  image_path: "assets/mon_logo.png"   # ← ici


  
Étape 3 — Lancer la génération
// bash
flutter pub get
dart run flutter_launcher_icons


────────────────────────────────────────────────────────────────────────────────



 2. Changer le nom
Après avoir modifié les fichiers listés précédemment ( AndroidManifest.xml ,  Info.plist , etc.), exécutez :

// bash
# Nettoyer le cache
flutter clean
 
# Réinstaller les dépendances
flutter pub get
 
# Reconstruire l'application
flutter run



────────────────────────────────────────────────────────────────────────────────


3. Changer l'image du splash screen (optionnel)
Dans  flutter_native_splash.yaml  :
// yaml
flutter_native_splash:
  color: "#000000"
  color_dark: "#000000"
  image: assets/mon_splash.png    # ← si vous voulez une image
  android_gravity: center
  ios_content_mode: center
  web: false
Puis :
// bash
dart run flutter_native_splash:create


────────────────────────────────────────────────────────────────────────────────


Résumé des commandes essentielles
┌───────────────────────────────┬───────────────────────────────────────┐
│ Action                        │ Commande                              │
├───────────────────────────────┼───────────────────────────────────────┤
│  Installer les dépendances    │ flutter pub get                       │
│  Générer les icônes Android   │ dart run flutter_launcher_icons       │
│  Nettoyer le cache            │ flutter clean                         │
│  Lancer l'app                 │ flutter run                           │
│  Mettre à jour le splash      │ dart run flutter_native_splash:create │
└───────────────────────────────┴───────────────────────────────────────
