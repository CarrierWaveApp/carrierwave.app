---
title: "Tours & Onboarding"
description: "Intro tour, mini-tours, logger guide, and first-run onboarding flow"
weight: 1
showToc: true
---

Carrier Wave includes guided tours and an onboarding flow to help new users get started quickly and discover features they might otherwise miss.

## Onboarding Flow

### First Launch

When you open Carrier Wave for the first time, a step-by-step onboarding flow guides you through initial setup:

#### Step 1: Callsign

- **Enter your callsign** - Primary operating callsign
- **Auto-lookup** - Carrier Wave queries QRZ to verify and fetch your name, QTH, and grid square
- **Skip option** - You can skip and enter your callsign later in Settings

#### Step 2: QRZ Connection

- **Connect to QRZ** - Enter your QRZ username and password
- **Benefits explained** - Callsign lookups, logbook sync, QSL confirmations
- **Skip option** - QRZ is recommended but not required

#### Step 3: Service Connections

Connect to additional services (all optional):

- **POTA** - For park activation uploads
- **Ham2K LoFi** - For cross-device sync
- **LoTW** - For confirmation downloads
- **Club Log** - For bidirectional sync
- **eQSL** - For electronic QSL cards

Each service shows a brief description of what it provides. Tap to configure or skip to continue.

#### Step 4: Activity Programs

Select which activity programs you participate in:

- **POTA** (Parks on the Air)
- **SOTA** (Summits on the Air)
- **WWFF** (World Wide Flora & Fauna)
- **Contests**

Selected programs enable program-specific features throughout the app (session types, spot sources, map layers).

#### Step 5: Community Features

Opt in to community features:

- **Enable community** - Registers your callsign with the activities server
- **Privacy explanation** - What data is shared and how it's used
- **Skip option** - Community features can be enabled later

#### Step 6: Ready to Go

- **Summary** of configured services and features
- **Start logging** button to open the Logger
- **Take the tour** button to begin the intro tour

### Returning Users

If you reinstall Carrier Wave or set it up on a new device:

- iCloud sync restores your settings and QSO database
- Service credentials need to be re-entered (stored in device Keychain)
- The onboarding flow detects existing data and skips completed steps

## Intro Tour

The intro tour provides a guided walkthrough of Carrier Wave's main features. It's offered after onboarding and accessible anytime from **Settings -> Help -> Take the Tour**.

### Tour Stops

The intro tour visits each major area of the app:

1. **Dashboard** - Activity grid, statistics, streaks, service status
2. **Logger** - Starting a session, callsign entry, commands
3. **Logs** - Searching contacts, session browsing
4. **Spots** - POTA spots, RBN, P2P opportunities
5. **Map** - QSO visualization, park boundaries
6. **Activity** - Friends, challenges, achievements
7. **Settings** - Key configuration options

Each stop highlights the most important features with:

- **Spotlight overlay** pointing to the relevant UI element
- **Brief explanation** (1-2 sentences)
- **Next/Skip/Done** navigation

### Tour Duration

The full intro tour takes approximately 2-3 minutes. You can skip at any point and resume later.

## Logger Tour with KI5GTR Guide

The Logger tour provides an in-depth walkthrough of the logging interface, guided by KI5GTR (the Carrier Wave developer's callsign):

### Tour Content

KI5GTR walks you through a simulated QSO:

1. **Starting a session** - Session wizard, mode/frequency selection
2. **Callsign entry** - Type a callsign, see the QRZ lookup populate
3. **Quick Entry** - Demonstrate the single-line entry format
4. **RST and fields** - How signal reports and optional fields work
5. **Logging the QSO** - Tap the log button, see the toast confirmation
6. **Commands** - Type `SPOT`, `BAND`, `MAP` to see command system
7. **Session management** - End session, view in Logs tab

### Interactive Elements

The Logger tour uses interactive overlays:

- **Simulated data** populates fields as the tour progresses
- **Animated arrows** point to buttons and fields
- **"Try it yourself"** prompts let you practice each step
- **KI5GTR dialog bubbles** provide context and tips

### Accessing the Logger Tour

- Offered automatically after the first session start wizard
- Available from **Settings -> Help -> Logger Tour**
- Triggered if you tap the **?** icon in the Logger header

## Mini-Tours

Mini-tours are brief, contextual walkthroughs that appear when you first encounter a feature:

### When Mini-Tours Appear

Mini-tours trigger on first use of specific features:

| Feature | Mini-Tour Content |
|---------|------------------|
| **POTA session** | Park entry, spotting, rove mode basics |
| **Activity Log** | Station profiles, quick entry, spot list |
| **CW Transcription** | Audio setup, frequency tracking, auto-fill |
| **FT8 Suite** | Waterfall, decode list, TX control |
| **WebSDR** | Receiver selection, recording, playback |
| **Smart Needs** | Need categories, configuration, alerts |
| **Community** | Friends, challenges, privacy |
| **BLE Radio** | Scanning, pairing, sync behavior |

### Mini-Tour Format

Each mini-tour consists of 3-5 spotlight steps:

1. **Welcome** - Brief description of the feature
2. **Key controls** - Spotlights on the most important UI elements
3. **Quick tip** - One actionable tip for getting the most from the feature
4. **Done** - Dismisses the tour

### Dismissing and Revisiting

- **Dismiss** a mini-tour at any step by tapping "Skip"
- Dismissed tours don't reappear automatically
- **Revisit** any mini-tour from **Settings -> Help -> Feature Tours**
- **Reset all tours** clears the "seen" state for all mini-tours

## Tour Settings

### Settings -> Help

- **Take the Tour** - Start the full intro tour
- **Logger Tour** - Start the Logger-specific tour
- **Feature Tours** - List of all mini-tours with "seen" status
- **Reset All Tours** - Mark all tours as unseen (they'll reappear on next feature use)

### Tour Preferences

- **Show mini-tours** toggle - Disable if you prefer to discover features on your own
- **Tour animation speed** - Normal or Fast for experienced users

## See Also

- [Logger](/reference/logger/) - Full Logger reference
- [Settings & Services](/reference/settings/) - Configuration options
- [Dashboard & Statistics](/reference/dashboard/) - Dashboard features
