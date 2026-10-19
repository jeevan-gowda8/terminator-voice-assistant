<p align="center">
  <img src="terminator-logoo.png" width="140" alt="Terminator logo" />
</p>

<h1 align="center">Terminator — Desktop Voice Assistant</h1>

<p align="center">
  A Python voice assistant for Windows that listens for commands, understands them with NLP,
  and controls your apps, music, system and the web — with a live Tkinter console.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python 3.9+" />
  <img src="https://img.shields.io/badge/NLP-spaCy-09A3D5?style=flat-square" alt="spaCy" />
  <img src="https://img.shields.io/badge/Speech-SpeechRecognition%20%2B%20pyttsx3-555?style=flat-square" alt="Speech" />
  <img src="https://img.shields.io/badge/GUI-Tkinter-555?style=flat-square" alt="Tkinter" />
  <img src="https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square&logo=windows&logoColor=white" alt="Windows" />
</p>

---

## Features

| Area | What you can say / do |
|---|---|
| **Apps** | "open chrome", "launch notepad", "close spotify" — finds installed apps by name |
| **Music** | "play &lt;song&gt;" from your local music folder, or on YouTube; pause, resume, stop |
| **Web** | Open YouTube / Google, search online, Wikipedia summaries |
| **Info** | Time, date, weather for a city, news headlines |
| **System** | CPU, RAM and battery status, volume up / down / mute, screenshot, clipboard |
| **Messaging** | Send an email, send a WhatsApp message (desktop app) |
| **Productivity** | Save notes, set reminders, tell a joke |
| **Power** | Shut down, restart or log off the PC by voice |
| **Images** | Generate an image from a text prompt (via Replicate) |
| **Wake word** | Optional hands-free wake word via Picovoice Porcupine |

## Tech stack

- **Speech:** `SpeechRecognition` (listening) and `pyttsx3` (talking)
- **Language understanding:** `spaCy`, `dateparser`
- **GUI:** `Tkinter` console with status and chat log
- **System control:** `psutil`, `pycaw` (Windows volume), `pygame` (local music)
- **APIs (optional):** OpenWeather, NewsAPI, Wikipedia, Replicate (image generation)

## Getting started

```bash
git clone https://github.com/jeevan-gowda8/Terminator-Desktop-Assisant.git
cd Terminator-Desktop-Assisant
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python -m spacy download en_core_web_sm
python terminator.py
```

### Configuration (optional)

Create a `.env` file next to `terminator.py`. Every key is optional — features that need a missing key are simply skipped.

```env
OPENWEATHER_API_KEY=your_key
NEWS_API_KEY=your_key
PICOVOICE_ACCESS_KEY=your_key      # wake word
REPLICATE_API_TOKEN=your_token     # image generation
EMAIL_ADDRESS=you@example.com
EMAIL_APP_PASSWORD=your_app_password
MUSIC_DIR=C:\Users\you\Music
```

> Never commit your `.env` file — it contains private keys.

## Author

**Jeevan Gowda A V** — IoT & Software Developer
[GitHub](https://github.com/jeevan-gowda8) · [LinkedIn](https://www.linkedin.com/in/jeevan-gowda8)
