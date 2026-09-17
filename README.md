# 🌤️ WeatherApp

A native Android weather app built in **Java**, with a Sinhala-language UI, powered by the free [Open-Meteo](https://open-meteo.com/) API (no API key required).

## Features

- 🔍 **City search** — search any city worldwide (type in English; results in Sinhala UI)
- 📍 **Current location** — auto-detects device location for instant local weather
- 🌡️ **Current conditions** — temperature, feels-like, humidity, wind speed, pressure
- ⏱️ **Hourly forecast** — next 12 hours
- 📅 **7-day forecast** — daily highs and lows
- 🎨 **Weather-based background theme** — background gradient changes with time of day and weather condition
- 🔄 **Pull-to-refresh** — swipe down to reload the current city's weather
- 🖼️ **Custom vector weather icons** — sunny, cloudy, rainy, snowy, stormy, foggy, and night variants
- 🌡️ **°C / °F toggle** — switch temperature units, preference is saved
- 🕘 **Recent searches** — quick-access chips for previously searched cities
- 🚀 **Splash screen** — branded loading screen on app launch

## Tech Stack

- **Language:** Java
- **IDE:** Android Studio
- **Min SDK:** 24 (Android 7.0)
- **API:** [Open-Meteo](https://open-meteo.com/) — free, no API key required
  - Geocoding API (city search)
  - Forecast API (current, hourly, daily weather)
- **Storage:** SharedPreferences (unit preference, recent searches)
- **No third-party networking library** — uses plain `HttpURLConnection` + `org.json`

## Project Structure

```
app/src/main/
├── java/com/example/weatherapp/
│   ├── SplashActivity.java   # Launch screen
│   └── MainActivity.java     # Search, location, API calls, UI logic
├── res/layout/
│   ├── activity_splash.xml
│   └── activity_main.xml
├── res/drawable/             # Custom vector weather icons
└── AndroidManifest.xml
```

## Setup

1. Clone this repository
2. Open the project in Android Studio
3. Let Gradle sync complete
4. Run on an emulator or a physical device (internet connection required)

## Permissions

- `INTERNET` — required to fetch weather data
- `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` — optional, used for the "use my location" button

## Notes

- City search input must be typed in **English/Latin script** — Open-Meteo's place database only matches Latin-script names, even though the rest of the UI is in Sinhala.
- No API key or account signup needed — Open-Meteo is free and open.

## License

This project is open for personal and educational use.
