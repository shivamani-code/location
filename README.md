# 📍 Location – Emergency Location Sharing

A minimal web page that lets a user share their current GPS location with one tap, built as the front end for an emergency location-sharing flow.

🔗 **Live demo:** https://location-henna-ten.vercel.app

## ✨ How It Works

1. The user taps **Share My Location**.
2. The browser's Geolocation API asks for permission and reads the current latitude/longitude.
3. The coordinates are sent as JSON (`{ "lat": ..., "lng": ... }`) in a `POST` request to a backend endpoint.
4. A confirmation alert is shown.

> ⚠️ The backend URL in `index.html` is a placeholder (`https://your-backend.com/location`). Point it at your own API to actually receive locations.

## 🛠️ Tech Stack

- HTML5
- Vanilla JavaScript
- Browser Geolocation API + Fetch API

## 📁 Project Structure

```
location/
└── index.html   # Page, button and location-sharing script
```

## 🚀 Run Locally

```bash
git clone https://github.com/shivamani-code/location.git
cd location
npx serve .
```

Open the local URL in your browser. Note: browsers only allow geolocation on `https://` or `localhost`.

## 🔧 Configure

In `index.html`, replace `https://your-backend.com/location` with your endpoint. It should accept:

```json
POST /location
Content-Type: application/json

{ "lat": 17.385, "lng": 78.4867 }
```
