# Landing Page Ekosistem Data Jateng

Ekosistem Data Jateng is a high-performance, statically generated landing page that serves as the centralized digital gateway for the Central Java Provincial Government's data services. 

Rather than acting as a heavy monolithic application, this project is architected strictly as a sleek, lightning-fast presentation layer. It seamlessly directs users to three primary specialized portals:
- **Open Data Jateng** (Data Terbuka)
- **Satu Data Jateng** (Data Terintegrasi)
- **Satu Peta Jateng** (Data Spasial)

The landing page establishes immediate institutional trust through a modern, professional, and user-friendly UI/UX design.

## 🏗️ Architecture & Tech Stack

This project prioritizes instant load times, SEO optimization, and an excellent developer experience by utilizing a modern static site generation (SSG) approach. It's built to be blazing fast and highly responsive.

- **Core Framework**: [Astro 5](https://astro.build/)
  - Chosen for its zero-JS-by-default output, ensuring the gateway loads instantaneously across all devices, even on slower mobile networks.
- **Styling Engine**: [Tailwind CSS v4](https://tailwindcss.com/)
  - Implemented via a modern CSS-first configuration (`@theme` variables in `global.css`) ensuring strict adherence to the project's color palette (Orange, Blue, Green accents) and typography tokens without CSS bloat.
- **Interactivity**: Vanilla JavaScript
  - Features like Intersection Observer API (for native CSS scroll reveal animations), active section nav highlighting, and mobile menu toggling are written in pure Vanilla JS, eliminating the need for heavy external animation libraries like Framer Motion or GSAP.

## ✨ Key Features

- **Modern Glassmorphism & Gradients**: Subtle UI aesthetics that feel premium and trustworthy.
- **Responsive Snap Scrolling**: Sections perfectly snap to the screen height (`calc(100vh - 5rem)`) for a distraction-free, app-like reading experience.
- **Micro-Animations**: Uses staggered reveals, floating images, and gentle glow effects to make the interface feel alive.
- **Dynamic Navbar**: Features a backdrop-blurred sticky header that automatically tracks and highlights the active section the user is currently reading.

## 📂 Project Structure

```text
/
├── public/                 # Static assets (Favicons, etc.)
├── src/
│   ├── assets/             # Local images, illustrations, SVG icons, and Fonts
│   ├── components/         # Astro components (Navbar, Hero, GatewaySection, Footer, etc.)
│   ├── layouts/            # Global HTML wrappers (Layout.astro with Meta/OG tags)
│   ├── pages/              # Routing pages (index.astro)
│   └── styles/             # Global CSS (Tailwind entry, @theme, custom animations)
├── astro.config.mjs        # Astro configuration file
├── package.json            # Project dependencies and scripts
└── README.md               # This documentation
```

## 🚀 Getting Started

To run this project locally, follow these steps:

### Prerequisites

- Node.js `v22.12.0` or higher
- npm (Node Package Manager)

### Installation

1. Clone the repository and navigate to the project directory:
   ```bash
   cd landing-page-data-jateng
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```

### Running Locally

Start the local development server:
```bash
npm run dev
```
The site will be available at `http://localhost:4321`.

### Building for Production

To create an optimized production build:
```bash
npm run build
```
This will compile your site to static HTML/CSS/JS in the `./dist/` folder, ready to be deployed to any static host (Vercel, Netlify, Nginx, etc.).

You can preview the production build locally using:
```bash
npm run preview
```

## 🎨 Theme Configuration

The project's design system is centralized in `src/styles/global.css` using Tailwind v4's new CSS-native configuration. 

You can easily modify:
- **Colors**: `--color-orange-primary`, `--color-blue-primary`, `--color-green-primary`
- **Typography**: Uses local variable fonts (`Inter` and `Plus Jakarta Sans`)
- **Animations**: Search for classes like `.reveal-up`, `.reveal-left`, and `.glass-card`
