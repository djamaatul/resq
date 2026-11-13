# Next.js + Postgres/PostGIS, deployed with Docker Compose on a VPS

ResQ is a full-stack TypeScript Next.js app backed by Postgres with PostGIS, run as Docker Compose containers on a single VPS. PostGIS gives us correct, indexed "Members within the Notification Radius" queries, and a long-running server (not serverless) lets us hold real-time connections for Request Chat and live status updates alongside Web Push.

## Considered Options

- **Laravel + MySQL**: familiar, but MySQL spatial support is weaker for radius queries.
- **Firebase**: auth/push out of the box, but geo queries need geohash workarounds and the data model locks us into Firestore.
- **Vercel + managed Postgres**: serverless functions can't hold real-time connections, so a separate real-time service would be needed.
