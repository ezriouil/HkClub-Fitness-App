<p align="center">
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android">
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin">
  <img src="https://img.shields.io/badge/💳-Payment%20Notify-green?style=for-the-badge" alt="Payment">
</p>

<h1 align="center">💳 HK Club App</h1>
<h3 align="center">Gym / Club – Payment Arrival Notifications</h3>

<p align="center">
  <strong>An Android app for gym or club management. Notifies when a user arrives to pay. Manages clients, tracks payments, and displays notifications for payment arrivals.</strong>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-project-structure">Project Structure</a> •
  <a href="#-screens">Screens</a>
</p>

---

## 📖 Overview

HK Club App helps gym/club staff manage clients and get notified when users arrive to make a payment. It uses a local SQLite database to store client data, RecyclerView for lists, and fragments for Home, Notifications, and User management.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔔 **Payment Notifications** | Notify when a user arrives to pay |
| 👥 **Client Management** | Add, view, and manage clients |
| 💾 **Local Database** | SQLite for offline client data |
| 📋 **RecyclerView Lists** | Efficient list display with DiffUtil |
| 🏠 **Home** | Main dashboard |
| 🔔 **Notifications** | Payment arrival alerts |
| 👤 **User** | User/client details and actions |
| 📱 **Fragment-based UI** | Home, Notification, User screens |
| 🎨 **Screen Animations** | Smooth transitions |

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|------------|
| **Language** | Kotlin |
| **Platform** | Android |
| **Database** | SQLite (Room or raw SQL) |
| **UI** | Activities, Fragments, RecyclerView |
| **List** | DiffUtil for efficient updates |

---

## 🚀 Getting Started

### Prerequisites

- Android Studio (Arctic Fox or newer)
- JDK 8+
- Android SDK (minSdk 21+)

### Installation

```bash
# Clone the repository
git clone https://github.com/ezriouil/hkclubapp.git
cd hkclubapp

# Open in Android Studio
# File → Open → Select project folder

# Sync Gradle
# Build → Sync Project with Gradle Files
```

### Run the App

```bash
./gradlew installDebug

# Or: Run → Run 'app' (Android Studio)
```

---

## 📁 Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/www/ezriouil/gym/
│   │   │   ├── local/
│   │   │   │   ├── model/
│   │   │   │   │   └── Client.kt           # Client data model
│   │   │   │   └── sql/
│   │   │   │       ├── DB.kt               # Database helper/queries
│   │   │   │       └── DataBase.kt         # Database setup
│   │   │   ├── recyclerView/
│   │   │   │   ├── Adapter.kt              # RecyclerView adapter
│   │   │   │   ├── Listener.kt             # Item click listener
│   │   │   │   ├── MyArrayAdapterForListView.kt
│   │   │   │   ├── MyDiffUtil.kt           # DiffUtil for list updates
│   │   │   │   ├── ViewHolder.kt
│   │   │   │   └── ViewHolder.kt
│   │   │   ├── ui/
│   │   │   │   ├── activity/
│   │   │   │   │   ├── MainActivity.kt     # Main activity
│   │   │   │   │   └── ScreenAnim.kt       # Screen animations
│   │   │   │   └── fragment/
│   │   │   │       ├── Home.kt             # Home screen
│   │   │   │       ├── Notification.kt     # Payment notifications
│   │   │   │       └── User.kt             # User/client screen
│   │   │   └── res/
│   │   ├── AndroidManifest.xml
│   │   └── ...
│   ├── androidTest/
│   │   └── java/www/ezriouil/hkclubapp/
│   └── test/
├── build.gradle
├── ic_launcher-playstore.png
└── proguard-rules.pro
```

---

## 📱 Screens

| Screen | Fragment | Description |
|--------|----------|-------------|
| **Home** | `Home.kt` | Main dashboard |
| **Notifications** | `Notification.kt` | Payment arrival alerts |
| **User** | `User.kt` | Client/user details |

---

## 📦 Key Components

| File | Description |
|------|-------------|
| `Client.kt` | Client model (name, payment status, etc.) |
| `DB.kt` | Database operations |
| `DataBase.kt` | SQLite database setup |
| `Adapter.kt` | RecyclerView adapter for client list |
| `MyDiffUtil.kt` | Efficient list diffing |
| `Listener.kt` | Item click/listener callbacks |
| `MainActivity.kt` | Host activity for fragments |
| `ScreenAnim.kt` | Transition animations |
| `Home.kt` | Home fragment |
| `Notification.kt` | Payment notification fragment |
| `User.kt` | User/client fragment |

---

## 💳 Payment Flow

```
User arrives to pay
        │
        ▼
   App detects / logs
        │
        ▼
 Notification shown
        │
        ▼
  Staff can confirm
   payment received
```

---

## 🔒 Package

**Application ID:** `www.ezriouil.hkclubapp` / `www.ezriouil.gym`

---

## 📄 License

MIT License

---

## 👤 Author

**Mohamed Ezriouil**
- GitHub: [@ezriouil](https://github.com/ezriouil)

---

<p align="center">⭐ Star this repo if you find it helpful!</p>
