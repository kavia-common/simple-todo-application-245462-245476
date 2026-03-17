# Simple Todo Application (React Frontend)

This repository contains a simple todo application implemented as a single React frontend container. The frontend is responsible for rendering the UI and managing todo state locally in the browser.

## What is included

The project currently includes:

- A React app in `react_frontend/`
- A light/dark theme toggle implemented in the UI
- Standard Create React App scripts for development, testing, and production builds

Although the broader work item mentions todo CRUD, filtering (all/active/completed), and local persistence, the current code in this repository is a React starter UI and does not yet implement todo functionality.

## Architecture (monolithic)

This repo is effectively monolithic for deployment because it runs as a single container:

- **react_frontend**: The only running component. It serves the web UI on port 3000.

There is no backend or database container in this repository.

## Getting started

### Prerequisites

- Node.js (LTS recommended)
- npm

### Run the frontend

```bash
cd react_frontend
npm install
npm start
```

Then open:

- http://localhost:3000

## Container documentation

For more detailed information about scripts and environment variables, see:

- `react_frontend/README.md`
