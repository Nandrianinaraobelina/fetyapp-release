# Personnalisation de l'application

Les commandes suivantes doivent être exécutées dans le terminal, à la racine du projet.

---

## 1. Changer l'icône de l'application

### Étape 1 — Préparer votre logo

Placez votre nouvelle image dans le dossier `assets/`.

**Exemple :**

```text
assets/mon_logo.png
```

> **Recommandation :**
>
> - Format : **PNG**
> - Taille minimale : **1024 × 1024 px**
> - Fond : **transparent**

### Étape 2 — Modifier le fichier `pubspec.yaml`

```yaml
flutter_launcher_icons:
  android: true
  ios: false
  image_path: "assets/mon_logo.png"
```

### Étape 3 — Générer les nouvelles icônes

```bash
flutter pub get
dart run flutter_launcher_icons
```

---

## 2. Changer le nom de l'application

Après avoir modifié les fichiers nécessaires (`AndroidManifest.xml`, `Info.plist`, etc.), exécutez les commandes suivantes :

```bash
# Nettoyer le projet
flutter clean

# Installer les dépendances
flutter pub get

# Lancer l'application
flutter run
```

---

## 3. Modifier le Splash Screen *(optionnel)*

Modifiez le fichier `flutter_native_splash.yaml` :

```yaml
flutter_native_splash:
  color: "#000000"
  color_dark: "#000000"
  image: assets/mon_splash.png
  android_gravity: center
  ios_content_mode: center
  web: false
```

Puis générez le nouveau Splash Screen :

```bash
dart run flutter_native_splash:create
```

---

# Résumé des commandes

| Action | Commande |
|---------|----------|
| Installer les dépendances | `flutter pub get` |
| Générer les icônes | `dart run flutter_launcher_icons` |
| Nettoyer le projet | `flutter clean` |
| Lancer l'application | `flutter run` |
| Générer le Splash Screen | `dart run flutter_native_splash:create` |

---

> **Remarque :**
>
> Après toute modification du nom de l'application, de l'icône ou du Splash Screen, il est recommandé d'exécuter :
>
> ```bash
> flutter clean
> flutter pub get
> flutter run
> ```
>
> afin de s'assurer que les changements sont correctement pris en compte.
