# 🎨 K5 Studio — Portfolio Website

Personal portfolio website for **Jakub Drużbiński (K5 Studio)** — showcasing programming, graphic design, video, and 3D projects.

**👉 [https://k5studio.dev/](https://k5studio.dev/)**

![Main Page Image](https://raw.githubusercontent.com/kubadoPL/K5-Studio/main/images/MainPageUpdated.png)

---

## ✨ Features

### 🖼️ Dynamic Project Showcase
- **Data-Driven Slideshow**: All projects loaded from `projects.json` — no HTML editing needed to add or reorder projects.
- **Rich Project Cards**: Each slide displays a thumbnail, icon, description, tags, visibility badges (🔓 Public / 🔒 Private / 💼 Commissioned), and popularity indicators (🔥 Popular).
- **Action Buttons**: Direct links to live demos, Roblox games, Steam Workshop, YouTube trailers, and source code.

### 📊 Live Statistics Integration
Real-time stats fetched from multiple APIs and displayed as interactive stat tiles:
- **Roblox Game Stats**: Total visits, currently playing, likes, and favorites — pulled via Roblox Games API proxy.
- **Steam Workshop Stats**: Lifetime subscribers, current subscribers, and favorites — via Steam API.
- **Radio GAMING Listeners**: Live listener count with Discord avatar display for online users across all stations.
- **Radio GAMING Stats**: Registered users, top listener time, total songs tracked, total listening time, and unique anonymous users.
- **Server Uptime**: Live-updating uptime counter (days/hours/minutes/seconds) with client-side ticker.
- **Running Services**: Count of active Discord bots and web services on the backend.
- **FormBot Stats**: Online users, total forms submitted, and total questions answered (all-time).
- **Portfolio Page Stats**: Total page views and unique visitors displayed in the footer.

### 🎬 Immersive Design
- **Hero Video Background**: Full-screen looping video with overlay and scroll indicator.
- **Typing Animation**: Animated subtitle with rotating text using a custom typewriter effect.
- **Scroll Reveal Animations**: Sections and elements animate in on scroll (fade, slide, zoom) with configurable delays.
- **Smooth Transitions**: CSS-powered slide transitions with active/exit states for the project slideshow.
- **Noise Overlay**: Subtle grain texture for visual depth.

### 📝 Reviews Section
- **Fiverr Reviews**: Showcases real client reviews with avatars, ratings (star system), country flags, dates, pricing, and links to the original Fiverr gig.

### 📬 Contact Section
- **Contact Cards**: Animated cards linking to email, Fiverr, GitHub, and LinkedIn.
- **Multiple Email Addresses**: Personal and professional (Game Changer) email links.

### 🔧 Technical Details
- **Pure Vanilla Stack**: HTML5, CSS3, and JavaScript — no frameworks, no build tools.
- **Google Fonts**: Uses Inter font family (weights 300–900).
- **Responsive Design**: Mobile-friendly layout with CSS media queries.
- **SEO Optimized**: Proper meta tags, semantic HTML, descriptive title.
- **API-Powered Stats**: Stats fetched from the [Discord Bot Launcher Manager](https://github.com/kubadoPL/Discord-Bot-Launcher-Manager) backend (`/K5ApiManager`, `/DiscordAuthChatApi`) and external APIs (Roblox, Steam, Fairgames).
- **Stat Persistence**: Page views and unique visitors tracked via the `service_stats` API (public service: `k5portfolio`).

---

## 🗂️ Project Structure

```
k5-studio-portfolio-webpage/
├── index.html          # Main page with all sections and JS logic
├── styles.css          # Complete styling (35KB+)
├── projects.json       # Project data (slides, stats config, buttons, tags)
├── images/             # Thumbnails, icons, flags, logos
│   ├── thumbails/      # Project screenshot thumbnails
│   ├── icons/          # Contact & UI icons
│   └── Flags/          # Country flags for reviews
└── videos/             # Hero background video
```

---

## 📋 Adding a New Project

Edit `projects.json` and add an entry:

```json
{
    "key": "my-project",
    "title": "My Awesome Project",
    "thumbnail": "images/thumbails/my-project.png",
    "icon": "images/my-project-icon.png",
    "description": "Description of the project.",
    "buttons": [
        { "label": "Visit Website", "url": "https://example.com" }
    ],
    "tags": ["🐍 Python", "🌐 HTML"],
    "visibility": "public",
    "popular": true
}
```

Optional stat fields: `universeId` (Roblox), `steamWorkshopId` (Steam), `radioStations` (Radio GAMING listeners), `showRadioStats`, `showUptime`, `showRunningServices`, `showFormbotStats`, `fairgames` + `placeId`.

Set `"hideProject": true` to hide a project from the slideshow without removing its data.

---

## 🛠️ Built With

- **HTML5** / **CSS3** / **JavaScript** (Vanilla)
- **Google Fonts** (Inter)
- **Backend APIs**: [Discord Bot Launcher Manager](https://github.com/kubadoPL/Discord-Bot-Launcher-Manager)
- **External APIs**: Roblox Games API, Steam Workshop API, Fairgames API

---

© 2026 Jakub Drużbiński — K5 Studio
