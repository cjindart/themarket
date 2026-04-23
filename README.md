# The Market

A peer-to-peer mobile marketplace app built with Flutter and Firebase. Users can list items for sale, browse and search listings, and message sellers directly — all within the app.

---

## Features

- **Browse listings** — scrollable grid or list view of items posted by other users
- **Search** — Algolia-powered search with category filtering
- **Post items** — upload multiple photos, set a price, pick a category and condition
- **In-app messaging** — real-time chat between buyers and sellers via Firestore
- **User profiles** — view your own listings and manage your account
- **Push notifications** — Firebase Cloud Messaging for message alerts
- **Auth** — email/password sign up and login via Firebase Auth

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| State management | GetX |
| Backend / Database | Firebase Firestore |
| Auth | Firebase Auth |
| File storage | Firebase Storage |
| Search | Algolia (custom HTTP client) |
| Push notifications | Firebase Cloud Messaging |

---

## Project Structure

```
the_market_app/
├── lib/
│   ├── main.dart               # App entry point, route definitions
│   ├── routes.dart             # Named route constants
│   ├── constants.dart          # App-wide constants
│   ├── widgets.dart            # Shared widgets (app bar, nav bar, item cards)
│   ├── model/
│   │   ├── item.dart           # Item model, category/condition enums
│   │   ├── message.dart        # Message model
│   │   ├── algolia.dart        # Algolia search client
│   │   └── appPrefs.dart       # Local preferences (shared_preferences)
│   ├── pages/
│   │   ├── homePage.dart       # Main feed
│   │   ├── itemPage.dart       # Item detail view
│   │   ├── onOpen/             # Splash, login, sign up
│   │   ├── profile/            # Profile, new post flow
│   │   ├── search/             # Search and filtered results
│   │   ├── messaging/          # Messages list and chat
│   │   └── settings/           # Settings, privacy policy, ToS, report user
│   └── services/
│       └── chat/               # Firestore chat service
└── assets/
    ├── images/                 # Category icons and default images
    ├── privacy_policy.txt
    └── terms_of_service.txt
```

---

## Item Categories

Bikes, Electronics, Clothes, Free Items, Furniture, Arts & Crafts, Books, Home Decor, Fashion, Beauty, Appliances, Miscellaneous

## Item Conditions

Brand New, Like New, Semi-Used, Very Used

---

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (Dart SDK `>=3.1.3 <4.0.0`)
- A Firebase project with Firestore, Auth, Storage, and Messaging enabled
- An Algolia account and index for search

### Setup

1. Clone the repo:
   ```bash
   git clone https://github.com/cjindart/themarket.git
   cd themarket/the_market_app
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Add your Firebase config files:
   - `android/app/google-services.json`
   - `ios/Runner/GoogleService-Info.plist`

4. Run the app:
   ```bash
   flutter run
   ```

---

## Platforms

Targets iOS, Android, macOS, Linux, and Web.
