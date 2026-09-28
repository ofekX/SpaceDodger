# 🚀 SpaceDodger (Kotlin / Android)

A five-lane space dodging game built in **Kotlin** for Android.  
Steer your spaceship using **tilt or button controls**, dodge UFOs, collect coins, and compete for a place on the **Top 10 leaderboard**. 🏆  
High scores are saved locally with their locations and displayed on an interactive **Google Map**. 📍

---

## ✨ Features

- 🎮 **Controls**
    - 🧭 Tilt (sensor) mode
    - ⬅️➡️ Button mode
- 👾 **Obstacles**
    - Crashing reduces lives ❤️
- 🪙 **Coins**
    - Collect coins to increase your score
- ❤️ **Lives system**
    - Game ends when lives reach 0
- 🏆 **Top 10 Leaderboard**
    - Only scores that **enter Top-10** prompt for a name ✍️
    - Saved locally using SharedPreferences 💾
- 🗺️ **Map screen**
    - Top half: leaderboard list
    - Bottom half: Google Map
    - Tap a record → map zooms to its saved location 📍

---

## 🧩 Project Structure (High Level)

- `MainActivity` 🎯  
  Runs the game loop, handles crashes/game-over, saves records (with location).

- `LeaderboardActivity` 🏆  
  Hosts the two fragments (table + map).

- `HighScoreFragment` 📋  
  RecyclerView showing Top 10 records.

- `MapFragment` 🌍  
  Google Map + `zoom(lat, lon)` to center camera and move a marker.

---

## ✅ Requirements

- Android Studio
- Min SDK: 26
- Google Play Services (Maps + Location)

---

## 🔑 Google Maps API Key (Required)

This project uses a manifest placeholder (`${MAPS_KEY}`) for the Maps key.

Create / edit the file **`local.properties`** in the **project root** (same folder as `settings.gradle.kts`) and add:

```properties
MAPS_KEY=YOUR_KEY_HERE
