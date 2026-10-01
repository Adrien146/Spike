# SPIKE v2.8.1 deployment fix

This release keeps the existing Vite + Node architecture but makes the Node server more robust when hosted:
- resolves the Vite `dist` directory relative to the server module instead of the process working directory;
- serves the built frontend at `/`;
- adds SPA fallback to `index.html` for client-side routes;
- returns a clear error if the frontend build is missing.

Hostingsurge: keep the Vite framework preset and default `npm run build`. The server is started by the detected Node runtime/start configuration.
