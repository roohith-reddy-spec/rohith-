# KAYDEN — Premium Cinematic OTT Streaming Platform

> *"Your world. Your mood. Your stories."*

**KAYDEN** is a bespoke, production-ready MERN streaming platform designed for auteur cinema, high-concept serialized drama, and mood-driven narrative discovery. Built with an original editorial identity, KAYDEN rejects generic AI dashboards and cookie-cutter streaming templates in favor of warm, human-designed typography, photographic depth, and sophisticated cinematic curation.

---

## 1. Key Differentiating Features

### ✦ Mood & Intention Discovery Engine
Unlike platforms relying solely on opaque watch-history algorithms, KAYDEN introduces emotional discovery:
1. **Mood Selection**: Choose from 16 emotional harmonics (e.g. *Contemplative, Electric, Melancholic, Warmth, Nostalgic, Adrenaline, Whimsical, Eerie, Romantic, Hopeful, Adventurous*).
2. **Mood Intention**: Specify what you yearn to experience (*"I want to feel better"*, *"I want something exciting"*, *"I want inspiration"*, *"I want to cry"*, etc.).
3. **Personalized Home Adaptation**: Dynamic backend ranking recalibrates genres, narrative tempos, and curator recommendations to mirror the active frequency.

### ✦ Multi-Profile Spaces
- Distinct profiles: **Adult**, **Kids** (filtered family/animation vault), **Guest**, and custom spaces.
- Independent watchlists, viewing progress, mood preferences, and language inclinations.
- Designed with forward-compatibility for dynamic video avatars.

### ✦ Professional Theatrical Player
- Responsive HTML5 cinema player with auto-fading controls.
- Interactive seek scrubber with real-time buffered indicators.
- 10-second skip backwards and forwards (`←` / `→`).
- Playback speed adjustment (0.75x, 1x, 1.25x, 1.5x) and streaming resolution switcher (4K Master, 1080p, 720p).
- Subtitle rendering with WebVTT closed captions.
- Background progress synchronization that persists viewing timestamps to MongoDB every 5 seconds.
- Keyboard shortcuts: `Space` (Play/Pause), `F` (Fullscreen), `M` (Mute/Unmute), `←`/`→` (Seek).

### ✦ Polyglot World Cinema & Sovereign Territories
- Explorable across 17+ languages (English, French, Japanese, Korean, Hindi, Spanish, German, Italian, Telugu, Tamil, Malayalam, Kannada, Bengali, Portuguese, Chinese, Arabic, Turkish).
- Discoverable across 12+ national territories with descriptions of their cinema traditions.

### ✦ The Auteur Guild
- Dedicated creator profiles for Directors, Screenwriters, and Performers with full linked filmographies.

### ✦ Membership & Patronage
- Multi-tier subscriptions: *KAYDEN Standard*, *KAYDEN Cinema Club (4K HDR)*, and *KAYDEN Premier Opus*.

---

## 2. Technology Stack

- **Frontend**:
  - React 18 + Vite
  - React Router DOM v6
  - Context API (`AuthContext`, `ProfileContext`, `PlayerContext`, `ThemeContext`)
  - Axios with JWT & Active-Profile interceptors
  - Lucide React iconography
  - Bespoke Editorial CSS Design System (Cormorant / Playfair Display / Plus Jakarta Sans)
- **Backend**:
  - Node.js & Express.js
  - RESTful API Architecture with Modular Controllers and Services
  - JWT Authentication & Bcrypt Password Hashing
  - Morgan Logging & Helmet Security Headers
- **Database**:
  - MongoDB & Mongoose Object Modeling
  - Comprehensive schemas with indexes, virtuals, and relational references
  - Automatic seed script with legal public-domain / creative commons demo feeds

---

## 3. Project Directory Structure

```text
mern-project/
│
├── client/
│   ├── src/
│   │   ├── assets/             # Branding, icons, logos
│   │   ├── components/         # 24 modular, reusable UI components
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Button.jsx
│   │   │   ├── Modal.jsx
│   │   │   ├── SearchBar.jsx
│   │   │   ├── MovieCard.jsx
│   │   │   ├── SeriesCard.jsx
│   │   │   ├── ContentRow.jsx
│   │   │   ├── HeroSection.jsx
│   │   │   ├── GenreCard.jsx
│   │   │   ├── LanguageCard.jsx
│   │   │   ├── CountryCard.jsx
│   │   │   ├── PersonCard.jsx
│   │   │   ├── ProfileCard.jsx
│   │   │   ├── ProfileSelector.jsx
│   │   │   ├── MoodCard.jsx
│   │   │   ├── MoodSelector.jsx
│   │   │   ├── Rating.jsx
│   │   │   ├── VideoPlayer.jsx
│   │   │   ├── EpisodeList.jsx
│   │   │   ├── SeasonSelector.jsx
│   │   │   ├── WatchProgress.jsx
│   │   │   ├── LoadingState.jsx
│   │   │   ├── ErrorState.jsx
│   │   │   ├── EmptyState.jsx
│   │   │   └── ProtectedRoute.jsx
│   │   ├── pages/              # 23 dedicated pages
│   │   │   ├── LandingPage.jsx
│   │   │   ├── LoginPage.jsx
│   │   │   ├── RegisterPage.jsx
│   │   │   ├── ProfileSelectionPage.jsx
│   │   │   ├── CreateProfilePage.jsx
│   │   │   ├── MoodSelectionPage.jsx
│   │   │   ├── MoodIntentionPage.jsx
│   │   │   ├── HomePage.jsx
│   │   │   ├── DiscoverPage.jsx
│   │   │   ├── GenresPage.jsx
│   │   │   ├── LanguagesPage.jsx
│   │   │   ├── CountriesPage.jsx
│   │   │   ├── PeoplePage.jsx
│   │   │   ├── MovieDetailsPage.jsx
│   │   │   ├── SeriesDetailsPage.jsx
│   │   │   ├── WatchPage.jsx
│   │   │   ├── SearchPage.jsx
│   │   │   ├── MySpacePage.jsx
│   │   │   ├── WatchlistPage.jsx
│   │   │   ├── HistoryPage.jsx
│   │   │   ├── SettingsPage.jsx
│   │   │   ├── SubscriptionPage.jsx
│   │   │   └── NotFoundPage.jsx
│   │   ├── layouts/
│   │   │   ├── MainLayout.jsx
│   │   │   ├── AuthLayout.jsx
│   │   │   └── StreamingLayout.jsx
│   │   ├── services/           # Axios API services
│   │   ├── hooks/              # Custom React hooks
│   │   ├── context/            # Global React Contexts
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css           # Editorial design system
│   ├── index.html
│   ├── vite.config.js
│   ├── package.json
│   └── .env
│
├── server/
│   ├── config/
│   │   └── db.js               # MongoDB connection
│   ├── controllers/            # 14 modular controllers
│   ├── middleware/             # Auth, error, logging, validation
│   ├── models/                 # 13 Mongoose schemas
│   │   ├── User.js
│   │   ├── Profile.js
│   │   ├── Movie.js
│   │   ├── Series.js
│   │   ├── Episode.js
│   │   ├── Genre.js
│   │   ├── Language.js
│   │   ├── Country.js
│   │   ├── Person.js
│   │   ├── Mood.js
│   │   ├── Watchlist.js
│   │   ├── WatchHistory.js
│   │   └── Subscription.js
│   ├── routes/                 # 15 Express route files
│   ├── services/               # Recommendation & business logic
│   ├── utils/                  # JWT, passwords, responses, seeder
│   │   ├── seedData.js
│   │   └── seedDatabase.js
│   ├── app.js
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── .gitignore
├── README.md
└── package.json
```

---

## 4. Environment Variables

### Server (`server/.env`):
```env
PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/kayden_ott
JWT_SECRET=kayden_production_jwt_secret_key_8923489123891283
JWT_EXPIRES_IN=7d
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```

### Client (`client/.env`):
```env
VITE_API_URL=http://localhost:5000/api
```

---

## 5. Quick Start & Installation

### Step 1: Install Dependencies
From the project root:
```bash
# In server directory
cd server
npm install

# In client directory
cd ../client
npm install
```

### Step 2: Seed the Database
Ensure your MongoDB service is running, then run the automated seeder:
```bash
cd server
npm run seed
```
> This populates curated feature films, serialized dramas, multi-season episodes, 20 genres, 17 languages, 12 countries, auteurs, and creates a demo user account.

**Pre-seeded Demo Patron:**
- **Email**: `demo@kayden.tv`
- **Password**: `Kayden123!`

### Step 3: Run the Development Servers
In two separate terminals:

**Terminal 1 (Backend API on http://localhost:5000):**
```bash
cd server
npm run dev
```

**Terminal 2 (Frontend Client on http://localhost:5173):**
```bash
cd client
npm run dev
```

---

## 6. REST API Endpoints Overview

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| **POST** | `/api/auth/register` | Register new account & default profiles |
| **POST** | `/api/auth/login` | Authenticate with JWT token |
| **GET** | `/api/auth/me` | Retrieve authenticated patron & profiles |
| **GET** | `/api/profiles` | List profiles belonging to current user |
| **POST** | `/api/profiles` | Create new space profile (max 5) |
| **PUT** | `/api/profiles/:id` | Update profile preferences & mood |
| **DELETE**| `/api/profiles/:id` | Remove non-default profile |
| **GET** | `/api/movies` | Filter feature films by genre, language, country, mood |
| **GET** | `/api/movies/:id` | Get movie details & similar recommendations |
| **GET** | `/api/series` | Filter serialized drama catalogues |
| **GET** | `/api/series/:id` | Get series details with season & episode breakdown |
| **GET** | `/api/moods` | Retrieve 16 curated moods |
| **POST** | `/api/moods/profile` | Synchronize active mood & intention |
| **GET** | `/api/recommendations/home` | Generate personalized editorial homepage feed |
| **GET** | `/api/search` | Search cross-entity (movies, series, cast, directors) |
| **GET** | `/api/watchlist` | Get saved titles for active profile |
| **POST** | `/api/watchlist` | Add title to My Space |
| **DELETE**| `/api/watchlist/:id` | Remove title from My Space |
| **POST** | `/api/history/progress` | Sync seconds watched & completion status |
| **GET** | `/api/history/continue` | Retrieve uncompleted continue-watching items |
| **GET** | `/api/subscriptions/plans`| Get membership tiers and pricing |

---

## 7. Production Build Verification

To compile the optimized client distribution:
```bash
cd client
npm run build
```
Generates production bundle in `client/dist/` with full asset optimization.

---

## 8. License
KAYDEN Streaming Atelier — Commercial Architecture.
