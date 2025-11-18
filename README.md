🎧 MoodPlay AI Agent

This Capstone Project is part of the 5-Day AI Agents Intensive Course with Google (Nov 10 - 14, 2025)

By: Maisura Jariwala

Project Overview:

MoodPlay is an intelligent multi-agent system that recommends music playlists based on a user’s mood. It understands natural language, infers emotional state, and dynamically provides a curated playlist using Spotify API or a fallback CSV dataset. This system leverages Google’s Gemini 2.5 Flash model and demonstrates Agent-to-Agent (A2A) communication between a front-facing Gemini agent and a backend NotebookLM-style agent.

Problem Statement:

Music is one of the most powerful emotional outlets. But how do we personalize music discovery based not just on genre, but on how a person feels? MoodPlay addresses the challenge of context-aware, real-time music curation using agent intelligence.

Key Features:

Mood Understanding via Gemini API

A2A Communication: Gemini agent delegates mood inference to a sub-agent (NotebookLM-style)

Live Spotify Playlist Recommendations

Fallback to CSV dataset when API fails

Memory + Context Engineering: Previous moods are stored to make the agent empathetic

Observability: Logs and print statements track mood interpretation and tool usage

Agent Evaluation: Logged inputs, fallbacks, and responses are tracked for reliability testing


Agent Architecture:

A --> [User Prompt] --> B[Gemini Agent (Gemini 2.5 Flash)]

B --> C[Notebook Agent (Sub-Agent)]

C --> D[Tool: match_song_by_mood()]

D --> E[Spotify API / CSV Dataset]

E --> D

D --> C

C --> B

B --> F[Final Response to User]


Run Locally (Kaggle or Colab)
1. Clone This Repo

git clone https://github.com/Maisuraa/moodplay-agent

cd moodplay-agent-capstone

2. Setup Environment

pip install -r requirements.txt

3. Add API Keys

   
Add your keys to Kaggle/Colab Secrets or create a .env file with:

SPOTIFY_CLIENT_ID=your_id

SPOTIFY_CLIENT_SECRET=your_secret

GOOGLE_API_KEY=your_gemini_key

Submission Requirements Met:


Features Implemented:

LLM Agent (Gemini)            ✅

Sub-agent (NotebookLM style)  ✅

Tools (Spotify, CSV)          ✅

Memory / Context Engineering  ✅

A2A Protocol                  ✅

Observability (Logs/Prints)   ✅

Gemini Use                    ✅

Inline Documentation          ✅

Kaggle Notebook               ✅

GitHub Repo                   ✅

Deployment Ready (mocked)     ✅ 


Credits & Acknowledgements:

Google & Kaggle GenAI Agent Course Team

Spotipy: Python client for Spotify Web API

Gemini API by Google

Dataset: [MoodyLyrics4Q Dataset (Creative Commons)]


Contact:

https://www.linkedin.com/in/maisura/

https://github.com/Maisuraa
