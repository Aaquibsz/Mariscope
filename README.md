# Mariscope · Marine Debris Intelligence

Demo / illustrative marine debris monitoring dashboard for the Indian west coast (Goa / Maharashtra region).

Single-file web app: `UIUX.html`

> All data is simulated. No live satellite, radar, vessel, or sensor feed is connected.

## Features

- **Map view** – geographic intelligence with simplified coastline, monitoring range, debris locations
- **Radar view** – tactical detection sweep with range rings
- **Drift prediction** – constant-velocity model (+6h / +12h / +24h), accumulation zone, landfall estimate
- **Risk identification** – High / Medium / Low per detection
- **Recovery Plan** – Detect → Locate → Predict Drift → Identify Risk → Plan Recovery
- **Filtering** – by Plastic, Fishing Net, Debris Cluster, Container/Debris, Unknown Debris
- Live-updating KPIs: active detections, high-risk count, nearest debris

## How to Run

No install, no build, no dependencies. Just a browser.

### Option 1 – Double-click (easiest)

1. Open this folder in File Explorer:
   `C:\Users\aamir\OneDrive\Desktop\Mariscope`
2. Double-click `UIUX.html`
3. It opens in your default browser.

### Option 2 – VS Code Live Server

1. Open the folder in VS Code
2. Right-click `UIUX.html` → **Open with Live Server**

### Option 3 – Python HTTP server

```powershell
cd "C:\Users\aamir\OneDrive\Desktop\Mariscope"
python -m http.server 8000
```

Then open: http://localhost:8000/UIUX.html

### Option 4 – Node.js HTTP server

```powershell
cd "C:\Users\aamir\OneDrive\Desktop\Mariscope"
npx serve .
```

Then open the URL it prints (usually http://localhost:3000/UIUX.html).

## Files

| File | Description |
|------|-------------|
| `UIUX.html` | Entire app – HTML + CSS + JS, no external dependencies |
| `README.md` | This file |

## Notes

- Google Maps tiles are not used. The basemap is a simplified approximate coastline drawn on canvas.
- `GMAPS_KEY` in the source is reserved for self-hosting with Google Maps – leave empty for the demo.
