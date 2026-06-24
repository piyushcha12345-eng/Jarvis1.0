JARVIS AI Assistant — Project Description
This is a Django-based AI chatbot inspired by Iron Man's JARVIS, powered by the Groq API (using the LLaMA 3.1 8B model). Here's a breakdown:

What It Does
A web-based AI assistant that accepts both text and voice input, processes commands through an LLM, responds in text, and speaks the answer aloud using the browser's text-to-speech engine.

Tech Stack
LayerTechnologyBackendDjango (Python)AI ModelGroq API — LLaMA 3.1 8B InstantDatabaseSQLite (via Django ORM)FrontendHTML, CSS, Vanilla JSVoice I/OWeb Speech API (input + output)Configpython-dotenv for API key management

Key Features

Bilingual support — responds in Hindi or English based on user input
Voice input via microphone, voice output via browser TTS
Chat history stored in a database through the ChatHistory model
Two UI versions — a basic version and an advanced Iron Man HUD-style interface with arc reactor animation, radar sweep, waveform visualizer, event log, and system stats display
JARVIS persona — the AI is instructed to always address the user as "Sir" and keep responses concise


How It Works

User types or speaks a command
Frontend sends a POST request to /ask/
Django view checks for simple greetings locally, otherwise forwards to Groq API
Response is saved to the database, returned as JSON, displayed in chat, and spoken aloud
