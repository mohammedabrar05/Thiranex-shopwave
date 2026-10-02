# 🛍 ShopWave – E-commerce Product Catalog

Web Development Capstone (Thiranex). A modular, fast, production-ready React single-page app.

**Live URL:** _add your Vercel/Netlify link here_

## Features
- Modular architecture: `components/`, `pages/`, `context/`, `data/`
- Client-side routing (React Router): `/`, `/products`, `/products/:id`, `/cart`, 404 page
- Search, category filter and sorting (state kept in the URL, so links are shareable)
- Cart with quantity editing, persisted in localStorage
- Responsive layout + automatic dark mode

## Performance optimizations
- Production build minifies JS/CSS (Vite + esbuild)
- Route-level code splitting with `React.lazy` + separate vendor chunk
- Lazy-loaded images with explicit width/height (no layout shift)
- Generated SVG product images (tiny, zero extra network requests)
- `memo` on product cards, `useMemo` for filtering

## Run locally
```bash
npm install
npm run dev        # http://localhost:5173
npm run build      # outputs /dist
npm run preview
```

## Deploy
**Vercel:** import the GitHub repo, framework Vite, Deploy (`vercel.json` handles SPA routing).
**Netlify:** import repo, build `npm run build`, publish `dist` (`netlify.toml` + `_redirects` included).
