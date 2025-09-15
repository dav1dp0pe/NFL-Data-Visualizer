Dockerfile: Container instructions (installs Nodes, copies code, runs npm run dev)

package.json: Lists dependencies (React, Recharts, Tailwind, etc) and scripts

tsconfig.json: TypeScript settings

vite.config.ts: Configuration for Vite (React build tool)

.env: Environment variables exposed to front end

/src:
    App.tsx: Main React component which ties everything together
    index.tsx: Entry point; renders <App /> into DOM
    api/: Functions to call your backend endpoints (players.ts, stats.ts)
    components/: Reusable UI parts (search box, charts)
    styles/: Tailwind/custom CSS