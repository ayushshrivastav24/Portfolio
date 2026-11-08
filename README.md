# Portfolio contact backend

## Run locally

1. Install Node.js 20 or newer.
2. Run `npm install`.
3. Copy `.env.example` to `.env` and set a unique `ADMIN_PASSWORD` and a random `SESSION_SECRET` of at least 32 characters. Generate a secret with `node -e "console.log(require('node:crypto').randomBytes(32).toString('hex'))"`.
4. Run `npm start` and open `http://localhost:3000`.
5. View messages at `http://localhost:3000/admin.html`.

Submissions are stored in `data/submissions.sqlite`. Back up this file to preserve messages. It is intentionally excluded from static file serving and version control.

## Deployment

Deploy to a Node.js host that supports Node 20 or newer. Configure `ADMIN_PASSWORD`, `SESSION_SECRET`, and `NODE_ENV=production` in the host's environment settings, and use HTTPS. Attach persistent disk storage for `data/` or set `DATABASE_PATH` to a file on that disk; ephemeral deployments can lose submissions when redeployed. The site must be opened through the Node server, not directly as a `file://` page.# Portfolio
