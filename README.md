# Budget Tracker (PWA)

A progressive web app for tracking spending and income. Add or subtract funds, see a running total and a chart of your balance over time, and keep working offline: transactions entered without a connection are saved in IndexedDB and uploaded when you're back online.

**Live demo: https://tferg7.github.io/pwabudgettracker/**
The demo runs without a server, so transactions are stored only in your browser.

## Features

- Add and subtract transactions with a running total and balance chart (Chart.js)
- Works offline: a service worker caches the app and the latest data
- Offline entries are queued in IndexedDB and synced to MongoDB once, when the connection returns
- Installable on phones and desktops (web app manifest)

## Tech

Node.js · Express · MongoDB · Mongoose · Service Worker · IndexedDB · Chart.js

## Run the full app locally

1. Install Node.js and run MongoDB locally (or set `MONGODB_URI` to a MongoDB Atlas connection string).
2. `npm install`
3. `npm start`, then open http://localhost:3006

To test offline mode, open DevTools → Network → Offline, add a transaction, then go back online.
