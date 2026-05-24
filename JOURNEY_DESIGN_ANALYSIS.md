# OWNLN — Journey vs Design Gap Analysis

> Comparing: `Fan Journey.csv` + `Creator Journey.csv` vs `index.html` prototype (39 screens)
> Purpose: Identify what is covered, what is missing, and what needs improvement for the Flutter build

---

## Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | Covered — screen and UI exist in design |
| ⚠️ | Partial — screen exists but missing key features from journey |
| ❌ | Missing — no screen or UI exists at all |
| 🔺 | Needs improvement — exists but needs design upgrade |

---

## Part 1 — Fan Journey Analysis

---

### Stage 1 — Discovery
*Goal: Find new artist or content*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Trending content surfaced on home | ✅ | Gold hero card "Trending Now" on FanHomeScreen |
| Multiple content types visible (music, podcasts) | ✅ | Home shows tracks + podcast section |
| Platform social presence / artist endorsement feel | ⚠️ | No landing page or web preview for unauthenticated users |
| Web preview before signup | ❌ | App goes straight to Auth — no guest browse mode |
| "First to discover" positioning | ❌ | No "You discovered them before everyone" discovery framing |
| Artist exclusivity signals | ❌ | No "OWNLN Exclusive" badge on tracks or artist profiles |
| Fan reward systems visible at discovery | ❌ | No teaser of reward system to motivate signup |
| Superior UX trust signal on landing | ⚠️ | Design is premium but no onboarding trust copy |

**Action Required:**
- Add a **Guest Preview Mode** — show the home screen with blurred player and a "Sign up free" overlay bar
- Add **"OWNLN Exclusive"** gold badge on tracks/artists that are platform-only
- Add **"🔥 Fans reward system"** teaser copy somewhere visible before signup to hook new users

---

### Stage 2 — Onboarding
*Goal: Create account, set preferences*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Email + social login | ✅ | AuthScreen has both |
| Role selection (Fan vs Artist) | ✅ | AuthScreen step 1 |
| Guest mode — browse limited before committing | ❌ | Not designed |
| Fan onboarding genre + mood preference selection | ✅ | FanOnboardingScreen — 3 steps |
| Auto-import music taste from other platforms | ❌ | No "Import from Spotify/Apple Music" option |
| Smart defaults based on referral source | ❌ | Not in design |
| Progress bar on onboarding steps | ✅ | FanOnboardingScreen has step indicator |
| Skip option for non-required steps | ⚠️ | Step indicator exists but no explicit "Skip" button visible |

**Action Required:**
- Add a **"Browse First"** button on AuthScreen below the signup buttons → leads to limited guest mode
- Add **"Import taste from Spotify"** as optional step 0 on FanOnboarding
- Add explicit **"Skip →"** ghost link on each optional onboarding step

---

### Stage 3 — Browse
*Goal: Explore by genre, mood, trending*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Genre categories + mood playlists | ✅ | FanHomeScreen mood pills + genre row |
| Trending charts | ✅ | "Trending Now" hero card + tracks |
| Artist-curated collections | ⚠️ | Only standard track rows — no "Curated by [Artist]" playlist cards |
| Fan-made playlists visible on browse | ⚠️ | Playlists exist (PlaylistScreen) but not surfaced on home browse |
| Discovery paths ("Late Night Vibes", "Workout Energy") | ❌ | Only raw mood tag filter — no themed collection cards |
| Regional/local scene hubs ("Pensacola Underground") | ❌ | No local/regional discovery section at all |
| "Underground Heat This Week" trending type | ❌ | Trending is generic — no culture-specific chart naming |
| Community-driven discovery ("Fans Like You") | ❌ | No social proof discovery cards |
| "People who finished this album also liked..." | ❌ | No social listening signals on browse |
| "Artists Rising Near You" location discovery | ❌ | Not in design |
| Browse by content type (music, films, live, freestyles, interviews, BTS) | ⚠️ | Music and podcasts exist; films, freestyles, interviews, BTS are absent |
| Artist pages with similar creators / collaborators / featured playlists | ⚠️ | ArtistPublicScreen exists but no "Similar Artists" or "Collaborators" section |
| Participatory discovery — fans influence culture | ❌ | No "Fan Charts" or vote/influence mechanic visible |

**Action Required (High Priority):**
- Add **Discovery Collection Cards** to FanHomeScreen: themed rows like "Late Night Vibes →", "Artists Rising Near You →", "Underground Heat This Week →" — each is a horizontal card rail, not just a list
- Add a **"Near You"** or **"Regional Scene"** section — even a single card like "🌆 Pensacola Underground" with a "Explore →" button
- Add **"Fans Like You Also Loved"** section — social proof row of 4 track/artist cards
- On ArtistPublicScreen — add **"Fans Also Follow"** section (3 artist avatars) and **"Featured Playlist by [Artist]"** card

---

### Stage 4 — Consume
*Goal: Stream music, watch video, listen to podcast*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Clean in-app player | ✅ | PlayerScreen — full controls, progress bar |
| Background playback (design signal) | ✅ | Mini player persistent bar exists |
| Queue management | ⚠️ | "Add to Playlist" button exists, no visible queue panel on player |
| Lyrics display | ⚠️ | "Show Lyrics" button exists but no lyrics panel UI designed |
| Album visuals | ⚠️ | Vinyl circle placeholder — no actual album art container |
| Artist notes / behind-the-scenes content | ❌ | No "Artist Note" or "Story behind this track" section on player |
| Credits display (producers, writers, engineers) | ❌ | No credits tab or section on player |
| Immersive visualizers | ❌ | No visualizer animation on player |
| Audio/video mode toggle | ❌ | No toggle to switch from audio to video version |
| Offline downloads (premium) | ❌ | No download button on tracks (even as locked/premium UI) |
| Fan reactions during premieres | ❌ | No premiere/live reaction UI |
| Synchronized community listening | ❌ | No "Listen Together" feature even as a teaser |
| Skip back/forward 15s buttons | ⚠️ | Only prev/next track buttons — no 15s skip controls |
| Cross-device sync indicator | ❌ | No "Playing on another device" UI |
| Unlockable fan reward content (commentary, alt versions) | ❌ | No "Unlock exclusive version" CTA on player |

**Action Required (High Priority):**
- Add **Lyrics Panel** — slide-up sheet with sample lyrics text and "Lyrics by [writer]" credit line
- Add **"Story Behind This Track"** — collapsible section below player controls with artist note text
- Add **Credits tab** — producer, mixer, writer listed as gold-tinted text rows
- Add **±15s skip buttons** (`« 15` and `15 »`) flanking the play button
- Add **Queue slide-up panel** — tap queue icon → list of upcoming tracks with drag reorder
- Add **"Download"** button on track row (padlocked for free users with "Go Pro" tooltip)

---

### Stage 5 — Follow
*Goal: Save artist, get notified of drops*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| One-click follow from artist pages | ✅ | Follow button on ArtistPublicScreen |
| Follow from during playback | ❌ | No follow button on PlayerScreen |
| Dedicated artist feed (releases, updates, events) | ⚠️ | "New From Artists You Follow" section on FanHomeScreen — but very minimal |
| Customizable notification preferences | ✅ | NotificationsScreen + SettingsScreen |
| Follower-only content signals | ❌ | No "Followers Only" badge/lock on any content |
| Fan tier badges for long-term followers | ❌ | No loyalty badge system visible anywhere |
| Artist voice notes / personalized updates | ❌ | No direct artist update format (separate from track releases) |
| Early access unlock for followers | ❌ | No "Early Access for Followers" UI element |
| Fan voting / listening events (follower exclusive) | ❌ | No voting or event mechanic visible |
| Visible fan recognition for early support | ❌ | No "Day-1 Supporter" or "Original Fan" badge UI |

**Action Required:**
- Add **Follow button on PlayerScreen** — small outlined follow button next to artist name
- Add **"Follower Only 🔒"** badge type to tracks/content on artist profile
- Add **Fan Tier Badge** chip to FanProfileScreen — e.g. gold "Day-1 Fan" or "Superfan" badge under name

---

### Stage 6 — Engage
*Goal: Comment, share, tip, message*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Comment on tracks | ❌ | No comment section on track or player at all |
| Live chat during streams/premieres | ❌ | OwnlnLiveScreen exists but no chat UI visible |
| Tipping from artist pages or during playback | ⚠️ | Wallet/subscribe exists, but no "Tip $1" quick-tap button |
| Fan-to-fan discussion boards | ✅ | FanfareScreen has forum threads |
| Collaborative playlists | ⚠️ | PlaylistScreen exists, no collaborative/shared editing UI |
| Reactions to moments within songs/videos | ❌ | No timestamp-based reaction or comment mechanic |
| Group listening sessions | ❌ | No "Listen Together" UI |
| Q&A events | ❌ | No Q&A format within community or artist profile |
| Contests / remix challenges | ❌ | No challenge/contest card UI |
| Artist-hosted watch parties | ❌ | No watch party feature in design |
| Reputation / trust system for positive participation | ❌ | No reputation score or trust level visible on profiles |
| Monetized messaging filters | ❌ | Not in design |
| Fan-moderated community spaces | ❌ | No moderator role/badge visible |

**Action Required (Medium Priority):**
- Add **"Tip Artist"** quick button to PlayerScreen and ArtistPublicScreen — small gold pill button: `💰 Tip`
- Add **Track Comments** as a slide-up panel on PlayerScreen — "💬 12 fans commented" tap target
- Add **Reaction bar** to PlayerScreen — emoji reactions row below progress bar
- Add **"Start Q&A"** card slot in CommunityScreen for artists (artist role only)
- Add **Challenge Card** to CommunityScreen — "🎤 Remix Challenge: Week 3 — Deadline Jun 30"

---

### Stage 7 — Purchase
*Goal: Buy merch, tickets, subscriptions*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Subscription tiers with clear benefits | ✅ | SubscribeScreen has 3 tiers |
| One-time track/album purchase | ✅ | Subscription screen shows track purchase option |
| In-app merch store | ✅ | MerchScreen + ArtistMerchStoreScreen |
| Integrated wallet for fans | ⚠️ | WalletScreen is artist-only — no fan wallet visible |
| "You supported artists with $48 this month" transparency | ❌ | No fan spending transparency widget anywhere |
| Digital collectibles / fan-owned assets | ❌ | No collectibles UI in design |
| Bundle purchase (album + merch + livestream) | ❌ | No bundle deal UI |
| Visible payout breakdown for trust ("artist gets 80%") | ⚠️ | Artist home shows "You keep 80–90%" — but fan never sees this |
| Wallet loyalty rewards for fans | ❌ | No fan loyalty points or cashback UI |
| Hybrid physical-digital experiences (hoodie unlocks music) | ❌ | No digital unlock trigger from physical merch purchase |
| Artist inventory / digital ownership visibility | ✅ | ArtistMerchStoreScreen has stock counts |

**Action Required:**
- Add **Fan Spending Summary card** to FanProfileScreen — "You've supported 3 artists · $48 this month" with gold breakdown
- Add **"Artist Receives 80%"** trust line on SubscribeScreen below each tier — e.g. small muted text: "Marcus Allen receives $0.80 of every $1.00"
- Add **Fan Wallet section** inside FanProfileScreen — tipping balance, purchase history, loyalty points earned
- Add **Digital Collectible teaser** on ArtistPublicScreen — "🏆 2 Collectibles Available" card that routes to a future collectibles screen

---

### Stage 8 — Retain
*Goal: Return for new releases*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Artist drop notifications | ✅ | NotificationsScreen exists |
| Community conversations driving return | ✅ | FanfareScreen, CommunityScreen |
| Discovery recommendations tailored to behavior | ⚠️ | Mood filter personalization exists but no "Based on your listening" label |
| Personal dashboard for supporter milestones | ❌ | FanProfileScreen is very minimal — no milestone tracker |
| Digital trophy case / vault | ❌ | No trophy case, collectibles vault, or achievement screen |
| Fan listening streaks | ❌ | No streak counter or daily listening reward UI |
| "You Discovered Them First" achievements | ❌ | No achievement/badge system |
| Artist project shares / community ownership | ❌ | No project shares or fan investment UI |
| Personalized culture report ("Trends you helped grow") | ❌ | No listening wrapped / culture report feature |
| Leaderboard systems | ❌ | No leaderboard for fans visible anywhere |
| Featured fan playlists driving return | ⚠️ | PlaylistScreen exists but fan playlists not featured on home |
| Rare collectibles with social flex value | ❌ | No collectibles system |
| Priority tickets / exclusive drops for loyal fans | ❌ | No "Early Access" or "Priority Drop" UI for retained fans |

**Action Required (High Priority for Retention):**
- Add **Fan Trophy Case section** to FanProfileScreen — horizontal scroll of achievement badges: "Day-1 Fan", "Top Supporter", "Explorer", "Streak: 7 days"
- Add **Listening Streak widget** to FanHomeScreen top area — "🔥 7-day streak · Keep it going"
- Add **"You Discovered Them First"** subtle badge on artist cards where fan followed before 1K followers
- Add a **"My Impact"** stats card to FanProfileScreen — "You've added 14 tracks to playlists · Tipped 3 artists · Shared 8 songs"

---

## Part 2 — Creator Journey Analysis

---

### Stage 1 — Discovery (Creator)
*Goal: Hear about OWNLN*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Clear differentiation from competitors | ⚠️ | FeaturesScreen exists but only accessible from inside app |
| 90/10 (or 80/20) split stated prominently | ⚠️ | Shown on artist home only — not visible at discovery/signup stage |
| "All resources to get further faster" positioning | ❌ | No landing or pre-signup value proposition screen |

**Action Required:**
- Add **Payout split** prominently to AuthScreen — below the artist role button: "Keep 80–90% of everything you earn"
- Add a **Pre-auth Features teaser** — single swipeable card on auth screen showing 3 platform differentiators

---

### Stage 2 — Onboarding (Creator)
*Goal: Create account, verify identity*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Email + social login | ✅ | AuthScreen |
| Role distinction clear | ✅ | AuthScreen role selection |
| No ID required at signup (only for payouts) | ⚠️ | No copy clarifying this — creates trust friction |
| Transparent data policy + no hidden fees stated | ❌ | Not visible anywhere in design |
| Split percentage stated upfront | ⚠️ | Only on artist home after full onboarding |

**Action Required:**
- Add **"No ID required to start — only for payouts"** small disclaimer on the artist role button
- Add **"0 hidden fees · Keep 80-90%"** as a trust badge row at bottom of AuthScreen

---

### Stage 3 — Setup (Creator)
*Goal: Build profile, link socials, set pricing*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Bio + photo upload | ✅ | ArtistOnboardingScreen step 1-2 |
| Genre + community tags | ✅ | ArtistOnboardingScreen step 3 |
| Social links | ✅ | ArtistOnboardingScreen step 4 |
| Payout setup during onboarding | ❌ | No payout/banking step in onboarding flow |
| AI-assisted bio generation | ❌ | No AI bio helper UI |
| AI metadata auto-fill | ❌ | Not in any upload or setup screen |
| Suggested pricing for subscription tiers | ❌ | No pricing recommendation in setup |
| Profile templates for different artist types | ❌ | No template selection |

**Action Required:**
- Add **Step 5** to ArtistOnboardingScreen — "Set Your Subscription Pricing" with suggested defaults and "Recommended: $1 / $3 / $5" preset buttons
- Add **"✨ Generate Bio with AI"** ghost button below the bio text area

---

### Stage 4 — Upload (Creator)
*Goal: Release music / podcast / video*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Drag-and-drop / file picker | ✅ | UploadScreen |
| Cover art upload | ✅ | UploadScreen |
| Metadata fields (title, genre, mood) | ✅ | UploadScreen |
| Release type selection | ✅ | UploadScreen |
| Bulk import from other platforms | ❌ | No "Import from DistroKid/TuneCore" option |
| AI-assisted metadata auto-fill | ❌ | No AI helper on upload form |
| File/format validation feedback | ⚠️ | No format requirement shown (WAV/MP3/FLAC specs) |
| Progress indicator for upload | ⚠️ | UI exists but no actual progress bar design visible |

**Action Required:**
- Add **"📁 Bulk Import"** button on ArtistLibraryScreen — "Import your catalog from DistroKid, TuneCore, or CD Baby"
- Add **"✨ Auto-fill from audio file"** button on UploadScreen — below the file picker
- Add **file spec text** under file picker: "Accepted: WAV, MP3, FLAC · Max 500MB"

---

### Stage 5 — Publish (Creator)
*Goal: Set metadata, tags, distribution options*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Go-live vs schedule toggle | ✅ | ReleaseSchedulingScreen + UploadScreen |
| Platform selection (exclusive vs external distribution) | ⚠️ | No "OWNLN Exclusive / Also distribute externally" toggle |
| Licensing / rights options | ❌ | No licensing/rights field in upload or publish flow |
| Preview before publishing | ⚠️ | No preview/confirmation step before going live |
| Instant URL generation | ❌ | No shareable link shown immediately after publish |
| Social auto-post option | ❌ | No "Share to Instagram/Twitter after publishing" toggle |

**Action Required:**
- Add **"Distribution"** toggle to UploadScreen: `OWNLN Exclusive` / `OWNLN + External` with explanation copy
- Add **"Your share link will be ready instantly"** confirmation line in UploadScreen submit area
- Add **Social Auto-Post** toggle: "📱 Auto-share to Instagram story when published"

---

### Stage 6 — Promote (Creator)
*Goal: Share to fans, track pre-saves*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| In-app share button | ✅ | Share icon on PlayerScreen |
| Generated smart link | ❌ | No smart link screen or shareable URL UI |
| Social auto-post | ❌ | Not in design |
| Pre-save campaign | ❌ | No pre-save functionality visible |
| Pre-made share templates | ❌ | No visual share card generator |
| Click/source tracking on shared links | ❌ | Not in OPI or any analytics screen |
| Fan referral rewards | ❌ | Not in design |

**Action Required (Medium Priority):**
- Add **"Promote This Track"** button on track rows in ArtistLibraryScreen → opens a bottom sheet with:
  - Generated share card (track art + title + QR)
  - Copy link button
  - Share to Instagram/Twitter buttons
  - Pre-save toggle (enable/disable)
- Add **Promo Analytics** mini card to OpiScreen — "Your share link · 248 clicks · 34 new followers from link"

---

### Stage 7 — Monetize (Creator)
*Goal: Earn from streams, tips, subscriptions*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Per-stream payout visible | ✅ | WalletScreen + ArtistHomeScreen revenue breakdown |
| Merch revenue | ✅ | Revenue breakdown includes merch |
| Exclusive content monetization | ✅ | Subscriber-only content gating in SubscribeScreen |
| Tips / direct fan payments | ⚠️ | No "tip received" notification design or tip feed visible |
| Transparent earnings dashboard | ✅ | WalletScreen + OpiScreen |
| Instant tip notification | ❌ | NotificationsScreen exists but no tip notification design |
| Tax document auto-generation teaser | ❌ | No "1099 auto-generated" mention anywhere |
| Low $10 payout threshold stated | ❌ | WalletScreen doesn't show minimum payout threshold |
| 30-day rolling delay explanation | ❌ | No payout timing explanation in wallet |

**Action Required:**
- Add **"Minimum payout: $10 · Processed within 3 business days"** to WalletScreen
- Add **"📄 Tax documents auto-generated"** info chip in WalletScreen
- Add **Tip notification type** to NotificationsScreen — "💰 Jamie D tipped you $5 on Midnight Gold"

---

### Stage 8 — Analyze (Creator)
*Goal: View stats, understand audience*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Stream count + revenue + demographics | ✅ | OpiScreen has comprehensive analytics |
| Geography + peak times + traffic source | ✅ | OpiScreen covers these |
| Simplified presentation | ✅ | OpiScreen is clean and well-organized |
| Benchmark against similar artists | ❌ | No "Your peers average X — you're Y% above" benchmark |
| Exportable reports | ❌ | No export/download button on OpiScreen |
| AI "what to do next" recommendation | ❌ | No AI insight or recommendation card |

**Action Required:**
- Add **"Peer Benchmark"** row to OpiScreen — "Artists like you average 12K streams/month · You: 48K 🔥"
- Add **"💡 AI Insight"** card to OpiScreen — "Your engagement peaks Thursday 8–10pm. Schedule your next release then."
- Add **"Export Report"** ghost button at bottom of OpiScreen

---

### Stage 9 — Engage (Creator)
*Goal: Reply to fans, build community*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| DMs and comments | ⚠️ | Community + Fanfare exist but no direct reply/DM screen |
| Community posts (announcements, polls) | ⚠️ | CommunityScreen has basic cards, no post creation UI visible |
| Livestream with chat | ⚠️ | OwnlnLiveScreen exists but no live chat panel designed |
| Fan tiering by engagement level | ❌ | No fan tier segmentation visible on any screen |
| Bulk reply tools | ❌ | Not in design |
| Community moderation by trusted fans | ❌ | No moderator badge or mod tools visible |
| Monetized messaging (future) | ❌ | Not in design |
| Too many messages problem — filters | ❌ | No message priority filter UI |

**Action Required:**
- Add **"Post Update"** CTA to ArtistScreen — gold ghost button "📣 Post to Fans" → opens a create-post modal with type selector: Announcement / Poll / Behind-the-Scenes / Merch Drop
- Add **Fan Tier Labels** to any fan list display — "Superfan", "Supporter", "Follower" badge chips
- Add **"Priority Messages"** tab in a future DM screen — filter: Superfans / Supporters / All

---

### Stage 10 — Retain (Creator)
*Goal: Return to upload next project*

| Journey Requirement | Status | Notes |
|---------------------|--------|-------|
| Community built on platform | ✅ | Multiple community screens |
| Easy upload tools | ✅ | UploadScreen, SchedulingScreen |
| Visible growth tracking | ✅ | OpiScreen + ArtistHomeScreen stats |
| Progress tracking with goals | ❌ | No "Goal: 100K streams by Jul" progress tracker |
| Exclusive access (live shows, touring tools) | ❌ | No touring/live event booking teaser |
| Personal check-in system (platform-to-creator) | ❌ | No check-in notification or milestone congratulations UI |
| Burnout prevention / wellness signals | ❌ | Not in design |
| Market research insights for creators | ❌ | No "Trending in your genre" market signal card |

**Action Required:**
- Add **Goal Tracker widget** to ArtistHomeScreen — "🎯 Goal: 50K streams · 48.2K / 50K · 96% complete"
- Add **Milestone Congratulations notification** type — "🎉 You hit 100K total streams! Here's your milestone badge."
- Add **"Trending in R&B This Week"** market signal card to OpiScreen or ArtistHomeScreen

---

## Summary Table — Priority Matrix

### Fan Journey Gaps

| Gap | Priority | Screen to Fix/Add |
|-----|----------|-------------------|
| Track comments panel | 🔴 High | PlayerScreen |
| Lyrics panel UI | 🔴 High | PlayerScreen |
| ±15s skip buttons | 🔴 High | PlayerScreen |
| Queue slide-up panel | 🔴 High | PlayerScreen |
| Discovery collection rows ("Late Night Vibes") | 🔴 High | FanHomeScreen |
| Regional scene hub section | 🔴 High | FanHomeScreen |
| "Fans Like You" social proof row | 🔴 High | FanHomeScreen |
| Fan Trophy Case / Achievements | 🔴 High | FanProfileScreen |
| Listening streak widget | 🔴 High | FanHomeScreen |
| Tip Artist button | 🟡 Medium | PlayerScreen + ArtistPublicScreen |
| Fan spending transparency card | 🟡 Medium | FanProfileScreen |
| Follow button on PlayerScreen | 🟡 Medium | PlayerScreen |
| "Artist Receives 80%" trust line | 🟡 Medium | SubscribeScreen |
| Guest browse mode | 🟡 Medium | AuthScreen |
| Download button (Pro locked) | 🟡 Medium | TrackRow component |
| Artist notes / credits on player | 🟡 Medium | PlayerScreen |
| Digital collectibles teaser | 🟢 Low | ArtistPublicScreen |
| Remix/challenge cards | 🟢 Low | CommunityScreen |
| "You discovered them first" badge | 🟢 Low | Search artist cards |

### Creator Journey Gaps

| Gap | Priority | Screen to Fix/Add |
|-----|----------|-------------------|
| Payout split on AuthScreen (pre-signup) | 🔴 High | AuthScreen |
| AI bio generator button | 🔴 High | ArtistOnboardingScreen |
| Subscription pricing step in onboarding | 🔴 High | ArtistOnboardingScreen |
| Goal tracker widget | 🔴 High | ArtistHomeScreen |
| AI insight card on analytics | 🔴 High | OpiScreen |
| "Post to Fans" CTA | 🔴 High | ArtistScreen |
| Share / Promote track bottom sheet | 🟡 Medium | ArtistLibraryScreen |
| Payout threshold + tax docs in wallet | 🟡 Medium | WalletScreen |
| Tip received notification type | 🟡 Medium | NotificationsScreen |
| Peer benchmark on analytics | 🟡 Medium | OpiScreen |
| Bulk import catalog button | 🟡 Medium | ArtistLibraryScreen |
| Distribution toggle (exclusive vs external) | 🟡 Medium | UploadScreen |
| File format specs on upload | 🟢 Low | UploadScreen |
| Export report button | 🟢 Low | OpiScreen |
| Milestone congratulation notification | 🟢 Low | NotificationsScreen |

---

## Screens That Are Well Covered ✅

These screens are strong and largely match their journey stage requirements:

| Screen | Journey Stage | Coverage |
|--------|--------------|---------|
| AuthScreen | Onboarding | Strong — role selection, social login, clean UX |
| ArtistOnboardingScreen | Setup | Strong — 4 steps, photo/bio/genres/socials |
| FanOnboardingScreen | Browse preference | Strong — 3 steps, genre + mood + follow |
| ArtistHomeScreen | Monetize / Analyze | Strong — OPI score, revenue breakdown, quick actions |
| OpiScreen | Analyze | Strong — comprehensive analytics with 5 categories |
| WalletScreen | Monetize | Strong — balance, breakdown, transaction history |
| SubscribeScreen | Purchase | Strong — 3 tier pricing, benefit lists |
| ReleaseSchedulingScreen | Publish | Strong — calendar, status badges, edit/cancel |
| CommunityScreen | Engage (hub) | Strong — 4 community entry points |
| FanfareScreen | Engage (forum) | Good — threads, replies, post structure |
| MerchScreen + ArtistMerchStoreScreen | Purchase | Good — product grid, stock, Shopify indicators |
| NotificationsScreen | Follow / Retain | Good — notification list, unread badges |
| PlaylistScreen | Consume / Follow | Good — track list, play all, shuffle |
| EpisodePageScreen | Consume | Strong — clips, gating, full episode |
| AdminScreen | Platform ops | Good — moderation, approval, payout controls |

---

## Top 10 Screens to Improve First

Based on journey impact and user frequency:

1. **PlayerScreen** — Add lyrics panel, ±15s skips, queue panel, artist notes, comments, tip button, follow button
2. **FanHomeScreen** — Add discovery collection rows, regional section, "Fans Like You", listening streak
3. **FanProfileScreen** — Add trophy case, fan spending card, fan wallet section, impact stats
4. **AuthScreen** — Add payout split trust line, guest browse option, pre-signup differentiators
5. **ArtistOnboardingScreen** — Add pricing step, AI bio button
6. **ArtistScreen (own profile)** — Add "Post to Fans" CTA
7. **OpiScreen** — Add AI insight card, peer benchmark, export button
8. **WalletScreen** — Add payout threshold, tax doc teaser, tip received history
9. **ArtistPublicScreen** — Add similar artists section, collectibles teaser, fan tier badges
10. **UploadScreen** — Add distribution toggle, format specs, social auto-post toggle

---

*Analysis based on: Fan Journey.csv · Creator Journey.csv · index.html prototype (39 screens, ~2100 lines)*
*Generated: May 2026 · For Sprint planning and Flutter development specification*
