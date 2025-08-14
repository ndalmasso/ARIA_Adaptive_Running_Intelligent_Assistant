# ARIA - Adaptive Running Intelligent Assistant

## Overview

A Python-based adaptive running coach that dynamically adjusts music and training based on real-time feedback. ARIA combines music science with personalized training zones to create a responsive running companion that adapts to your actual performance and mood, not just predetermined plans.

## "Adaptive Running for Everyone"
Here's how ARIA transforms your running experience through intelligent music curation and real-time adaptation.

### The Problem

Despite the explosion of running apps and wearables, every runner faces the same issues: we're treated like walking statistics. Playlists are static, training plans ignore moods and fatigue, and you get pep talks from a phone that has no clue how you're actually doing.

ARIA fixes three core issues:
- **Static Systems:** Existing apps miss how motivation, energy, and intent fluctuate mid-run
- **Wasted Potential:** Music is treated as background noise instead of a dynamic performance tool  
- **No Learning Loop:** When a session is tough or amazing, there's no way for real-time input to improve future runs

### The Solution

ARIA is an adaptive, music-driven coach that actually cares how your run is going:

- **Personal Profile:** Your stats, goals, and training zones
- **Embedded Training Assistant:** Crafts sessions that fit your goals and current state, not generic averages
- **Instant Feedback Loop:** Voice commands or simple inputs to signal you're dying, thriving, or coasting - ARIA reacts immediately
- **Smart Music Engine:** Songs selected for BPM and energy that match your current performance, nudging you up or down as needed
- **Intent Awareness:** Constantly checks your state and adapts training (speed, recovery, intervals) and music to where you are now

## Demo Experience

The interactive notebook demonstrates ARIA's core functionality:

### Step 1: Personal Setup
Configure your runner profile with basic stats (age, weight, height) to calculate personalized heart rate zones and optimal BPM ranges for each training zone.

### Step 2: Pre-Run Planning  
ARIA analyzes your goals and creates a dynamic session plan, mapping training zones to musical BPM ranges that will guide your workout intensity.

### Step 3: Live Adaptation
During your simulated run, provide real-time feedback:
- **UP** - Feeling strong, ready for higher intensity
- **DOWN** - Need to dial it back, lower the intensity  
- **OK** - Current pace feels right

ARIA instantly adjusts both your training zone and music selection to match your actual state.

### Step 4: Learning & Growth
Post-run feedback helps ARIA learn your patterns and preferences for future sessions.

## Repository Structure

```
├── aria_demo.ipynb                    # Interactive ARIA demonstration
├── demo_video.mp4                     # Visual demonstration of ARIA in action
└── README.md                          # This file
```

## Requirements

```python
numpy>=1.20.0
matplotlib>=3.3.0
ipywidgets>=7.6.0
IPython>=7.0.0
time  # Built-in module
random  # Built-in module
```

## Key Features

**Real-Time Adaptation:**
- Instant response to user feedback during workouts
- Dynamic music BPM adjustment based on training zones
- Flexible session modification without stopping

**Personalized Training:**
- Heart rate zone calculation based on individual characteristics
- BPM mapping to physiological training zones
- Adaptive session planning

**Interactive Experience:**
- Live feedback collection during simulated runs
- Visual progress tracking and zone transitions
- Post-session learning and improvement

## Methods

The system employs:
- **Heart Rate Zone Calculation** using age-based formulas and personal characteristics
- **BPM-to-Zone Mapping** linking musical tempo to physiological training intensities
- **Real-Time Adaptation** through continuous feedback loops
- **Machine Learning Principles** for session optimization based on user responses

## Known Issues

⚠️ **Current Limitations in Demo:**

- **Input Box Persistence:** When the run ends, the live input box "💬 How do you feel? (UP / DOWN / OK):" remains visible even though the session is over. This can cause a crash or force a kernel restart if additional input is attempted.

- **Post-Run Feedback Timeout:** After the run completes, ARIA asks "📝 How was the session overall? (GOOD / OK / BAD):". If no feedback is provided within the 4-second timeout, ARIA correctly skips, but the input box stays active, which can be confusing or cause the UI to hang. This won't kill the kernel but affects user experience.

*These UI/UX issues stem from limitations in standard input mechanisms within Jupyter environments. Solutions would require significant control flow alterations or alternative input frameworks.*

## Expected Impact

What ARIA delivers:
- **Genuine Motivation:** Music dynamically boosts you when needed and eases off when it's "just not your day"
- **True Personalization:** Training sessions flex with you - bad sleep, great mood, unexpected hills, whatever
- **Continuous Learning:** Every run teaches ARIA what works, how you respond, and when to switch tactics
- **Applied Science:** BPM and performance research actually used to improve your runs, not just academic footnotes

## Ideal Implementation

In a production environment, ARIA would integrate with:
- **Music Streaming APIs** (Spotify, Apple Music) for real song selection
- **GPS Tracking** for pace and location data
- **Heart Rate Monitors** for physiological feedback
- **Voice Recognition** for hands-free interaction
- **Machine Learning Models** for advanced personalization

## Why This Matters

Existing apps like Spotify Running and RockMyRun try to match music tempo to pace, but they stop there. None listen to your actual, in-the-moment experience or learn from real feedback. They treat you like every other runner whose training, mood, and music needs are supposedly identical day after day. 

ARIA breaks this mold by being truly responsive: a living, learning companion that evolves with you, not just another app barking timers.

## Getting Started

1. Clone the repository
2. Install requirements: `pip install numpy matplotlib ipywidgets IPython`
3. Open `aria_demo.ipynb` in Jupyter Notebook
4. Run all cells and interact with the demo
5. Watch `demo_video.mp4` for a visual walkthrough

## Future Development

- Integration with real music streaming services
- GPS and heart rate monitor connectivity
- Advanced ML models for preference learning
- Mobile app development
- Social features and training communities

---

**Note**: This is a proof-of-concept demonstration. The core algorithms and interaction patterns are designed for real-world implementation with proper hardware integration and production-grade error handling.

Running is hard. Staying motivated is harder.  
ARIA is the answer to both: an assistant that doesn't hand you a prescription, but gives you a partner.
