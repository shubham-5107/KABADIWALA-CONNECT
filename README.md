# Kabadiwala Connect — Prototype

A mobile-first, multilingual (English / हिन्दी / मराठी) prototype that connects informal e-waste collectors (*kabadiwalas*) with certified recyclers. Collectors log a lot of e-waste with a photo, get an instant price estimate, and hand it over to a verified recycler, with a tamper-evident handover record at every step.

## Features

- **Collector app:** photo capture, material category, weight and condition, instant price estimate
- **Offline-first:** lots are queued locally when offline and marked *"Queued — will sync"*
- **Recycler portal:** view incoming lots, make an offer, confirm handover, mark as paid
- **Handover record:** unique reference ID, timestamp, GPS location and a 5-step status tracker
- **Live market prices:** per-kg rates with up/down trend indicators
- **Safety tips** with text-to-speech (*Listen* button) for low-literacy users
- **3 languages:** English, Hindi, Marathi
- **Demo controls:** switch between Collector and Recycler views and reset demo data

## Tech stack

Plain HTML, CSS and vanilla JavaScript in a single file. No build step, no dependencies.

- `localStorage` for data (simulates a shared backend)
- Web Speech API for audio tips
- Geolocation API for handover location
- Google Fonts (Noto Sans / Noto Sans Devanagari)

## Run locally

```bash
git clone https://github.com/shubham-5107/kabadiwala-connect.git
cd kabadiwala-connect
# just open index.html in a browser, or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Project structure

```
kabadiwala-connect/
├── index.html                  # entire app (HTML + CSS + JS)
├── README.md
├── LICENSE
├── .gitignore
├── RESOURCES
    ├── Monitors.jpg
    ├──pcb.jpg
    
```

## Prototype limitations

- Data lives in the browser's `localStorage`; there is no real backend or authentication.
- The recycler (*GreenLoop Recyclers*), CPCB number and market prices are demo placeholders.
- Payments are simulated (status change only).


## Contributing

Issues and pull requests are welcome. Please open an issue first to discuss major changes.

## Author
• Shubham Sharma
• Sachin Choudhary
• Pooja Mehra
• Siddhant Mishra
• Ragini
• Yashika Shirvastav
