@'
# 🎥 AI Video & Meeting Intelligence Assistant

An end-to-end meeting intelligence and media processing platform that transforms raw audio/video content (YouTube URLs or local files) into actionable insights. Powered by Retrieval-Augmented Generation (RAG), local speech-to-text models, and multilingual regional AI models, this application automates transcription, summarization, action item assignment, and contextual Q&A with sub-second latency.

---

## 🌟 Key Features

* **Multi-Format Media Ingestion:** Process local audio/video files or extract audio directly from YouTube URLs.
* **Multilingual Speech Recognition:** 
  * **English:** High-accuracy transcription using local **OpenAI Whisper**.
  * **Regional (Hindi/Hinglish):** High-precision extraction via **Sarvam AI** integration, boosting multilingual accuracy by **35%**.
* **Automated Meeting Intelligence:** Automatically generates structured executive summaries, maps action items to owners, and tracks key business decisions.
* **Context-Aware RAG Engine:** Ask natural-language questions against meeting transcripts powered by **LangChain LCEL**, **ChromaDB**, **HuggingFace Embeddings**, and **Mistral AI** with low response latency (**~300ms**).
* **Export & Analytics:** Export reports into structured PDF/TXT formats with real-time pipeline status tracking built in Streamlit.

---

## 🛠️ Tech Stack & Architecture

* **Frontend & UI:** Streamlit
* **Orchestration & RAG Framework:** LangChain (LCEL - LangChain Expression Language)
* **LLM Engine:** Mistral AI
* **Speech-to-Text (STT):** OpenAI Whisper (Local), Sarvam AI (Regional Hindi/Hinglish)
* **Vector Store:** ChromaDB
* **Embeddings:** HuggingFace Embeddings
* **Environment:** Python 3.10+

---

## 🏗️ System Architecture Workflow

1. **Input Stage:** User provides a YouTube link or uploads a media file (`.mp4`, `.mp3`, `.wav`).
2. **Audio Processing & Transcription:** Audio is extracted and routed to **Whisper AI** or **Sarvam AI** based on language selection.
3. **Indexing:** Transcripts are chunked and embedded into **ChromaDB** using **HuggingFace Embeddings**.
4. **Intelligence Generation:** **Mistral AI** via **LangChain LCEL** generates summaries, action items, and decision logs.
5. **Interactive RAG:** Users query the meeting transcript via an interactive chatbot interface.

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.10 or higher installed, along with `ffmpeg` for audio extraction.

```bash
# Linux / macOS
sudo apt install ffmpeg

# Windows (via Chocolatey)
choco install ffmpeg