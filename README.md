# Writing helper

Paste text, pick (or type) what you want done, get the result. Uses the Gemini API through a tiny server so your key is never exposed in the browser.

## Run it
1. Install Node 18 or newer (https://nodejs.org).
2. Copy `.env.example` to `.env` and paste your Gemini key (free at https://aistudio.google.com/apikey).
3. In this folder run: `node server.js`
4. Open http://localhost:3000

## Put it online
Any host that runs Node works (Render, Railway, Fly.io). Set `GEMINI_API_KEY` as an environment variable there instead of using a `.env` file. Start command: `node server.js`.

## Important
- Never put your API key in `index.html`. Anyone could view it and use up your quota.
- Free Gemini keys have rate limits, and Google may use free-tier data to improve its products. Don't send private text if that matters to you.
- To change the model, set `GEMINI_MODEL` in `.env`.
