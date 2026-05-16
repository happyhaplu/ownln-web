# OWNLN — Project Documentation

> **"Own Your Music. Own Your Future."**

---

## What is OWNLN?

OWNLN is a creator-first music and media platform built on a single principle: **artists should own their music, their audience, and the majority of their earnings.** While traditional streaming platforms pay fractions of a cent per stream and take 50–70% of revenue, OWNLN was designed to flip that model entirely.

OWNLN is not just a streaming app. It is a complete creative economy platform where musicians, podcasters, educators, and content creators can distribute, monetize, and grow — all in one place.

---

## The Two User Types

OWNLN serves two distinct audiences, each with a tailored experience:

### 🎧 Fans
- Discover music by mood, genre, and personalized recommendations
- Follow artists and get notified of new releases
- Save tracks, build playlists, purchase music
- Subscribe to artists for exclusive content access
- Participate in the Fanfare community forum
- Browse merch directly from creators

### 🎤 Creators (Artists, Podcasters, Educators)
- Upload tracks, albums, podcasts, and film content
- Earn from 5 distinct revenue streams
- Keep 80–90% of every dollar earned
- Access real-time performance analytics and scoring
- Build direct fan relationships via subscriptions
- Sell merch without managing inventory
- Learn and grow via the Education Center
- Network with other creators and industry professionals

---

## The Creator Revenue Model

OWNLN creators earn from **5 revenue streams simultaneously**:

| Revenue Source     | Description                                              |
|--------------------|----------------------------------------------------------|
| Streaming Royalties| Per-stream payments from free and paid listeners         |
| Fan Subscriptions  | Monthly recurring revenue from Pro Fan subscribers      |
| Track Purchases    | Fans buy individual tracks or albums to own permanently  |
| Merch Sales        | Print-on-demand merchandise sold through creator stores  |
| Ad Revenue Share   | A share of platform ad revenue, distributed to creators  |

**Creator Split: 80–90%.** The platform retains only 10–20% to cover infrastructure and operations.

---

## Fan Membership Tiers

| Feature                            | Free Fan | Pro Fan ($9.99/mo) |
|------------------------------------|----------|--------------------|
| Stream public tracks                | ✓        | ✓                  |
| Follow artists & release alerts     | ✓        | ✓                  |
| Free podcast episodes               | ✓        | ✓                  |
| Fanfare community forum             | ✓        | ✓                  |
| Browse creator merch                | ✓        | ✓                  |
| Exclusive unreleased content        | —        | ✓                  |
| Direct messages with artist         | —        | ✓                  |
| Behind-the-scenes videos            | —        | ✓                  |
| Early access to drops               | —        | ✓                  |
| Name in credits                     | —        | ✓                  |
| Ad-free listening                   | —        | ✓                  |
| Offline downloads                   | —        | ✓                  |

---

## Platform Features

### 1. Music Streaming
Adaptive quality streaming from 128kbps to 320kbps. Background play. Offline mode for Pro subscribers. Global CDN delivery.

### 2. Artist Profiles
Each creator has a public profile page displaying their music, bio, genre tags, stats, merch store, and subscription options.

### 3. Upload & Release Tools
- Upload WAV, FLAC, or MP3 (up to 500MB)
- Tag tracks with genre and mood
- Schedule release dates
- Set pricing: Free Stream, Pay to Download, or Subscriber Only

### 4. Discovery & Search
- Mood-based browsing: Chill, Hype, Late Night, Heartbreak, Focus, Film Score, Soulful
- Genre taxonomy: R&B, Soul, Hip-Hop, Afrobeats, Neo-Soul, Gospel, Jazz, Pop
- Trending algorithm powered by plays, saves, shares, and subscription conversions
- Artist directory with role filtering

### 5. Podcasts & Film
Hierarchical structure:
**Show → Season → Episode → Episode Detail**
- Each show has multiple seasons
- Episodes are tagged Free or Pro
- Fans can preview clips before subscribing

### 6. Fan Subscriptions
Artists set a monthly subscription price. Fans choose Free or Pro. 80% of every subscription goes directly to the artist.

### 7. Merch Store
Print-on-demand integrated store. Artists upload designs, set prices. No inventory required. OWNLN handles fulfillment.

### 8. Creator Dashboard (Performance Score)
- Real-time Performance Score (0–100)
- Revenue breakdown by source
- Audience growth metrics
- Top-performing tracks
- 80/20 split visualized

### 9. Wallet & Payouts
- Total earnings tracked across all 5 sources
- Pending vs. paid-out balance
- Transaction history with source labels
- Stripe Connect payout integration

### 10. Education Center
- Free courses: Music Business Basics, Marketing for Indie Artists, Community Building
- Pro courses: Sync Licensing Masterclass, Templates & Contracts Library, Growth Analytics Playbook
- Progress tracking per course

### 11. Community

**Fanfare Forum**
Fan-led discussion threads, creator interaction, playlist sharing, release hype.

**Networking Directory**
Artists, producers, engineers, A&Rs, and managers listed with role tags, genre focus, and availability status. Role-filtered browsing.

**Collaboration Board** (Creator only)
Post open projects and find creative partners.

---

## Discovery System

OWNLN's discovery is built on three layers:

1. **Mood Tags** — For You, Chill, Hype, Late Night, Heartbreak, Focus, Film Score, Soulful
2. **Genre Taxonomy** — R&B, Soul, Hip-Hop, Afrobeats, Neo-Soul, Gospel, Jazz, Pop
3. **Trending Algorithm** — Weighted by plays, saves, shares, and subscription conversions

---

## Why OWNLN is Different

| Traditional Platforms | OWNLN |
|-----------------------|-------|
| 50–70% platform cut   | 10–20% platform cut |
| No direct fan connection | Direct fan subscriptions |
| One revenue stream (streaming) | 5 revenue streams |
| Opaque analytics | Real-time Performance Score |
| Artist owns nothing | Artist owns their masters |
| No education tools | Built-in Education Center |
| No networking | Professional Networking Directory |

---

## Prototype Technical Stack

- **React 18** (CDN, no build tools)
- **Babel Standalone** (JSX transpilation in-browser)
- **Single HTML file** — `ownln_web/index.html`
- **Design**: `#0A0A0A` dark background, `#D4AF37` gold accent, cinematic aesthetic
- **Architecture**: State-driven routing via `React.useState`, role-aware screens

## GitHub Repository

`https://github.com/happyhaplu/ownln-web`

---

*OWNLN — Built for the creators who refused to wait for permission.*
