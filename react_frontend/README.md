# React Frontend (Simple Todo Application)

This folder contains the React frontend for the simple todo application workspace. At the moment, the implementation is a Create React App-based starter UI that includes a light/dark theme toggle and basic responsive styling.

Although the overall product requirements mention todo CRUD, filtering, and local persistence, those features are not currently implemented in the code under `src/`. This README documents what exists today and how to run it.

## Features implemented

The current frontend includes:

- A **light/dark theme toggle** implemented in `src/App.js` using React Hooks (`useState`, `useEffect`)
- Theme styling via CSS variables in `src/App.css` using the `data-theme="dark"` attribute
- A responsive adjustment for the theme toggle button on smaller screens

## Local persistence

The current code does not persist application state (for example, via `localStorage`). If local persistence is added in the future, it should be described here along with any keys used and migration considerations.

## Getting started

### Install dependencies

From this directory:

```bash
npm install
```

### Start the development server

```bash
npm start
```

By default the app runs on port 3000.

### Run tests

Create React App runs tests in watch mode by default. In CI/non-interactive environments you can use:

```bash
CI=true npm test
```

### Build for production

```bash
npm run build
```

## Configuration (environment variables)

Create React App exposes only environment variables prefixed with `REACT_APP_`. This repository includes a `.env` file with variables that are commonly used when a frontend talks to a backend, but the current frontend code does not reference them.

The `.env` file contains:

- `REACT_APP_API_BASE`: Base URL for API requests.
- `REACT_APP_BACKEND_URL`: Backend base URL (often the same as `REACT_APP_API_BASE`).
- `REACT_APP_FRONTEND_URL`: Public URL for the frontend.
- `REACT_APP_WS_URL`: WebSocket URL (for realtime features).
- `REACT_APP_NODE_ENV`: Environment hint (for example `development`).
- `REACT_APP_NEXT_TELEMETRY_DISABLED`: Present for environments that also run Next.js tooling; not used by Create React App.
- `REACT_APP_ENABLE_SOURCE_MAPS`: Controls source map output if respected by the build environment.
- `REACT_APP_PORT`: Intended port value (the actual dev-server port is typically controlled via `PORT`).
- `REACT_APP_TRUST_PROXY`: Proxy hint, typically relevant to servers rather than a static frontend.
- `REACT_APP_LOG_LEVEL`: Log verbosity hint.
- `REACT_APP_HEALTHCHECK_PATH`: Health check path hint (usually relevant for servers).
- `REACT_APP_FEATURE_FLAGS`: Feature flags as a JSON-like string.
- `REACT_APP_EXPERIMENTS_ENABLED`: Enables/disables experiments.

If you add API calls later, prefer reading a single base URL (for example `REACT_APP_API_BASE`) and build request URLs from it.

## Project structure

- `public/`: Static assets and the HTML template
- `src/index.js`: React entry point that renders `<App />`
- `src/App.js`: Main UI component (currently theme toggle starter)
- `src/App.css`: Theme variables and styling

## Notes for KAVIA preview

In the KAVIA environment, the React frontend container is typically previewed on port 3000.
