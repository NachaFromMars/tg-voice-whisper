# tg-voice-whisper — Offline Telegram voice message transcription

> Transcribe incoming Telegram voice notes (.ogg) locally using OpenAI Whisper. 100% offline, no API keys, auto-deletes audio after transcription.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
tg-voice-whisper watches for Telegram voice messages and transcribes them using Whisper (tiny model) locally. Everything runs on-device — no audio leaves the machine. When a `.ogg` file lands in the inbound folder, the skill runs Whisper, replies with transcription, then auto-deletes the file. ~4GB RAM recommended.

## Features
- 100% offline — no cloud, no API keys
- Whisper tiny model — fast on CPU
- Privacy-first: auto-delete after processing
- Auto-setup: sub-agent or 5s cron loop
- Handles Telegram native `.ogg` Opus format

## Usage / Quick Start
```bash
apt install ffmpeg && pip install openai-whisper
```
When `.ogg` arrives in `/root/.openclaw/media/inbound/` → whisper → reply → rm file.

## Trigger Keywords (OpenClaw)
transcribe voice message, Telegram voice, ogg to text, whisper transcribe, voice message text

## Related Skills
- [tesseract-ocr](https://github.com/NachaFromMars/tesseract-ocr) — image text extraction
- [telegram-offline-voice](https://github.com/NachaFromMars/telegram-offline-voice) — outgoing voice messages

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
