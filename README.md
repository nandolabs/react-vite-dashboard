# React Vite Dashboard# React + TypeScript + Vite



A modern, responsive dashboard application built with React, TypeScript, Vite, and TailwindCSS v4. Features real-time charts, data visualization, and a clean user interface.This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.



![Dashboard Preview](https://img.shields.io/badge/Status-Production_Ready-brightgreen)Currently, two official plugins are available:

![React](https://img.shields.io/badge/React-19.2.0-blue)

![TypeScript](https://img.shields.io/badge/TypeScript-5.9.3-blue)- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh

![Vite](https://img.shields.io/badge/Vite-7.2.4-646CFF)- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v4-38B2AC)

## React Compiler

## ✨ Features

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

- **Modern Tech Stack**: Built with React 19, TypeScript 5, and Vite 7 for blazing-fast development

- **TailwindCSS v4**: Latest version with new `@import` syntax and improved PostCSS integration## Expanding the ESLint configuration

- **Responsive Design**: Fully responsive layout that works on desktop, tablet, and mobile devices

- **Interactive Charts**: Revenue trends, order analytics, and status distribution using RechartsIf you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

- **Client-Side Routing**: Seamless navigation with React Router 6

- **Component Architecture**: Modular, reusable components following React best practices```js

- **Type Safety**: Full TypeScript coverage across all components and pagesexport default defineConfig([

- **Docker Ready**: Multi-stage Docker build with nginx for production deployment  globalIgnores(['dist']),

- **Clean Code**: ESLint configuration for code quality and consistency  {

    files: ['**/*.{ts,tsx}'],

## 📊 Dashboard Pages    extends: [

      // Other configs...

### Overview

- Key performance metrics (Total Revenue, Orders, Customers, Conversion Rate)      // Remove tseslint.configs.recommended and replace with this

- Revenue trend chart (6-month line chart)      tseslint.configs.recommendedTypeChecked,

- Recent orders table with status indicators      // Alternatively, use this for stricter rules

- Trend indicators showing percentage changes      tseslint.configs.strictTypeChecked,

      // Optionally, add this for stylistic rules

### Orders      tseslint.configs.stylisticTypeChecked,

- Comprehensive orders table

- Order details including customer info, amount, status, and date      // Other configs...

- Status badges (Pending, Completed, Cancelled)    ],

- Mock data with realistic order information    languageOptions: {

      parserOptions: {

### Analytics        project: ['./tsconfig.node.json', './tsconfig.app.json'],

- Monthly order volume bar chart        tsconfigRootDir: import.meta.dirname,

- Order status distribution pie chart      },

- Visual insights into business performance      // other options...

    },

### Settings  },

- User profile management])

- Email and notification preferences```

- Password change functionality

- Notification toggles for various eventsYou can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:



## 🛠️ Tech Stack```js

// eslint.config.js

| Technology | Version | Purpose |import reactX from 'eslint-plugin-react-x'

|------------|---------|---------|import reactDom from 'eslint-plugin-react-dom'

| React | 19.2.0 | UI Framework |

| TypeScript | 5.9.3 | Type Safety |export default defineConfig([

| Vite | 7.2.4 | Build Tool |  globalIgnores(['dist']),

| TailwindCSS | v4.x | Styling |  {

| React Router | 6.x | Routing |    files: ['**/*.{ts,tsx}'],

| Recharts | 2.x | Data Visualization |    extends: [

| Lucide React | Latest | Icons |      // Other configs...

| @tanstack/react-query | Latest | Data Fetching (installed) |      // Enable lint rules for React

| Axios | Latest | HTTP Client (installed) |      reactX.configs['recommended-typescript'],

      // Enable lint rules for React DOM

## 🚀 Getting Started      reactDom.configs.recommended,

    ],

### Prerequisites    languageOptions: {

      parserOptions: {

- **Node.js 20.19+ or 22.12+** (required for Vite 7)        project: ['./tsconfig.node.json', './tsconfig.app.json'],

- npm 10+ or yarn        tsconfigRootDir: import.meta.dirname,

- Docker (optional, for containerized deployment)      },

      // other options...

### Installation    },

  },

1. **Clone the repository**])

```bash```

git clone https://github.com/nandolabs/react-vite-dashboard.git
cd react-vite-dashboard
```

2. **Install dependencies**
```bash
npm install
```

3. **Start development server**
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

### Available Scripts

```bash
npm run dev          # Start development server with hot reload
npm run build        # Build for production
npm run preview      # Preview production build locally
npm run lint         # Run ESLint for code quality checks
```

## 🐳 Docker Deployment

### Build and Run with Docker Compose

```bash
# Build and start the container
docker-compose up --build

# Run in detached mode
docker-compose up -d

# Stop the container
docker-compose down
```

The application will be available at `http://localhost:3000`

### Manual Docker Build

```bash
# Build the image
docker build -t react-vite-dashboard .

# Run the container
docker run -p 3000:80 react-vite-dashboard
```

### Docker Configuration

- **Multi-stage build**: Optimized for production with minimal image size
- **nginx alpine**: Lightweight web server for serving static files
- **SPA routing**: Configured to handle client-side routing
- **Gzip compression**: Enabled for faster asset delivery
- **Cache headers**: 1-year cache for static assets

## 📁 Project Structure

```
react-vite-dashboard/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── Card.tsx         # Base card component
│   │   ├── StatsCard.tsx    # Statistics display card
│   │   ├── Sidebar.tsx      # Navigation sidebar
│   │   ├── Navbar.tsx       # Top navigation bar
│   │   └── Layout.tsx       # Main layout wrapper
│   ├── pages/               # Route pages
│   │   ├── Overview.tsx     # Dashboard home with charts
│   │   ├── Orders.tsx       # Orders management page
│   │   ├── Analytics.tsx    # Analytics and insights
│   │   └── Settings.tsx     # User settings page
│   ├── types/               # TypeScript type definitions
│   │   └── index.ts         # Order, Stats, RevenueData types
│   ├── data/                # Mock data and repositories
│   │   └── mockData.ts      # Sample data for development
│   ├── App.tsx              # Main application component
│   ├── main.tsx             # Application entry point
│   └── index.css            # Global styles and Tailwind import
├── public/                  # Static assets
├── Dockerfile               # Multi-stage Docker build
├── nginx.conf               # nginx configuration for SPA
├── docker-compose.yml       # Docker Compose configuration
├── tailwind.config.js       # TailwindCSS v4 configuration
├── postcss.config.js        # PostCSS with Tailwind plugin
├── tsconfig.json            # TypeScript configuration
└── vite.config.ts           # Vite build configuration
```

## 🎨 TailwindCSS v4 Setup

This project uses TailwindCSS v4, which has breaking changes from v3:

### Key Differences

1. **CSS Import Syntax**
```css
/* v4 syntax (used in this project) */
@import "tailwindcss";

/* v3 syntax (deprecated) */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

2. **PostCSS Plugin**
```javascript
// v4 requires separate package
export default {
  plugins: {
    '@tailwindcss/postcss': {},
    autoprefixer: {},
  },
}
```

### Installation Steps

```bash
# Install TailwindCSS v4 and PostCSS plugin
npm install -D tailwindcss @tailwindcss/postcss autoprefixer

# Configuration files are already set up in this project
```

## 🐛 Troubleshooting

### Node.js Version Error

**Error**: `The Vite distribution for "x64-linux" requires Node.js 20.19.0 or later`

**Solution**: Upgrade to Node.js 22+
```bash
# Using nvm
nvm install 22
nvm use 22

# Or download from nodejs.org
```

### TailwindCSS PostCSS Error

**Error**: `Using 'tailwindcss' directly as a PostCSS plugin...moved to a separate package`

**Solution**: Already fixed in this project
- Installed `@tailwindcss/postcss` package
- Updated `postcss.config.js` to use `'@tailwindcss/postcss'`
- Changed `index.css` to use `@import "tailwindcss"`

### Styles Not Applying

**Issue**: Dashboard displays but without styling

**Causes & Solutions**:
1. Using old Tailwind v3 syntax → Update to `@import "tailwindcss"`
2. PostCSS config incorrect → Use `'@tailwindcss/postcss'` plugin
3. Dev server not restarted → Stop and restart `npm run dev`

## 🔧 Customization

### Adding New Pages

1. Create page component in `src/pages/`
2. Add route in `src/App.tsx`
3. Add navigation link in `src/components/Sidebar.tsx`

### Connecting Real API

Replace mock data in `src/data/mockData.ts` with API calls:

```typescript
// Example using axios and React Query
import { useQuery } from '@tanstack/react-query';
import axios from 'axios';

export const useOrders = () => {
  return useQuery({
    queryKey: ['orders'],
    queryFn: () => axios.get('/api/orders').then(res => res.data)
  });
};
```

### Styling Customization

Edit `tailwind.config.js` to customize colors, fonts, and spacing:

```javascript
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {
      colors: {
        primary: '#your-color',
      },
    },
  },
};
```

## 📝 Development Notes

- **Mock Data**: All data is currently mocked in `src/data/mockData.ts`
- **Type Safety**: All components are fully typed with TypeScript
- **Component Reusability**: Base components like `Card` and `StatsCard` can be reused across pages
- **Responsive Charts**: Recharts components wrapped in `ResponsiveContainer` for mobile support
- **Clean Architecture**: Separation of concerns with components, pages, types, and data layers

## 🚀 Production Deployment

### Build for Production

```bash
npm run build
```

Output will be in the `dist/` directory.

### Deploy Options

1. **Vercel/Netlify**: Connect your GitHub repo for automatic deployments
2. **AWS S3 + CloudFront**: Upload `dist/` folder to S3 bucket
3. **Docker**: Use provided Dockerfile for containerized deployment
4. **nginx/Apache**: Serve `dist/` folder with proper SPA routing

### Environment Variables

Create `.env` file for environment-specific configuration:

```bash
VITE_API_URL=https://api.example.com
VITE_APP_NAME=My Dashboard
```

Access in code:
```typescript
const apiUrl = import.meta.env.VITE_API_URL;
```

## 🤝 Contributing

This is a portfolio project by NandoLabs. Feel free to fork and customize for your own use.

## 📄 License

MIT License - feel free to use this project for learning or commercial purposes.

## 👨‍💻 Author

**NandoLabs**
- GitHub: [@nandolabs](https://github.com/nandolabs)
- Portfolio: Professional React developer specializing in modern web applications

## 🙏 Acknowledgments

- React team for React 19
- Vite team for blazing-fast build tool
- TailwindCSS team for utility-first CSS framework
- Recharts team for simple yet powerful charting library
- Lucide team for beautiful open-source icons

---

Built with ❤️ by NandoLabs
