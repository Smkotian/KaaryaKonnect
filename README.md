
# KaaryaKonnect
KaaryaKonnect is an offline worker–employer connect platform designed for daily wage workers in Karnataka.
The system operates entirely through Kannada voice interaction, making job discovery and registration natural, accessible, 
and barrier-free for all workers—even those with low literacy, limited smartphone access, or regional language preference.

---

## Features

### Employers Portal (`employers.html`)

* Employers post their requirements:

  * Skills needed
  * Location of work
  * Wages offered

---

### Worker Voice Transcription (transcription.ipynb)

* Workers speak directly in **Kannada**.
* Uses **[`vasista22/whisper-kannada-small`](https://huggingface.co/vasista22/whisper-kannada-small)** for transcription.
* Extracts structured details:

  * Name
  * Location
  * Skills
  * Experience
  * Expected wages

---

### Job Matching Algorithm (jobmtching_algo.ipynb)

* Uses **Indic-transliteration** to translate Kannada → English.
* Matches workers and employers based on:

  * Skills
  * Location
  * Wage expectations(within a range of +/- 500)

---

### Offline-Friendly (Twilio Integration)

* SMS and Voice call support via **Twilio**.
* Ensures workers can access opportunities even **without internet**.

---

### Tech Stack

Backend: Python, Flask

Voice Processing: HuggingFace Transformers (Whisper customised – vasista22/whisper-kannada-small)

Telephony / SMS: Twilio, Twilio REST API

Realtime Database: Firebase Realtime Database, firebase-sdk-admin

Tunneling: pyngrok (for exposing local Flask server)

Frontend: HTML/CSS (Flask-rendered dashboard)/Javascript

## Why KaaryaKonnect?

* **Workers** → Kannada-first, voice-based, offline-friendly.
* **Employers** → Simple and fast way to hire the right workers.
* **Community** → Bridges the gap between daily wage earners and opportunities.


