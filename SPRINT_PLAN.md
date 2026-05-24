# OWNLN — Sprint Plan & Delivery Roadmap

> **"Own Your Music. Own Your Future."**
> Client: Shadow Works Entertainment LLC
> Developer: [Your Studio Name]
> Start Date: June 2, 2026 · End Date: November 28, 2026
> Total Duration: 24 Weeks · 12 Sprints · 2 Weeks Each
> Total Investment: $7,900

---

## Overview

This sprint plan maps the complete development lifecycle of the OWNLN mobile platform — a creator-first music and media app built with Flutter (iOS + Android) and FastAPI. Each sprint is scoped to deliver production-quality, demonstrable software. No sprint begins until the prior sprint's demo is approved and invoiced.

The prototype mockup (`ownln_web/index.html`) — a full-fidelity, single-file React/HTML design preview — has been reviewed and approved by the client. All screen designs, user flows, color tokens, typography, and interaction patterns reflected in that prototype serve as the definitive visual specification for the Flutter build.

---

## Design System Reference (From Approved Mockup)

The approved prototype establishes the following design tokens. All Flutter screens must match these exactly.

| Token | Value | Usage |
|---|---|---|
| Background | `#000000` | App base background |
| Card Level 1 | `#0A0A0A` | Primary cards |
| Card Level 2 | `#121212` | Nested cards |
| Card Level 3 | `#1A1A1A` | Elevated surfaces |
| Main Gold | `#C79A3A` | Primary accent, borders, icons |
| Highlight Gold | `#E6B857` | Hover states, gradient start |
| Light Gold | `#FFF4A3` | Text gradient start |
| Dark Gold | `#A67C2E` | Gradient end, shadows |
| Body Font | `Inter` | All body text |
| Display Font | `Inter Tight` | Headings, weight 800–900 |
| Card Radius | `26–28px` | All cards |
| Button Radius | `42px` | Primary / secondary buttons |
| Pill Radius | `99px` | Tags, filters, badges |
| Primary Button | Gold gradient fill, black text, 900 weight |
| Secondary Button | Gold outline, transparent fill |
| Ghost Button | Subtle gold tint, low-opacity border |

**Animations:** `fadeInUp`, `shimmerFlow`, `premiumGlow`, `floatSoft`, `pulse`, `scaleIn`

---

## Prototype Screen Index (Approved Mockup)

The following screens are fully designed and approved in `index.html`. Flutter development must replicate each screen with identical layout, spacing, typography, and interaction states.

| # | Screen | Route Key | Role |
|---|--------|-----------|------|
| 1 | Auth / Role Select | `auth` | Both |
| 2 | Fan Home | `home` (fan) | Fan |
| 3 | Artist Home | `home` (artist) | Artist |
| 4 | Music Player (Full) | `player` | Both |
| 5 | Persistent Mini Player | Component | Both |
| 6 | Upload Track | `upload` | Artist |
| 7 | Content Approval Queue | `approval` | Artist |
| 8 | Search & Discovery | `search` | Both |
| 9 | OPI Dashboard | `opi` | Artist |
| 10 | Wallet & Payouts | `wallet` | Artist |
| 11 | Subscribe / Membership | `subscribe` | Both |
| 12 | Podcast Hub | `podcast` | Both |
| 13 | Education Center | `education` | Both |
| 14 | Community Hub | `community` | Both |
| 15 | Fanfare Forum | `fanfare` | Fan |
| 16 | Networking Directory | `networking` | Both |
| 17 | Merch Store (Platform) | `merch` | Both |
| 18 | Notifications | `notifications` | Both |
| 19 | Settings | `settings` | Both |
| 20 | Admin Panel | `admin` | Admin |
| 21 | Marketplace | `marketplace` | Both |
| 22 | Collab Hub | `collabhub` | Artist |
| 23 | Producer Connect | `producerconnect` | Artist |
| 24 | AR Hub | `arhub` | Both |
| 25 | OWNLN Live | `ownlnlive` | Both |
| 26 | Fan Clubs | `fanclubs` | Fan |
| 27 | Streaming Ops | `streamingops` | Artist |
| 28 | Features Overview | `features` | Both |
| 29 | Artist Public Profile | `artistpublic` | Both |
| 30 | Fan Profile | `fanprofile` | Fan |
| 31 | Fan Saved / Library | `fansaved` | Fan |
| 32 | Artist Library | `library` (artist) | Artist |
| 33 | Fan Library | `library` (fan) | Fan |
| 34 | Playlist View & Manage | `playlist` | Both |
| 35 | Podcast Episode Page | `episode` | Both |
| 36 | Release Scheduling | `scheduling` | Artist |
| 37 | Artist Onboarding Flow | `artistonboarding` | Artist |
| 38 | Fan Onboarding Flow | `fanonboarding` | Fan |
| 39 | Artist Merch Storefront | `artistmerch` | Both |

---

## Sprint Calendar

| Sprint | Dates | Phase | Focus |
|--------|-------|-------|-------|
| S00 | Jun 2 – Jun 15 | Foundation | Infrastructure & Setup |
| S01 | Jun 16 – Jun 29 | Phase 1 | Profiles & Onboarding |
| S02 | Jun 30 – Jul 13 | Phase 2 | Music Upload & Streaming |
| S03 | Jul 14 – Jul 27 | Phase 2 | Fan Music Experience |
| S04 | Jul 28 – Aug 10 | Phase 2–3 | Artist Dashboard & OPI |
| S05 | Aug 11 – Aug 24 | Phase 2 | Search, Discovery & Playlists |
| S06 | Aug 25 – Sep 7 | Phase 4 | Monetization & Wallets |
| S07 | Sep 8 – Sep 21 | Phase 3 | Podcast, Film & Episodes |
| S08 | Sep 22 – Oct 5 | Phase 5 | Education Hub |
| S09 | Oct 6 – Oct 19 | Phase 5 | Community, Fanfare & Networking |
| S10 | Oct 20 – Nov 2 | Phase 5 | Merch, Notifications & Admin |
| S11 | Nov 3 – Nov 28 | Phase 6–7 | App Delivery & Launch |

---

## Milestone Targets

| Milestone | Target Date |
|-----------|-------------|
| Streaming MVP (Fan can stream music end-to-end) | Jun 29, 2026 |
| Monetization Live (Stripe + wallets active) | Sep 7, 2026 |
| App Builds Distributed (TestFlight + APK) | Nov 3, 2026 |
| App Store / Play Store Submission | Nov 17, 2026 |
| Go-Live Target | Nov 28, 2026 |

---

## Sprint Details

---

### Sprint 00 — Foundation & Infrastructure
**Dates:** Jun 2 – Jun 15, 2026
**Invoice:** $400 *(Discounted onboarding rate — due at project kickoff)*
**Phase:** 0–1

#### Objective
Establish the complete technical foundation. No feature work begins until the infrastructure is verified, tested, and running in both local and production environments.

#### Deliverables

**Monorepo & CI/CD**
- [ ] Monorepo initialized under Shadow Works Entertainment LLC GitHub org
- [ ] Flutter project scaffolded (iOS + Android targets)
- [ ] FastAPI project scaffolded with folder structure, virtual environment, and requirements
- [ ] GitHub Actions CI/CD pipeline: lint, test, build checks on every push
- [ ] `.env` management — local, staging, and production configs documented

**Infrastructure**
- [ ] PostgreSQL schema v1 deployed on Railway/Render
  - Users, roles, artist profiles, fan profiles, follows
  - Tracks, albums, moods, genres, content status
  - Subscriptions, wallet ledger, transactions
- [ ] Clerk authentication configured (social login, email, role management)
- [ ] Mux account + API keys connected (audio/video streaming)
- [ ] Cloudflare R2 bucket provisioned (audio file storage)
- [ ] Celery + Redis setup for background jobs
- [ ] Supabase Realtime configured for live activity feeds

**Flutter App Shell**
- [ ] App launch screen with OWNLN logo and gold animation
- [ ] Design system implemented:
  - Color tokens matching approved mockup (`#000000`, `#C79A3A`, `#E6B857`)
  - Typography: Inter (body) + Inter Tight (headings, 800–900 weight)
  - Card styles (26–28px radius), button styles (42px radius), pill styles (99px)
  - Animation tokens: `fadeInUp`, `shimmerFlow`, `premiumGlow`, `pulse`
- [ ] Navigation shell: bottom nav bar (5 tabs), screen router
- [ ] Dark/gold global theme applied across all base widgets

**Demo Deliverables**
- [ ] Live app shell on device (black screen, gold nav, animated launch)
- [ ] Database schema diagram shared
- [ ] All third-party services connected and verified live

---

### Sprint 01 — Profiles & Onboarding
**Dates:** Jun 16 – Jun 29, 2026
**Invoice:** $400 *(Discounted onboarding rate — due at Sprint 00 demo approval)*
**Phase:** 1

#### Objective
Complete user registration, onboarding flows, and public profile infrastructure. Both artist and fan roles fully operable by end of sprint.

#### Screens Delivered (Matching Approved Mockup)
- `auth` — Role selection + login / signup (email + social)
- `artistonboarding` — 4-step artist setup: photo, bio, genre tags, social links
- `fanonboarding` — 3-step fan setup: genres, moods, follow artists
- `artistpublic` — Public artist profile (bio, avatar, banner, genre tags, stats)
- `fanprofile` — Fan profile (avatar, display name, following list)

#### Deliverables

**Auth & Registration**
- [ ] Clerk auth integrated in Flutter (email/password + Google/Apple social login)
- [ ] Role selection on first launch: Artist or Fan
- [ ] JWT session management — persistent login across app restarts
- [ ] Backend user creation endpoint linked to Clerk webhook

**Artist Onboarding (4 Steps)**
- [ ] Step 1: Profile photo upload → Cloudflare R2 storage → preview thumbnail
- [ ] Step 2: Artist bio — text input, 500-character limit
- [ ] Step 3: Genre tags — multi-select (up to 3 from approved taxonomy)
- [ ] Step 4: Social links — Instagram, Twitter/X, TikTok, YouTube fields
- [ ] Progress bar with gold gradient fill (step N of 4, percentage display)
- [ ] Skip option on non-required steps; complete at any time from settings

**Fan Onboarding (3 Steps)**
- [ ] Step 1: Favorite genres — multi-select (genre taxonomy from mockup)
- [ ] Step 2: Music moods — multi-select (mood taxonomy from mockup)
- [ ] Step 3: Follow artists — curated list with gold `FOLLOW` button per artist
- [ ] Progress bar with gold gradient fill
- [ ] Selections stored to fan preference profile for discovery personalization

**Public Artist Profile**
- [ ] Avatar, banner image, artist name, verified badge (if applicable)
- [ ] Bio, genre tags displayed as gold pills
- [ ] Follower count, track count, play count stats row
- [ ] Gold `Subscribe` CTA button → routes to `subscribe` screen
- [ ] Gold outline `Follow` button (toggles follow/unfollow)
- [ ] Recent tracks preview list (tappable → player)
- [ ] Follow/unfollow persisted in backend, real-time follower count update

**Fan Profile**
- [ ] Avatar, display name, member since date
- [ ] Following list with artist thumbnails
- [ ] Saved tracks count, playlist count

**API Endpoints (FastAPI)**
- [ ] `POST /users/register` — create user (artist or fan)
- [ ] `GET /artists/{id}` — public artist profile
- [ ] `GET /fans/{id}` — fan profile
- [ ] `POST /follows` / `DELETE /follows` — follow/unfollow
- [ ] `GET /artists/{id}/followers/count`

**Demo Deliverables**
- [ ] Live registration → onboarding → profile flow on device
- [ ] Artist profile page fully populated with follow/subscribe CTAs working
- [ ] Fan profile showing followed artists

---

### Sprint 02 — Music Upload & Streaming
**Dates:** Jun 30 – Jul 13, 2026
**Invoice:** $650 *(Due at Sprint 01 demo approval)*
**Phase:** 2

#### Objective
Artists can upload tracks end-to-end. Fans can stream tracks. Audio pipeline fully operational.

#### Screens Delivered
- `upload` — Track upload form (metadata, file, pricing, release date)
- `scheduling` — Release calendar with scheduled/draft release management
- `approval` — Artist-facing content approval queue

#### Deliverables

**Upload Pipeline**
- [ ] WAV / MP3 file picker (up to 500MB)
- [ ] Upload to Cloudflare R2 via presigned URL (progress bar with gold fill)
- [ ] Celery background job: trigger Mux processing after upload complete
- [ ] Auto-generate 320kbps MP3 + 128kbps AAC variants via Mux
- [ ] Track metadata form: title, genre tag, mood tag, cover art, description
- [ ] Pricing option: Free Stream / Pay to Download / Subscriber Only
- [ ] Album grouping — attach track to new or existing album

**Release Scheduling**
- [ ] Calendar UI showing all artist's upcoming releases
- [ ] Schedule release with date + time picker
- [ ] Status badges: `Scheduled` (green) / `Draft` (gold)
- [ ] Edit / Cancel release actions
- [ ] Celery scheduled task triggers publication at set date/time

**Content Approval Queue**
- [ ] Tracks pending review listed with metadata preview
- [ ] Status flow: `Pending` → `Under Review` → `Approved` / `Rejected`
- [ ] Rejection reason field shown to artist
- [ ] Admin-side approval controls (used in Sprint 10)

**Mux HLS Player (Flutter)**
- [ ] Mux HLS player widget integrated in Flutter
- [ ] 30-second audio preview waveform for non-subscribers
- [ ] Full playback for subscribers / free tracks
- [ ] Loading state with gold shimmer animation

**API Endpoints**
- [ ] `POST /tracks/upload-url` — generate presigned R2 URL
- [ ] `POST /tracks` — create track record after upload
- [ ] `GET /tracks/{id}` — track detail + Mux playback URL
- [ ] `GET /artists/{id}/tracks` — artist track list
- [ ] `POST /tracks/{id}/schedule` — set release date
- [ ] `GET /artists/{id}/releases/schedule` — release calendar

**Demo Deliverables**
- [ ] Live upload flow on device (drag file → metadata → publish)
- [ ] Track visible on artist profile immediately after approval
- [ ] Scheduled release visible on calendar

---

### Sprint 03 — Fan Music Experience
**Dates:** Jul 14 – Jul 27, 2026
**Invoice:** $650 *(Due at Sprint 02 demo approval)*
**Phase:** 2

#### Objective
Fans have a complete music listening experience. Background playback, lock-screen controls, and the persistent mini-player are all live.

#### Screens Delivered
- `home` (fan) — Fan home with mood tags, trending card, track feed
- `player` — Full-screen music player
- Persistent Mini Player — Fixed bottom bar across all screens
- `fansaved` — Saved tracks library

#### Deliverables

**Fan Home Screen**
- [ ] OWNLN logo with gold gradient, `floatSoft` animation
- [ ] Horizontal mood tag scroll bar (gold active pill, shimmer effect)
- [ ] `Trending Now` gold hero card (shimmer overlay, `premiumGlow` animation)
- [ ] `Play Now` gold button + `Subscribe` outline button on hero card
- [ ] Track feed filtered by selected mood — live data from backend
- [ ] Notification bell icon with live unread badge

**Full-Screen Player**
- [ ] Album art (large, rounded, `scaleIn` entry animation)
- [ ] Track title, artist name, album
- [ ] Gold progress bar with scrubbing gesture
- [ ] Controls: previous, skip back 15s, play/pause, skip forward 15s, next
- [ ] Like button (toggles, persisted to backend)
- [ ] Queue panel (swipe up or tab)
- [ ] Lyrics panel (placeholder UI, content model for Sprint 7)
- [ ] Share button

**Persistent Mini Player**
- [ ] Fixed bottom overlay above bottom nav bar
- [ ] Album art thumbnail (52×52px, 14px radius)
- [ ] Track title + artist (truncated with ellipsis)
- [ ] Play/pause, queue, lyrics icons
- [ ] Gold progress bar (5px height, shimmer animation)
- [ ] `50px` backdrop blur, gold border top
- [ ] Tap on title/art → expands to full player

**Playback Features**
- [ ] Background audio playback (Flutter `just_audio`)
- [ ] Lock-screen media controls (iOS Control Center + Android notification)
- [ ] Android notification media controls
- [ ] Bluetooth headphone compatibility (play/pause/skip)
- [ ] 60-minute continuous playback validation (QA test)

**Like & Save**
- [ ] Heart button on player + track row → persisted to backend
- [ ] `fansaved` screen shows all liked/saved tracks
- [ ] Recently played list stored locally

**API Endpoints**
- [ ] `GET /feed` — personalized track feed by mood/genre/follows
- [ ] `GET /trending` — trending tracks algorithm
- [ ] `POST /tracks/{id}/like` / `DELETE /tracks/{id}/like`
- [ ] `GET /fans/{id}/saved` — saved tracks list
- [ ] `GET /tracks/{id}/stream-url` — Mux HLS playback URL

**Demo Deliverables**
- [ ] Full end-to-end listen: home → tap track → full player → background play → lock screen controls
- [ ] Mini player visible and functional while browsing other screens
- [ ] Saved tracks library populated

---

### Sprint 04 — Artist Dashboard & OPI
**Dates:** Jul 28 – Aug 10, 2026
**Invoice:** $650 *(Due at Sprint 03 demo approval)*
**Phase:** 2–3

#### Objective
Artists have a complete real-time dashboard including the proprietary OPI (OWNLN Performance Index) score and full revenue visibility.

#### Screens Delivered
- `home` (artist) — Artist home dashboard
- `opi` — OPI detailed analytics view
- `streamingops` — Streaming performance data
- `artist` — Artist self-profile / management view
- `library` (artist) — Artist content library

#### Deliverables

**Artist Home Dashboard**
- [ ] OPI score card (0–100 composite score, gold progress ring, `premiumGlow`)
- [ ] Revenue summary row: Today / This Week / This Month
- [ ] Streams today vs. yesterday delta indicator
- [ ] Quick-action buttons: Upload, Schedule, Analytics, Wallet
- [ ] Top performing track this week (mini `TrackRow` card)
- [ ] Recent fan activity (new follows, likes, subscriptions)

**OPI (OWNLN Performance Index) Dashboard**
- [ ] Composite score formula: streams + followers + subscriptions + engagement + revenue
- [ ] Score trend line chart (7-day, 30-day, 90-day toggle)
- [ ] Category breakdown:
  - Streaming Performance (plays, unique listeners, completion rate)
  - Audience Growth (follower count, follow velocity)
  - Revenue Performance (MRR, ARPU, payout history)
  - Content Engagement (likes, saves, shares per track)
- [ ] Fan geography heatmap (country/region distribution)
- [ ] Top 5 tracks by stream count table

**Streaming Operations**
- [ ] Per-track stream analytics (plays, completions, skip rate)
- [ ] Peak listening hours chart
- [ ] Platform CDN health indicators

**Artist Library**
- [ ] All uploaded tracks with status badges (Published / Scheduled / Draft / Rejected)
- [ ] Edit track metadata inline
- [ ] Delete / archive track
- [ ] Album grouping view

**API Endpoints**
- [ ] `GET /artists/{id}/opi` — computed OPI score + breakdown
- [ ] `GET /artists/{id}/analytics` — aggregated stream data
- [ ] `GET /artists/{id}/revenue/summary` — revenue by source + period
- [ ] `GET /artists/{id}/geography` — fan location data from Mux
- [ ] `GET /artists/{id}/tracks/performance` — per-track metrics

**Demo Deliverables**
- [ ] Live OPI score updating in real-time on device
- [ ] All 5 analytics sub-sections navigable and populated with real data
- [ ] Artist library showing track status management

---

### Sprint 05 — Search, Discovery & Playlists
**Dates:** Aug 11 – Aug 24, 2026
**Invoice:** $650 *(Due at Sprint 04 demo approval)*
**Phase:** 2

#### Objective
Fans and artists can discover content through search and mood/genre browsing. Playlist creation and management is fully operational.

#### Screens Delivered
- `search` — Search & discovery hub
- `playlist` — Playlist view and management
- `library` (fan) — Fan music library

#### Deliverables

**Search & Discovery**
- [ ] Full-text search bar (Typesense) — tracks, artists, podcasts, albums
- [ ] Real-time results as user types (debounced 300ms)
- [ ] Result type tabs: All / Tracks / Artists / Podcasts
- [ ] Mood filter pills (horizontal scroll, gold active state)
- [ ] Genre filter pills (horizontal scroll)
- [ ] Trending tracks list below search bar (default state)
- [ ] Trending artists grid with follow button
- [ ] `Trending Algorithm` info card (plays + saves + shares + conversions weighted)
- [ ] Artist directory page with role-filter tabs

**Playlist Management**
- [ ] Create new playlist (name, cover emoji/image)
- [ ] View playlist: cover art, track count, total duration
- [ ] `Play All` gold button + `Shuffle` outline button
- [ ] Reorder tracks via drag handle
- [ ] Remove track from playlist (swipe or tap `⋯` menu)
- [ ] Add tracks CTA → navigates to search with `Add to Playlist` mode
- [ ] Playlist saved to backend + synced across devices

**Fan Library**
- [ ] Tabs: Playlists / Saved Tracks / Following / Recently Played
- [ ] Playlist grid (2-column, gold border cards)
- [ ] Saved tracks list with `TrackRow` component
- [ ] Following list with artist thumbnails + quick-play latest track

**Typesense Integration**
- [ ] Typesense index populated on track/artist creation
- [ ] Search weights: title match > artist match > genre/mood match
- [ ] Typo tolerance enabled

**API Endpoints**
- [ ] `GET /search?q=&type=` — Typesense-backed search
- [ ] `GET /trending?limit=` — trending tracks algorithm
- [ ] `POST /playlists` — create playlist
- [ ] `GET /playlists/{id}` — playlist detail
- [ ] `POST /playlists/{id}/tracks` — add track to playlist
- [ ] `DELETE /playlists/{id}/tracks/{trackId}` — remove track
- [ ] `PUT /playlists/{id}/order` — reorder tracks

**Demo Deliverables**
- [ ] Live search returning real results in under 300ms
- [ ] Full playlist create → add tracks → reorder → play all flow on device
- [ ] Fan library tabs all populated with real data

---

### Sprint 06 — Monetization & Wallets
**Dates:** Aug 25 – Sep 7, 2026
**Invoice:** $650 *(Due at Sprint 05 demo approval)*
**Phase:** 4

#### Objective
Full monetization infrastructure is live. Fans can subscribe and purchase. Artists receive real payouts via Stripe Connect. The 80/20 revenue split is enforced and auditable.

#### Screens Delivered
- `subscribe` — Fan subscription / membership tiers
- `wallet` — Artist wallet and payout history

#### Deliverables

**Fan Subscriptions**
- [ ] Free tier vs. Pro Fan ($9.99/mo) plan comparison screen
- [ ] Stripe Checkout integration for Pro subscription
- [ ] Subscription status persisted + enforced on gated content
- [ ] Upgrade/downgrade and cancellation flows
- [ ] Subscription renewal receipts via Resend email

**Track & Album Purchase**
- [ ] One-time purchase flow for `Pay to Download` tracks
- [ ] Stripe Payment Intent for individual track/album purchases
- [ ] Download fulfillment: Cloudflare R2 signed download URL
- [ ] Purchase receipt email via Resend

**Artist Wallet (Stripe Connect)**
- [ ] Stripe Connect onboarding flow (identity, banking details)
- [ ] Wallet home: Total Earned / Pending / Paid Out balances
- [ ] Revenue breakdown: Streams / Subscriptions / Purchases / Merch / Ads
- [ ] 80/20 split logic implemented in backend revenue router
- [ ] Transaction history table (source, amount, date, status)
- [ ] Withdrawal request → Stripe Connect payout triggered
- [ ] Payout confirmation email via Resend

**Revenue Ledger (Backend)**
- [ ] Every revenue event logged: timestamp, source, gross, platform cut, artist net
- [ ] Revenue split enforced at payment capture:
  - Artist: 80% (scaling to 90% for high performers at $10K+ MRR)
  - Platform: 20%
- [ ] Admin payout override controls (used in Sprint 10)

**Gated Content Enforcement**
- [ ] `Subscriber Only` tracks reject playback for free users → prompt upgrade
- [ ] Premium podcast episodes blocked for free users
- [ ] Education content gating by tier

**API Endpoints**
- [ ] `POST /subscriptions` — create Stripe subscription
- [ ] `GET /subscriptions/{userId}` — subscription status
- [ ] `POST /purchases` — one-time track purchase
- [ ] `GET /artists/{id}/wallet` — balance + breakdown
- [ ] `GET /artists/{id}/transactions` — ledger history
- [ ] `POST /payouts/request` — trigger Stripe Connect payout
- [ ] `POST /webhooks/stripe` — Stripe event handler

**Demo Deliverables**
- [ ] Live end-to-end: fan subscribes → artist wallet balance increases → artist withdraws
- [ ] 80/20 split visible in transaction log
- [ ] Gated content correctly blocked/unlocked by subscription status

---

### Sprint 07 — Podcast, Film & Episodes
**Dates:** Sep 8 – Sep 21, 2026
**Invoice:** $650 *(Due at Sprint 06 demo approval)*
**Phase:** 3

#### Objective
Complete podcast and video content infrastructure. Artists can publish shows. Fans can browse episodes with correct free/gated access.

#### Screens Delivered
- `podcast` — Podcast hub (all shows)
- `episode` — Episode detail page (summary, clips, full player)

#### Deliverables

**Content Hierarchy**
- [ ] Data model: `Show → Season → Episode → Episode Detail`
- [ ] Show creation form (title, description, cover art, category)
- [ ] Season management (create, edit, episode count)
- [ ] Episode upload: Mux video/audio processing pipeline
- [ ] Episode metadata: title, season, episode number, summary, duration
- [ ] Episode access flag: `Free` or `Pro`
- [ ] YouTube/Vimeo embed support for external video content

**Podcast Hub Screen**
- [ ] Featured show banner card (gold shimmer, `premiumGlow`)
- [ ] Show list with cover art, host name, episode count
- [ ] Tap show → season list → episode list
- [ ] `FREE` / `PRO` badge on each episode row
- [ ] Progress ring on episodes started but not finished

**Episode Detail Screen**
- [ ] Episode header: show name, season badge, episode number badge
- [ ] Free / Pro access badge (green `FREE`, gold `PRO`)
- [ ] `Play Full Episode` gold button (gated for Pro if Pro episode)
- [ ] Episode summary text block
- [ ] `Key Clips` section — tappable clips with timestamp + PRO lock where applicable
- [ ] Playback via Mux HLS (audio or video based on content type)

**Film / Exclusive Video**
- [ ] Film content model (single video, plan-gated)
- [ ] Film browse tab within podcast hub
- [ ] Full-screen Mux HLS video player

**API Endpoints**
- [ ] `POST /shows` / `GET /shows` — show management
- [ ] `GET /shows/{id}/seasons` — season list
- [ ] `GET /seasons/{id}/episodes` — episode list
- [ ] `GET /episodes/{id}` — episode detail + Mux playback URL (gated)
- [ ] `POST /episodes/{id}/progress` — save listen progress

**Demo Deliverables**
- [ ] Full podcast browse → tap show → season → episode → play flow on device
- [ ] Free episode plays for all users; Pro episode prompts upgrade for free users
- [ ] Episode clips section interactive and correctly gated

---

### Sprint 08 — Education Hub
**Dates:** Sep 22 – Oct 5, 2026
**Invoice:** $650 *(Due at Sprint 07 demo approval)*
**Phase:** 5

#### Objective
Complete education platform with free and gated content, progress tracking, and the templates & contracts library.

#### Screens Delivered
- `education` — Education hub with courses and resources

#### Deliverables

**Content Model**
- [ ] `Course → Module → Lesson` hierarchy
- [ ] Lesson types: article (rich text), video (Mux), audio
- [ ] Content tags: Free / Pro
- [ ] Admin content management endpoints

**Education Hub Screen**
- [ ] Featured course banner (gold card, shimmer)
- [ ] Free tier section:
  - Music Business Basics
  - Marketing for Indie Artists
  - Community Building
- [ ] Pro tier section (PRO badge, blurred preview for free users):
  - Sync Licensing Masterclass
  - Templates & Contracts Library
  - Growth Analytics Playbook
- [ ] Course card: title, module count, estimated hours, progress ring
- [ ] Tap course → module list → lesson view

**Progress Tracking**
- [ ] Lesson completion state persisted per user
- [ ] Course progress percentage shown on card
- [ ] Resume lesson from last watched position

**Templates & Contracts Library (Pro)**
- [ ] Downloadable PDF templates (R2 signed URLs)
- [ ] Categories: Recording Agreements, Sync Licenses, Management Deals, Publishing Splits
- [ ] Preview first page; download requires Pro subscription

**API Endpoints**
- [ ] `GET /courses` — course list with user progress
- [ ] `GET /courses/{id}/modules` — module list
- [ ] `GET /lessons/{id}` — lesson content (gated check)
- [ ] `POST /lessons/{id}/complete` — mark lesson complete
- [ ] `GET /templates` — template library (Pro gated)

**Demo Deliverables**
- [ ] Full course browse → module → lesson flow on device
- [ ] Progress ring advancing as lessons completed
- [ ] Free user sees Pro content preview with upgrade prompt
- [ ] Templates section downloads correctly for Pro user

---

### Sprint 09 — Community: Fanfare & Networking
**Dates:** Oct 6 – Oct 19, 2026
**Invoice:** $650 *(Due at Sprint 08 demo approval)*
**Phase:** 5

#### Objective
Community features fully live. Fan-to-artist interaction, creator networking, and collaboration tooling all operational.

#### Screens Delivered
- `community` — Community hub
- `fanfare` — Fan forum
- `networking` — Networking directory
- `collabhub` — Collaboration board

#### Deliverables

**Fanfare Forum**
- [ ] Topic list: categories (Releases, Interviews, Playlists, Events)
- [ ] Thread view: posts, replies, timestamp, author avatar
- [ ] Create post / reply CTA (gold button)
- [ ] Like / react to posts
- [ ] Playlist sharing within threads (embedded playlist card)
- [ ] Artist pinned announcement posts (gold highlight)
- [ ] Supabase Realtime: new replies appear without refresh

**Networking Directory**
- [ ] Role filter tabs: Artists / Producers / Engineers / Managers / A&Rs
- [ ] Per-profile card: avatar, name, role badge, genre focus, availability status
- [ ] Availability toggle: `Open to Collabs` (green) / `Busy` (muted)
- [ ] Contact / Connect button → direct message (placeholder for DM Sprint 11)
- [ ] Search within networking directory

**Collab Hub**
- [ ] Post open project board (title, role needed, genre, deadline)
- [ ] Browse open projects by role / genre filter
- [ ] Express interest button → notification to project owner

**Reporting & Moderation (Baseline)**
- [ ] Report post / report user flow
- [ ] Reported items queue visible in Admin panel (Sprint 10)

**Activity Feed**
- [ ] Per-user activity feed: new posts in followed threads, new tracks from followed artists
- [ ] Supabase Realtime for live activity updates

**API Endpoints**
- [ ] `GET /forum/topics` / `POST /forum/topics`
- [ ] `GET /forum/topics/{id}/posts` / `POST /forum/topics/{id}/posts`
- [ ] `POST /forum/posts/{id}/like`
- [ ] `GET /networking` — directory with role filter
- [ ] `GET /collab/projects` / `POST /collab/projects`
- [ ] `POST /reports` — content/user report submission

**Demo Deliverables**
- [ ] Live post + reply in Fanfare visible in real-time on second device
- [ ] Networking directory filterable by role
- [ ] Collab project board navigable with post + browse flow
- [ ] Reported content surfacing in admin queue

---

### Sprint 10 — Merch, Notifications & Admin
**Dates:** Oct 20 – Nov 2, 2026
**Invoice:** $650 *(Due at Sprint 09 demo approval)*
**Phase:** 5

#### Objective
Merch integration complete. Push notifications and email flows live. Admin panel fully operational for platform management.

#### Screens Delivered
- `merch` — Platform merch hub
- `artistmerch` — Individual artist Shopify storefront
- `notifications` — Notification center
- `admin` — Admin panel
- `settings` — User settings

#### Deliverables

**Shopify Merch Integration**
- [ ] Shopify Storefront API connected
- [ ] Platform merch hub: featured products from all artists
- [ ] Artist merch storefront: per-artist product grid (2-column)
- [ ] Product card: image/emoji, name, price, stock count
- [ ] `Buy Now` gold button → Shopify checkout (external browser or WebView)
- [ ] Merch tab surfaced on public artist profile
- [ ] `Secure checkout via Shopify` trust badge

**Push Notifications (FCM)**
- [ ] FCM integration in Flutter (iOS + Android)
- [ ] Notification triggers:
  - New track release from followed artist
  - New podcast episode from followed show
  - Reply to your forum post
  - Subscription renewal alert
  - Payout processed confirmation
  - New follower alert (artist)
- [ ] Notification preferences screen (per-category toggle)
- [ ] In-app notification center (`notifications` screen) with unread count badge

**Transactional Emails (Resend)**
- [ ] Welcome email (fan + artist, role-specific)
- [ ] Track purchase receipt
- [ ] Subscription confirmation + renewal receipts
- [ ] Payout processed confirmation
- [ ] Release published confirmation (artist)
- [ ] Password reset (via Clerk)

**Admin Panel**
- [ ] User management: list, search, suspend, unsuspend accounts
- [ ] Content moderation: approve/reject track queue, remove reported content
- [ ] Subscription override: manually grant/revoke Pro access
- [ ] Payout controls: trigger manual payout, adjust split rate for high performers
- [ ] Featured placement: pin artists/tracks to home screen
- [ ] DMCA takedown workflow: log, notify, remove, repeat-infringer tracking

**Settings Screen**
- [ ] Account: edit profile photo, display name, bio
- [ ] Subscription: current plan, upgrade/cancel
- [ ] Notifications: per-category push toggle
- [ ] Privacy: data download, account deletion request
- [ ] About: version, terms, privacy policy, support contact
- [ ] Logout

**API Endpoints**
- [ ] `GET /notifications/{userId}` — notification list
- [ ] `POST /notifications/preferences` — update push preferences
- [ ] `GET /merch/featured` — platform merch feed (Shopify)
- [ ] `GET /artists/{id}/merch` — artist Shopify products
- [ ] Admin endpoints: `/admin/users`, `/admin/content/queue`, `/admin/payouts`

**Demo Deliverables**
- [ ] Push notification received on real device when artist publishes new track
- [ ] Merch storefront loading Shopify products in real-time
- [ ] Admin panel: full moderation workflow demonstrated live
- [ ] Settings: all account management flows functional

---

### Sprint 11 — App Delivery & Launch Prep
**Dates:** Nov 3 – Nov 28, 2026
**Invoice:** $650 *(Due at Sprint 10 demo approval)*
**Phase:** 6–7

#### Objective
Production-ready app delivered to client on real devices. App Store and Play Store submissions complete. Performance, security, and stability validated.

#### Deliverables

**App Builds**
- [ ] TestFlight build distributed to Chris + Tracy (iOS)
- [ ] APK build distributed to client (Android)
- [ ] Version `1.0.0` tagged in GitHub

**Performance Audit**
- [ ] App launch time < 2.5 seconds (cold start)
- [ ] Player screen LCP < 1.5 seconds
- [ ] Search response < 300ms (Typesense)
- [ ] 60-minute continuous playback validated (background + screen off)
- [ ] Memory leak testing (30-min device session)

**Security Review**
- [ ] All API endpoints authenticated (no unauthenticated data access)
- [ ] Stripe webhook signature validation verified
- [ ] R2 file access requires signed URLs (no public bucket exposure)
- [ ] Clerk JWT validation on every protected route
- [ ] DMCA takedown pipeline tested end-to-end

**Load Testing**
- [ ] Simulate 500 concurrent streams → Mux CDN confirmed stable
- [ ] 1,000 concurrent API requests → FastAPI under load
- [ ] Database query optimization audit (slow query log review)

**Monitoring**
- [ ] GlitchTip error tracking configured for Flutter + FastAPI
- [ ] Alerting rules: 5xx error spike, payment failure spike, auth failure spike
- [ ] Uptime monitoring on all production services

**App Store Submission**
- [ ] App Store Connect: metadata, screenshots (all device sizes), description, keywords
- [ ] Play Store Console: listing, graphics, content rating questionnaire
- [ ] Privacy policy URL provided by client (required by both stores)
- [ ] App submitted for review (Apple: 1–3 day review; Google: 1–7 day review)

**Sprint 11 Polish Pass**
- [ ] All minor/cosmetic issues from Sprints 0–10 batched and addressed
- [ ] Placeholder screens replaced with final content
- [ ] Edge case handling: empty states, network errors, offline mode fallbacks

**Documentation Delivered**
- [ ] API documentation (all endpoints, request/response schemas)
- [ ] Database schema documentation (ER diagram + table descriptions)
- [ ] Environment variable reference (all services)
- [ ] Deployment runbook (staging + production)
- [ ] GitHub repository handed over to Shadow Works Entertainment LLC org

**Demo Deliverables**
- [ ] Client installs TestFlight build + APK — live app, real usage
- [ ] Full platform walkthrough on real device: auth → stream → subscribe → pay → admin
- [ ] App Store + Play Store submission confirmation shared
- [ ] All documentation delivered

---

## Payment Schedule

| Sprint | Payment Trigger | Amount | Due Date (Est.) |
|--------|----------------|--------|-----------------|
| Sprint 00 | Invoice at project kickoff | $400 | Jun 2, 2026 |
| Sprint 01 | Sprint 00 demo approval | $400 | Jun 16, 2026 |
| Sprint 02 | Sprint 01 demo approval | $650 | Jun 30, 2026 |
| Sprint 03 | Sprint 02 demo approval | $650 | Jul 14, 2026 |
| Sprint 04 | Sprint 03 demo approval | $650 | Jul 28, 2026 |
| Sprint 05 | Sprint 04 demo approval | $650 | Aug 11, 2026 |
| Sprint 06 | Sprint 05 demo approval | $650 | Aug 25, 2026 |
| Sprint 07 | Sprint 06 demo approval | $650 | Sep 8, 2026 |
| Sprint 08 | Sprint 07 demo approval | $650 | Sep 22, 2026 |
| Sprint 09 | Sprint 08 demo approval | $650 | Oct 6, 2026 |
| Sprint 10 | Sprint 09 demo approval | $650 | Oct 20, 2026 |
| Sprint 11 | Sprint 10 demo approval | $650 | Nov 3, 2026 |
| **TOTAL** | | **$7,900** | **Nov 28, 2026** |

> All amounts USD. Third-party vendor fees (Mux, Stripe, Clerk, Cloudflare R2, Railway) are billed separately by vendors and are not included above. Shadow Works Entertainment LLC is responsible for all third-party service subscriptions per the Development Agreement.

---

## Sprint Cycle Process

Every sprint follows this exact cycle:

```
Day 1     → Sprint kickoff call (30 min) — align on scope and priorities
Days 2–13 → Active development — GitHub commits pushed throughout
Day 13    → Internal testing and QA by developer
Day 14    → Demo call — live walkthrough on real device, all features demonstrated
Days 15–19→ Client review window (5 business days per Development Agreement)
Day 20    → Written approval OR written Critical Blocking Issues submitted
Day 21    → Next sprint invoice issued + next sprint begins
```

---

## Issue Resolution Policy

| Issue Type | Definition | Resolution Timeline |
|------------|-----------|---------------------|
| **Critical Blocking** | Core feature not functional, blocks user flow | Fixed within 14 days (30 days for Modules 0, 5, 10, 11, 12) |
| **Major** | Feature incomplete or incorrect but workaround exists | Next available sprint or as agreed |
| **Minor / Cosmetic** | Visual polish, copy, spacing, color delta | Batched — addressed in Sprint 11 polish pass |

---

## Scope Reference

### In Scope

- Flutter iOS + Android mobile application
- FastAPI backend (all endpoints, auth middleware, business logic)
- PostgreSQL schema design, Alembic migrations, query optimization
- Clerk authentication (artist + fan + admin roles)
- Mux streaming — music, podcast, and video (HLS, background playback)
- Stripe + Stripe Connect — subscriptions, purchases, artist payouts
- OPI analytics dashboard (proprietary creator performance index)
- Creator wallet + 80/20 payout routing + earnings ledger
- Shopify Storefront API merch integration
- Typesense search and discovery infrastructure
- Admin panel (moderation, content approval, payout controls)
- DMCA / repeat-infringer tracking + takedown workflow
- Push notifications (FCM) and transactional emails (Resend)
- CI/CD pipeline, staging + production environments
- GitHub repository under Shadow Works Entertainment LLC org
- TestFlight + APK builds from Sprint 06 onwards
- App Store + Play Store submission
- All documentation per Development Agreement
- 12 sprint demo calls + sprint reports

### Out of Scope

- Web platform / browser version (separate future phase)
- Native merch store (post-launch roadmap)
- AI recommendation engine or signal-detection layer
- Third-party vendor subscription fees (Mux, Stripe, Clerk, etc.)
- Content moderation staffing or manual review team
- Legal contracts, Terms of Service, Privacy Policy drafting
- Marketing, SEO campaigns, ad management
- Creator onboarding support or community management
- Music licensing or rights management infrastructure

---

## Technology Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| Mobile App | Flutter | iOS + Android, single codebase, native performance |
| Backend API | FastAPI (Python) | Async, high-performance API |
| Database | PostgreSQL | Relational data: subscriptions, wallets, content |
| Auth | Clerk | Social login, role management, JWT sessions |
| Audio/Video | Mux | HLS adaptive streaming, CDN delivery, analytics |
| File Storage | Cloudflare R2 | Audio/video file storage, zero egress fees |
| Payments | Stripe + Connect | Subscriptions, purchases, artist payouts |
| Search | Typesense | Full-text search, typo tolerance, fast results |
| Merch | Shopify Storefront API | E-commerce, no inventory risk |
| Background Jobs | Celery + Redis | Release scheduling, payout routing, async tasks |
| Real-time | Supabase Realtime | Live community feeds, activity streams |
| Email | Resend | Transactional emails (receipts, alerts) |
| Hosting | Railway / Render | Auto-scaling deploys, no DevOps overhead |
| Monitoring | GlitchTip | Self-hosted error tracking across all services |
| Dev Tools | VS Code + Claude Code | Flutter + FastAPI extensions, AI-assisted scaffolding |

---

*OWNLN Sprint Plan — Prepared for Shadow Works Entertainment LLC*
*Document reflects approved prototype mockup (`ownln_web/index.html`) as design specification*
*All screen designs, interactions, and visual tokens in the prototype are considered final unless revised by client in writing*
