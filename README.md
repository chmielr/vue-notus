# Vue Notus

![version](https://img.shields.io/badge/version-1.1.0-blue.svg) ![license](https://img.shields.io/badge/license-MIT-blue.svg) [![GitHub issues open](https://img.shields.io/github/issues/creativetimofficial/vue-notus.svg)](https://github.com/creativetimofficial/vue-notus/issues?q=is%3Aopen+is%3Aissue) [![GitHub issues closed](https://img.shields.io/github/issues-closed-raw/creativetimofficial/vue-notus.svg)](https://github.com/creativetimofficial/vue-notus/issues?q=is%3Aissue+is%3Aclosed)

![Vue Notus](https://github.com/creativetimofficial/public-assets/blob/master/vue-notus/vue-notus.jpg?raw=true)

## Overview

**Vue Notus** is a free and open-source UI Kit and Admin Dashboard built with **Vue 3**, **Tailwind CSS**, and modern web technologies. Created by [Creative Tim](https://creative-tim.com/), it provides a comprehensive set of components and pages to accelerate your web development process.

This template features a clean, modern design with over 120 UI components, making it perfect for building admin dashboards, landing pages, authentication flows, and presentation websites.

## Key Features

- Built with **Vue 3.0.7** (Composition API support)
- **Tailwind CSS 2.0.4** for utility-first styling
- **120+ UI Components** (Cards, Buttons, Forms, Tables, etc.)
- **Chart.js 2.9.4** integration for data visualization
- **FontAwesome 5.15.3** icons included
- **Vue Router 4.0.5** for client-side routing
- Fully responsive design
- Admin dashboard layouts
- Authentication pages (Login/Register)
- Presentation pages (Landing, Profile)
- MIT Licensed

## Technology Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| Vue.js | 3.0.7 | Frontend framework |
| Vue Router | 4.0.5 | Client-side routing |
| Tailwind CSS | 2.0.4 | Utility-first CSS framework |
| Chart.js | 2.9.4 | Data visualization |
| FontAwesome | 5.15.3 | Icon library |
| Popper.js | 2.9.1 | Tooltip & dropdown positioning |
| Vue CLI | 5.0.0-alpha.7 | Build tooling |

## Project Architecture

### Directory Structure

```
vue-notus/
├── public/                 # Static assets
│   ├── favicon.ico
│   └── index.html
├── src/
│   ├── App.vue            # Root component
│   ├── main.js            # Application entry point
│   ├── assets/            # Images, styles, and static resources
│   │   ├── img/
│   │   └── styles/
│   │       ├── index.css
│   │       └── tailwind.css
│   ├── components/        # Reusable Vue components
│   │   ├── Cards/         # Card components (Stats, Charts, Tables)
│   │   ├── Dropdowns/     # Dropdown menu components
│   │   ├── Footers/       # Footer components
│   │   ├── Headers/       # Header components
│   │   ├── Maps/          # Map integration components
│   │   ├── Navbars/       # Navigation bar components
│   │   └── Sidebar/       # Sidebar navigation
│   ├── layouts/           # Page layout wrappers
│   │   ├── Admin.vue      # Admin dashboard layout
│   │   └── Auth.vue       # Authentication pages layout
│   └── views/             # Page components
│       ├── Index.vue      # Homepage
│       ├── Landing.vue    # Landing page
│       ├── Profile.vue    # Profile page
│       ├── admin/         # Admin dashboard pages
│       │   ├── Dashboard.vue
│       │   ├── Maps.vue
│       │   ├── Settings.vue
│       │   └── Tables.vue
│       └── auth/          # Authentication pages
│           ├── Login.vue
│           └── Register.vue
├── tailwind.config.js     # Tailwind CSS configuration
├── vue.config.js          # Vue CLI configuration
├── babel.config.js        # Babel configuration
└── package.json           # Dependencies and scripts
```

### Component Architecture

Vue Notus follows a modular component architecture:

1. **Layouts**: Provide the overall page structure (Admin, Auth)
   - Admin layout includes: Sidebar, AdminNavbar, HeaderStats, FooterAdmin
   - Auth layout provides a clean interface for login/register pages

2. **Views**: Page-level components that represent routes
   - Compose multiple components to create complete pages
   - Use layout components as wrappers

3. **Components**: Reusable UI elements organized by category
   - Cards: Statistical displays, charts, data tables
   - Dropdowns: Menu systems and action triggers
   - Navbars: Navigation components for different layouts
   - Footers: Page footers with various styles

### Routing Structure

The application uses Vue Router 4 with the following route structure:

```
/                    → Index (Homepage)
/landing             → Landing page
/profile             → Profile page
/admin               → Admin Layout
  ├── /dashboard     → Dashboard with stats and charts
  ├── /settings      → Settings page
  ├── /tables        → Data tables page
  └── /maps          → Maps integration page
/auth                → Auth Layout
  ├── /login         → Login page
  └── /register      → Registration page
```

## Installation and Setup

### Prerequisites

- **Node.js** LTS version (14.x or higher recommended)
- **npm** or **yarn** package manager

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/creativetimofficial/vue-notus.git
   cd vue-notus
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Build Tailwind CSS**
   ```bash
   npm run build:tailwind
   ```

4. **Start development server**
   ```bash
   npm run serve
   ```

5. **Open your browser**
   ```
   Navigate to http://localhost:8080
   ```

### Alternative: One-Command Setup (Linux/Mac)

```bash
npm run install:clean
```

This command will:
- Remove existing `node_modules` and `package-lock.json`
- Install fresh dependencies
- Build Tailwind CSS
- Start the development server

### Production Build

```bash
npm run build
```

This creates an optimized production build in the `dist/` directory.

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm run serve` | Start development server with hot-reload |
| `npm run build` | Build for production with minification |
| `npm run lint` | Lint and fix files using ESLint |
| `npm run build:tailwind` | Compile Tailwind CSS (run after adding new classes) |
| `npm run install:clean` | Clean install and start dev server |

## Development Guidelines

### Working with Tailwind CSS

When you add new Tailwind CSS classes that don't exist in `src/assets/styles/tailwind.css`:

1. Run the Tailwind build command:
   ```bash
   npm run build:tailwind
   ```

2. Restart the development server:
   ```bash
   npm run serve
   ```

### Customizing Tailwind

Edit `tailwind.config.js` to:
- Add custom colors
- Extend spacing utilities
- Configure custom breakpoints
- Add plugins

The current configuration includes custom utilities for:
- Custom heights (95-px, 350-px, 500-px, 600-px)
- Custom widths (100-px to 580-px)
- Custom inset positions
- Custom z-index values

### Adding New Components

1. Create component file in appropriate directory under `src/components/`
2. Follow the existing naming convention (PascalCase)
3. Import and register in parent component or view
4. Use Tailwind CSS classes for styling

### Code Style

The project uses:
- **ESLint** for JavaScript linting
- **Vue 3 Composition API** (optional, can use Options API)
- **Babel** for modern JavaScript transpilation

Run linting:
```bash
npm run lint
```

## Pages and Features

### Presentation Pages

- **Index/Homepage** - Modern landing page with hero section
- **Landing Page** - Full-featured landing page with sections
- **Profile Page** - User profile display

### Admin Dashboard Pages

- **Dashboard** - Statistics cards with Chart.js visualizations
  - Line charts for trends
  - Bar charts for comparisons
  - Page visits table
  - Social traffic statistics

- **Settings** - User settings and configuration forms
- **Tables** - Data table with sorting and actions
- **Maps** - Interactive map integration

### Authentication Pages

- **Login** - User login form with social login options
- **Register** - User registration form

## Component Library

Vue Notus includes 120+ CSS components and 18+ dynamic Vue components:

### Card Components
- `CardStats` - Statistical display cards
- `CardLineChart` - Line chart visualization
- `CardBarChart` - Bar chart visualization
- `CardPageVisits` - Page visits table
- `CardSocialTraffic` - Social media traffic stats
- `CardSettings` - Settings form card
- `CardTable` - Data table with actions
- `CardProfile` - User profile display

### Navigation Components
- `IndexNavbar` - Main site navigation
- `AdminNavbar` - Admin dashboard navigation
- `AuthNavbar` - Authentication pages navigation
- `Sidebar` - Admin sidebar menu

### Dropdown Components
- `IndexDropdown` - Homepage dropdown menu
- `NotificationDropdown` - Notifications menu
- `PagesDropdown` - Pages navigation menu
- `UserDropdown` - User account menu
- `TableDropdown` - Table action menu

### Layout Components
- `HeaderStats` - Statistics header for admin
- `Footer` - Main footer
- `FooterAdmin` - Admin dashboard footer
- `FooterSmall` - Compact footer

## Browser Support

Supports the last two versions of:

| Chrome | Firefox | Edge | Safari | Opera |
|:------:|:-------:|:----:|:------:|:-----:|
| ✅ | ✅ | ✅ | ✅ | ✅ |

## Documentation

Full documentation is available at:
[https://www.creative-tim.com/learning-lab/tailwind/vue/overview/notus](https://www.creative-tim.com/learning-lab/tailwind/vue/overview/notus?ref=vn-readme)

Topics covered:
- Alerts
- Buttons
- Inputs
- Dropdowns
- Navbars
- Tabs
- Modals
- Tooltips
- Popovers
- And more...

## Demo

Live demo: [https://demos.creative-tim.com/vue-notus/](https://demos.creative-tim.com/vue-notus/?ref=vn-readme)

## Other Framework Versions

Vue Notus is available in multiple frameworks:

| Framework | Repository |
|-----------|------------|
| Angular | [notus-angular](https://www.creative-tim.com/product/notus-angular) |
| JavaScript/HTML | [notus-js](https://www.creative-tim.com/product/notus-js) |
| Next.js | [notus-nextjs](https://www.creative-tim.com/product/notus-nextjs) |
| React | [notus-react](https://www.creative-tim.com/product/notus-react) |
| Svelte | [notus-svelte](https://www.creative-tim.com/product/notus-svelte) |
| Vue.js | [vue-notus](https://www.creative-tim.com/product/vue-notus) |

## Reporting Issues

Found a bug? Please report it on [GitHub Issues](https://github.com/creativetimofficial/vue-notus/issues).

When reporting:
1. Check you're using the latest version
2. Provide reproducible steps
3. Specify browser and OS information
4. Include screenshots if applicable

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - Copyright 2021 [Creative Tim](https://www.creative-tim.com/?ref=vn-readme)

See [LICENSE.md](https://github.com/creativetimofficial/vue-notus/blob/main/LICENSE.md) for details.

## Resources

- **Live Demo**: [https://demos.creative-tim.com/vue-notus/](https://demos.creative-tim.com/vue-notus/?ref=vn-readme)
- **Download**: [https://www.creative-tim.com/product/vue-notus](https://www.creative-tim.com/product/vue-notus?ref=vn-github-readme)
- **Documentation**: [https://www.creative-tim.com/learning-lab/tailwind/vue/overview/notus](https://www.creative-tim.com/learning-lab/tailwind/vue/overview/notus?ref=vn-readme)
- **GitHub**: [https://github.com/creativetimofficial/vue-notus](https://github.com/creativetimofficial/vue-notus)
- **Support**: [https://www.creative-tim.com/contact-us](https://www.creative-tim.com/contact-us?ref=vn-readme)

## Useful Links

- [YouTube Tutorials](https://www.youtube.com/channel/UCVyTG4sCw-rOvB9oHkzZD1w)
- [Blog Creative Tim](http://blog.creative-tim.com/?ref=vn-readme)
- [Free Products](https://www.creative-tim.com/templates/free?ref=vn-readme)
- [Premium Products](https://www.creative-tim.com/templates/premium?ref=vn-readme)
- [Tailwind Starter Kit](https://www.creative-tim.com/learning-lab/tailwind-starter-kit/presentation?ref=vn-readme)

## Social Media

- **Twitter**: [@CreativeTim](https://twitter.com/CreativeTim)
- **Facebook**: [Creative Tim](https://www.facebook.com/CreativeTim)
- **Dribbble**: [creativetim](https://dribbble.com/creativetim)
- **Instagram**: [@creativetimofficial](https://www.instagram.com/creativetimofficial/)

---

Made with ❤️ by [Creative Tim](https://www.creative-tim.com)
