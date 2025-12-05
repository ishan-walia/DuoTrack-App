# 🚀 DuoTrack – Real-Time Live Location Tracker App

DuoTrack is a simple 2-person real-time GPS tracking application built using:

- Kotlin  
- Google Maps SDK  
- Fused Location Provider API  
- Firebase Realtime Database  
- Foreground Location Service  

This app allows two users to create or join a **Room ID** and track each other’s live location smoothly.

## ⭐ Features

### 🛰 Real-Time Tracking  
- Location updates every 2–5 seconds  
- Smooth Google Maps camera animation  
- Live movement tracking  

### 🔐 No Login System  
- No email / password  
- Just enter **Room ID** and start tracking  

### 🔄 Background Tracking  
- Works when app minimized  
- Works when screen locked  
- Foreground service ensures reliability  

### 📍 Map Features  
- Marker animation  
- Auto-update  
- Clean UI  
- Handles both User A and User B  

### 🔁 Auto Restart  
- App automatically resumes tracking after reboot  
- Uses BootReceiver  

## 🧱 Tech Stack

| Component        | Technology Used |
|------------------|------------------|
| Language         | Kotlin           |
| Maps             | Google Maps SDK  |
| Backend Database | Firebase Realtime Database |
| Location         | Fused Location Provider |
| Background Work  | Foreground Service |

## 📲 How DuoTrack Works

### 1️⃣ Create a Room  
User A taps **Create Room** → App generates code like:  
```
AB123
```

### 2️⃣ Join Room  
User B enters the same room ID → Tracking starts.

### 3️⃣ Both users see each other’s live location on Google Maps.

## 📁 Project Structure

```
app/
 ├── java/com/example/duotrack/
 │     ├── MainActivity.kt
 │     ├── MapActivity.kt
 │     ├── LocationService.kt
 │     ├── BootReceiver.kt
 │     └── model/LocationData.kt
 │
 └── res/
       ├── layout/
       │     ├── activity_main.xml
       │     ├── activity_map.xml
       │     └── activity_room_created.xml
       ├── drawable/
       │     ├── trackerduo.png
       │     ├── ic_location.png
       │     └── input_bg.xml
       └── values/
             ├── colors.xml
             ├── styles.xml
             └── strings.xml
```

## 🔧 Setup Instructions

### ✔ Step 1 — Clone the Repository
```bash
git clone https://github.com/yourusername/DuoTrack.git
```

### ✔ Step 2 — Add Firebase  
- Go to Firebase Console  
- Create new project  
- Add Android app  
- Use package name:  
```
com.example.duotrack
```
- Download `google-services.json`  
- Place it inside:

```
app/google-services.json
```

### ✔ Step 3 — Add Google Maps API Key  
In `AndroidManifest.xml`:

```xml
<meta-data
    android:name="com.google.android.geo.API_KEY"
    android:value="YOUR_API_KEY_HERE" />
```

## 🗄 Firebase Database Structure

```json
{
  "rooms": {
    "AB123": {
      "userA": { "lat": 31.12345, "lng": 76.98765 },
      "userB": { "lat": 31.12456, "lng": 76.98876 }
    }
  }
}
```

## 🔐 Required Permissions

```xml
ACCESS_FINE_LOCATION  
ACCESS_COARSE_LOCATION  
ACCESS_BACKGROUND_LOCATION  
FOREGROUND_SERVICE  
POST_NOTIFICATIONS  
INTERNET  
```

## 👨‍💻 Developer

**Ishan Walia**  
- GitHub: https://github.com/ishanwalia7579  
- LinkedIn: https://www.linkedin.com/in/ishanwalia/  

## ⭐ If you like this project
Don’t forget to **Star ⭐ the repo!**
