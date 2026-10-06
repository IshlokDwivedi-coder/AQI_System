# 🌿 AeroGemma — Touch Grass with AI-Powered Air Quality

> **Submission for Hacktoberfest Open-Source AI Challenge: Week 1 ("Touch Grass")**  
> **Prize Category Track:** 🏆 **Best Use of Gemma** (Google's Open-Weight Model)  
> **Live GitHub Repo:** [IshlokDwivedi-coder/AQI_System](https://github.com/IshlokDwivedi-coder/AQI_System)  
> **Author:** Ishlok Dwivedi ([@ishlokdwivedicoder](https://dev.to/ishlokdwivedicoder))

---

## 📖 Overview

The theme of this week's Hacktoberfest challenge is **Touch Grass**: build something with open-source AI at its core that gets people away from screens and out into the real world.

While spending time in nature (hiking, running, gardening, birding) is vital for physical and mental health, **poor air quality** (elevated PM2.5, ground-level ozone, and chemical smog) can turn a refreshing outdoor workout into a health hazard—especially for children, older adults, and those with respiratory conditions.

**AeroGemma** solves this dilemma. It is a sleek, intuitive, and responsive web application that fetches real-time atmospheric readings from global monitoring stations and pairs them with **Google's open-weight Gemma model (`gemma-4-26b-a4b-it`)**. 

AeroGemma gives you a clear, instant answer: **"Can I touch grass right now?"** along with tailored activity advice for runners, gardeners, pet owners, and families.

---

## ✨ Features

- 🌿 **"Touch Grass" Instant Verdict:** Clear green/yellow/orange/red gauge and status message showing whether it's safe to head outdoors right now.
- 🤖 **Google Gemma AI Outdoor Advisor:** Real-time atmospheric intelligence powered by Google's open-weight Gemma model that assesses ambient pollutants and generates personalized activity briefings.
- 🏃 **Activity Feasibility Matrix:** Individual suitability indicators for:
  - 🏃‍♂️ Running & High-Intensity Cardio
  - 🌱 Gardening & Planting
  - 🐕 Dog Walking & Nature Trail Hikes
  - 🪁 Children & Playground Sessions
- 📊 **Comprehensive Pollutant Breakdown:** Detailed metrics for **PM2.5**, **PM10**, **Ozone (O₃)**, **Nitrogen Dioxide (NO₂)**, **Sulphur Dioxide (SO₂)**, and **Carbon Monoxide (CO)** compared against World Health Organization (WHO) safety thresholds.
- 📍 **Global Coverage & Geolocation:** Instant 1-click GPS detection or fast search across any city or town worldwide using the Open-Meteo station mesh (free, open, no rate limits).
- 🛡️ **Edge & Offline Fallback Engine:** Features an offline edge rule engine so you can run AeroGemma even when deep in the backcountry or on remote trails with zero cellular service.
- ⚙️ **Customizable Settings Modal:** Easily switch between Gemma models (`gemma-4-26b-a4b-it`, `gemma-4-31b-it`, offline engine) or supply your own Google AI Studio key.

---

## 💡 Why Open Innovation & Gemma Matter

Closed, proprietary AI APIs have significant drawbacks for outdoor recreation and health applications:
1. **Backcountry & Trail Availability:** Closed APIs require continuous cellular internet connectivity. With Gemma's open weights, the model can be deployed locally on a laptop, tablet, or edge device to deliver health recommendations in national parks and remote trails with no signal.
2. **Location & Health Privacy:** Users should not have to upload their precise GPS trail coordinates and personal respiratory vulnerabilities to centralized corporate servers. Open-weight models empower users to keep their data local.
3. **Zero Paywalls & Independence:** Open innovation ensures that community wellness tools remain accessible forever without sudden rate-limit shutoffs or expensive token fees.

---

## 🛠️ Architecture & Tech Stack

```
   ┌─────────────────────────────────────────────────────────┐
   │                     AeroGemma UI                        │
   │           (Vanilla HTML5, Modern CSS3, JS)              │
   └───────────────┬─────────────────────────┬───────────────┘
                   │                         │
                   ▼                         ▼
      ┌─────────────────────────┐ ┌─────────────────────────┐
      │  Open-Meteo Station API │ │ Google Gemma AI Studio  │
      │   (Real-time AQI, PM,   │ │ (gemma-4-26b-a4b-it /   │
      │    Weather, UV Index)   │ │  Offline Edge Engine)   │
      └─────────────────────────┘ └─────────────────────────┘
```

- **Frontend:** Vanilla HTML5, CSS3 (Glassmorphism, CSS Custom Properties for dynamic AQI-state theme shifting, SVG vector rings, responsive grid), Vanilla JavaScript ES6+.
- **AI Core:** Google Gemma (`gemma-4-26b-a4b-it`) accessed via Google AI Studio API with built-in edge rule-based fallback.
- **Environmental Data:** Open-Meteo Air Quality & Weather API (completely open, global coverage, zero API keys required).
- **Backend / Server:** Zero-dependency Node.js HTTP server.

---

## 🚀 Quick Start (Running Locally)

### 1. Clone the repository
```bash
git clone https://github.com/IshlokDwivedi-coder/AQI_System.git
cd AQI_System
```

### 2. Run the application
You can run it using Node.js:
```bash
node server.js
```
or simply double-click and open `index.html` directly in any web browser!

### 3. Open in Browser
Visit `http://localhost:3000` in your browser.

---

## 📸 Screenshots

- **Live AQI & Touch Grass Verdict:** Real-time gauge and status indicating safe outdoor times.
- **Gemma Intelligence Briefing:** Natural-language advice detailing safe windows for running, hiking, and gardening.
- **Pollutant Breakdown:** Detailed micro-metrics for PM2.5, PM10, O3, NO2, SO2, and CO.

---

## 🏆 Hacktoberfest 2026 Submission Details

- **Event:** Hacktoberfest Open-Source AI Challenge: Week 1 (Oct 5 – Oct 11, 2026)
- **Theme:** Touch Grass
- **Partner Prize Category:** Best Use of Gemma ($200 USD)
- **Tags:** `#hf26challenge`, `#devchallenge`
- **Developer:** Ishlok Dwivedi
- **License:** MIT License
