# Client Category Monitor
### WPP Media Taiwan — intelligence dashboard

---

## What this is
A web dashboard that runs live AI-powered intelligence briefs on your 6 clients (LVMH, Google, Richemont, Mazda, Estee Lauder, Jaguar Land Rover). Searches real-time news and returns structured briefs: competitor moves, category trends, brand sentiment, and a sharp angle for your next client meeting.

---

## Deploy in 10 minutes (Railway — free tier)

### Step 1 — Get your Anthropic API key
1. Go to https://console.anthropic.com
2. Click **API Keys** → **Create Key**
3. Copy the key (starts with `sk-ant-...`)

### Step 2 — Deploy to Railway
1. Go to https://railway.app and sign up (free, use GitHub login)
2. Click **New Project** → **Deploy from GitHub repo**
3. Upload this folder as a GitHub repo, OR click **Deploy from local** and drag this folder
4. Once deployed, go to **Variables** tab
5. Add: `ANTHROPIC_API_KEY` = your key from Step 1
6. Railway will restart automatically

### Step 3 — Open your dashboard
Railway gives you a URL like `https://client-monitor-production.up.railway.app`
Bookmark it. That's your dashboard.

---

## Alternative: Run locally (if you have Node.js installed)

```bash
# In terminal, navigate to this folder
cd client-monitor

# Set your API key
export ANTHROPIC_API_KEY=sk-ant-your-key-here

# Start the server
node server/index.js

# Open in browser
open http://localhost:3000
```

---

## How to use
1. Open the dashboard URL
2. Click a client card (LVMH, Google, etc.)
3. Choose signal focus (or leave on "All signals")
4. Hit **Run brief**
5. Read the brief — takes 15-30 seconds as it searches live news

---

## Cost
- Railway free tier: $5/month credit (more than enough for personal use)
- Anthropic API: ~$0.01–0.03 per brief (negligible)

---

## Adding more clients
Edit `public/index.html` — find the `client-grid` div and add a new card following the same pattern.
