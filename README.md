# 🎬 Funverse

A premium movie discovery app built with **React**, **Vite**, **Firebase**, and **TMDB API**. Browse trending movies, search thousands of titles, manage your personal watchlist, and enjoy a stunning cinema-inspired UI.

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-6-646CFF?logo=vite&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-12-FFCA28?logo=firebase&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)

## ✨ Features

- 🔍 **Movie Search & Discovery** — Search and browse movies powered by TMDB API
- 🔥 **Trending Movies** — See what's trending based on community search activity (tracked via Firebase)
- 📝 **Personal Watchlist** — Save movies, view stats (total, avg rating, top year), and manage your collection
- 👤 **User Authentication** — Email/password sign-up & sign-in, plus Google Sign-In via Firebase Auth
- 🎬 **Movie Details** — Full movie pages with cast, videos, production info, and tabbed navigation
- 🎨 **Premium UI** — Cinema-noir design with glassmorphism, smooth animations, and a red-tinted color palette
- ⚡ **Fast Performance** — Built with Vite for instant HMR and optimized production builds
- 🔔 **Toast Notifications** — Elegant feedback for user actions (add/remove watchlist, auth events)

## 🛠️ Tech Stack

| Layer                | Technology                       |
| -------------------- | -------------------------------- |
| **Frontend**         | React 19, Vite 6, Tailwind CSS 4 |
| **Backend / BaaS**   | Firebase (Auth, Firestore)       |
| **API**              | The Movie Database (TMDB)        |
| **Routing**          | React Router DOM v6              |
| **State Management** | React Context API                |
| **Fonts**            | Inter, Space Grotesk, Bebas Neue |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- A [Firebase](https://firebase.google.com/) project
- A [TMDB API](https://developer.themoviedb.org/) read access token

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/PrashantJaybhaye/React-Movie-v2.git
   cd React-Movie-v2
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Configure Firebase**
   - Create a project in [Firebase Console](https://console.firebase.google.com/)
   - Enable **Authentication** → Email/Password and Google sign-in providers
   - Create a **Firestore Database** (the app uses a `metrics` collection for search tracking)
   - Add `localhost` to your authorized domains

4. **Start the development server**
   ```bash
   npm run dev
   ```
   The app will be available at `http://localhost:5173`

## 📁 Project Structure

```
src/
├── components/
│   ├── Header.jsx          # Glassmorphism navbar with auth modal
│   ├── Home.jsx            # Hero section, trending carousel, movie grid
│   ├── MovieCard.jsx       # Animated movie card with hover effects
│   ├── MovieDetail.jsx     # Full movie page with tabs (overview, cast, details, videos)
│   ├── Search.jsx          # Search bar with focus animations
│   ├── Watchlist.jsx       # Watchlist page with stats and movie grid
│   ├── WatchlistButton.jsx # Add/remove watchlist toggle button
│   ├── Profile.jsx         # User profile with stats and account details
│   ├── Spinner.jsx         # Loading spinner
│   └── Toast.jsx           # Toast notification system
├── context/
│   ├── AuthContext.jsx     # Firebase Auth state management
│   ├── WatchlistContext.jsx# Watchlist state with Firestore persistence
│   └── ToastContext.jsx    # Toast notification state
├── utils/
│   ├── auth.js             # Auth helper functions (display name, initials)
│   ├── mockMovies.js       # Fallback mock data when API is unavailable
│   └── tmdb-test.js        # TMDB API connection tester
├── firebase.js             # Firebase config and Firestore helpers
├── App.jsx                 # Router and app layout
├── main.jsx                # App entry point
└── index.css               # Global styles, theme, animations, components
```

## 📱 Pages & Routes

| Route        | Page         | Description                                         |
| ------------ | ------------ | --------------------------------------------------- |
| `/`          | Home         | Hero section, search, trending carousel, movie grid |
| `/movie/:id` | Movie Detail | Full movie info with cast, videos, tabs             |
| `/watchlist` | Watchlist    | Personal movie collection with stats                |
| `/profile`   | Profile      | User account details, stats, actions                |

## 🎨 Design System

The app uses a **cinema-noir** aesthetic with a red-tinted color palette:

- **Background**: Deep dark red (`#160000`)
- **Accent**: Cinema red (`#e50914`) with coral highlights (`#ff3b3f`)
- **Text**: Warm light pink (`#FECECE`)
- **Typography**: Space Grotesk for headings, Inter for body text
- **Effects**: Glassmorphism, stagger animations, hover glow effects, smooth transitions

## 📜 Available Scripts

| Command           | Description              |
| ----------------- | ------------------------ |
| `npm run dev`     | Start development server |
| `npm run build`   | Build for production     |
| `npm run preview` | Preview production build |
| `npm run lint`    | Run ESLint               |

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Made with ❤️ by [Prashant Jaybhaye](https://github.com/PrashantJaybhaye)
