# AJS TRADING PRO — Render ENOENT fix

## What was fixed
- `server.js` now searches for `public/index.html` in the project root and common nested project paths.
- Static assets and the fallback route use the same resolved frontend directory.
- If `index.html` is missing, the server logs every checked path and returns a readable diagnostic instead of throwing ENOENT.
- No real Upstox access token is included in this ZIP. Set `UPSTOX_ACCESS_TOKEN` privately in Render Environment.

## Deploy this ZIP
1. Extract the ZIP.
2. Upload/commit the CONTENTS of this folder to the root of your GitHub repository (so `server.js`, `package.json`, and `public/` are all at the same level).
3. In Render Settings, set Root Directory blank if the files are at repository root.
4. Build Command: `npm install`
5. Start Command: `npm start`
6. Add `UPSTOX_ACCESS_TOKEN` in Render Environment only if you use live Upstox data. Never commit `.env` or a real token.
7. Commit and push, then Manual Deploy → Deploy latest commit.

If you keep all files inside a subfolder named `AJS_TRADING_PRO`, set Render Root Directory to `AJS_TRADING_PRO` instead.
