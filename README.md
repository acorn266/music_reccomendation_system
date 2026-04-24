# Music Recommender System

A reinforcement learning-based music recommendation system that learns your taste over time using feature-based preferences, mood detection, and skip simulation.

## Features

- **Mood-based recommendations** — select your current mood (Happy, Sad, Energetic, Calm) to influence suggestions
- **Preference learning** — rate songs and the system updates your profile in real time
- **Greedy epsilon exploration** — balances recommending familiar vs. discovering new songs
- **Skip simulation** — simulates skips for low-utility songs and refines your playlist
- **Popularity scoring** — factors in song popularity alongside personal taste
- **Profile visualization** — bar chart comparing your taste profile vs. the recommended playlist

## How It Works

1. Register as a user
2. Select your mood and preferred music features (genre, decade, style)
3. Rate a set of songs to bootstrap your profile
4. Receive a 10-song playlist
5. The system simulates skips and refines a second playlist based on what it learned

## Setup

```bash
pip install pandas numpy matplotlib
```

Make sure `songs.csv` is in the same directory as the script. The CSV must include columns for all 21 features:
(1980s), (1990s), (2000s), (2010s), (2020s),
Pop, Rock, Country, Folk, Dance, Grunge,
Love, Metal, Classic, Funk, Electric,
Acoustic, Indie, Jazz, SoundTrack, Rap

Plus: `Title`, `popularity` (optional — auto-generated if missing)

## Usage

```bash
python recommender.py
```

Follow the prompts to register, select a mood, pick features, and rate songs.

## Project Structure
├── recommender.py   # Main script
└── songs.csv        # Song dataset with feature vectors

## Tech Stack

- Python 3
- pandas, numpy
- matplotlib
