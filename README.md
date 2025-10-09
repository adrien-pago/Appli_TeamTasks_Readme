# TeamTasks - Application de Gestion de Tâches

## 📱 Application Mobile Flutter + 🌐 API Symfony

### Description
Application mobile de gestion de tâches avec synchronisation cloud, notifications push et intégration Google Calendar.

### Architecture du Projet

```
Appli_TeamTasks/
├── mobile/                 # Application Flutter
│   ├── lib/
│   │   ├── models/         # Modèles de données
│   │   ├── services/       # Services API et logique métier
│   │   ├── providers/      # Gestion d'état (Provider/Riverpod)
│   │   ├── screens/        # Écrans de l'application
│   │   ├── widgets/        # Widgets réutilisables
│   │   ├── styles/         # Thèmes et styles
│   │   └── utils/          # Utilitaires
│   ├── assets/             # Images, icônes, etc.
│   └── pubspec.yaml
├── api/                    # API Symfony
│   ├── src/
│   │   ├── Controller/     # Contrôleurs API
│   │   ├── Entity/         # Entités Doctrine
│   │   ├── Repository/     # Repositories
│   │   ├── Service/        # Services métier
│   │   ├── DTO/            # Data Transfer Objects
│   │   └── Security/       # Authentification et sécurité
│   ├── config/             # Configuration
│   └── composer.json
└── docs/                   # Documentation
```

### Fonctionnalités

#### Mobile (Flutter)
- ✅ To-do list avec états (à faire, en cours, terminé)
- 🛒 Création de listes de courses
- 📊 Historisation en BDD
- 🔔 Notifications push
- 📅 Agenda intégré avec Google Calendar

#### API (Symfony)
- 🔐 Authentification JWT
- 📝 CRUD tâches et listes
- 📚 Gestion historique
- 🔄 Synchronisation Google Calendar
- 📱 Notifications Firebase

### Technologies
- **Frontend**: Flutter, Provider/Riverpod
- **Backend**: Symfony 6+, Doctrine, JWT
- **Base de données**: MySQL
- **Notifications**: Firebase Cloud Messaging
- **Agenda**: Google Calendar API

### Installation

#### Mobile
```bash
cd mobile
flutter pub get
flutter run
flutter run -d chrome
flutter run -d chrome --web-port=52218
# Activer le support web
flutter create . --platforms=web
// ...existing code...
IconB// ...existing code...
IconB// ...existing code...
IconButton(
  icon: Icon(Icons.arrow_back),
  onPressed: () {
    Navigator.pushNamed(context, '/'); // Retourne à la Home
  },
),
// ...existing code...
```

#### API
```bash
cd api
composer install
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
php bin/console server:start
```

### Configuration
1. Configurer les variables d'environnement
2. Configurer Firebase pour les notifications
3. Configurer Google Calendar API
4. Configurer la base de données MySQL

# Build la nouvelle APK :
cd mobile
flutter clean
flutter pub get
flutter build apk --release

