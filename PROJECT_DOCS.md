# OWNLN Project Documentation

## 1) Product Overview
OWNLN is a creator-first entertainment ecosystem designed for independent artists and creators who need direct audience ownership, transparent monetization, and unified workflows.

OWNLN consolidates:
- Music streaming
- Podcast and film/exclusive content
- Fan subscriptions and digital purchases
- Creator analytics (OPI)
- Wallet and payout visibility
- Community layers (Fanfare + Networking)
- Education hub (free + paid resources)
- Merch integration

The product direction is mobile-first with a premium dark cinematic UX language.

---

## 2) Core Value Proposition

### Creator-first economics
- Creator revenue share starts at **80%**.
- Can scale to **90%** for high-performing creators.
- Revenue routing and payout logic are transparent and trackable.

### Unified creator stack
OWNLN replaces fragmented creator workflows spread across separate products (streaming, subscriptions, merch, community, and education) with one integrated platform.

### Direct fan relationships
Subscriptions, purchases, and community interactions happen within the platform without third-party middlemen controlling audience access.

---

## 3) Target Users

### Primary creator ICP
Independent artists with existing fanbases who are underserved by low per-stream payouts and want:
- Better monetization
- Better fan ownership
- Better performance visibility

### Fan users
Fans who want:
- Closer access to creators
- Exclusive releases and behind-the-scenes content
- Community participation

### Industry users
Producers, engineers, managers, and collaborators using networking/community layers.

---

## 4) Product Modules

## 4.1 Accounts, Profiles, Onboarding
- Artist and fan registration flows
- Profile pages (bio, avatar, banner, links)
- Profile editing
- Follow/unfollow relationships
- Public discovery browse

## 4.2 Music Upload & Streaming
- Track + album models
- Upload flow (WAV/MP3)
- Processing pipeline and publish scheduling
- Stream-ready delivery for fan playback

## 4.3 Fan Playback Experience
- Track and album playback
- Background audio behavior
- Session continuity UX
- Like/save and release feed behavior

## 4.4 Artist Dashboard + OPI
- Composite Performance Index (OPI)
- Stream and follower growth visibility
- Revenue and payout split visualization
- Upload/release management surfaces

## 4.5 Search & Discovery
- Full-text search surfaces
- Mood/genre taxonomy
- Trending logic surfaces
- Playlist and favorites flows

## 4.6 Monetization & Wallets
- Free and paid subscription tiers
- Creator wallet balances (pending/paid)
- Payout visibility and ledger views
- Gated content access behavior

## 4.7 Podcast, Video, Film
- Show/season/episode style models
- Plan-gated content experiences
- Unified media consumption UI

## 4.8 Education Hub
- Articles and videos
- Free vs paid resource gating
- Learning/progress-oriented UI

## 4.9 Community
- Fanfare forum-style interactions
- Networking directory interactions
- Creator-fan engagement surfaces

## 4.10 Merch, Notifications, Admin
- Merch storefront integration surfaces
- Notification UX (release and interaction alerts)
- Admin controls for moderation and operational tasks

---

## 5) Technology Direction (Implementation Scope)
- **Mobile App:** Flutter (single codebase for iOS + Android)
- **Backend API:** FastAPI
- **Database:** PostgreSQL
- **Authentication:** Clerk
- **Media Streaming:** Mux
- **Object Storage:** Cloudflare R2
- **Payments:** Stripe + Stripe Connect
- **Search:** Typesense
- **Background Jobs:** Celery + Redis
- **Realtime:** Supabase Realtime
- **Email:** Resend
- **Infra/Hosting:** Railway or Render
- **Monitoring:** GlitchTip

---

## 6) Delivery Roadmap (12 Sprints)
- **S00–S01:** Foundation, infra, onboarding, profiles
- **S02–S03:** Music upload/streaming + fan playback UX
- **S04–S05:** OPI dashboard + discovery/search/playlist surfaces
- **S06–S07:** Monetization, wallets, subscriptions, podcast/video
- **S08–S09:** Education hub + community modules
- **S10–S11:** Merch, notifications, admin, launch readiness

Total roadmap duration: ~24 weeks.

---

## 7) UX & Design System Direction
- Near-black base background
- Gold as primary action and value accent
- Dark card surfaces and low-contrast separators
- Cinematic premium styling over generic social UI
- Mobile-first interaction patterns and hierarchy

---

## 8) Current Prototype Status (Web Mockup)
A UI prototype exists in:
- `ownln_web/index.html`

Prototype includes:
- Email login/signup UI
- Core app screens (home, profile, player, OPI, wallet, subscription)
- Extended module mockups (search, library, community, upload, podcast, education, merch, admin)
- Dedicated in-app docs view for quick reference

This prototype is static and frontend-only:
- No API calls
- No backend integration
- No persistence

---

## 9) Notes
This document is project-focused and excludes proposal-only commercial/legal acceptance text. It is intended as a product and implementation reference for design, planning, and development alignment.
