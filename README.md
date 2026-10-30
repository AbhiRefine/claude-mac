# claude-mac

On-demand macOS session (GitHub-hosted runner) for manual app QA, reachable only over a private Tailscale tailnet via VNC. Read `SECURITY-RULES.md` first.

Required repo secrets: `TS_OAUTH_CLIENT_ID`, `TS_OAUTH_SECRET`, `VNC_PASSWORD` (max 8 chars). Optional: `NOVA_STAGING_WEB_URL`, `NOVA_STAGING_API_URL`, `NOVA_DMG_URL`.
