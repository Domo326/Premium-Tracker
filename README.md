# 🎁 Premium Tracker

> A mobile-first giveaway inventory tracker for tour managers. Track what you start with, what came in, what's left — and let the app do the math. 📦✨

🌐 **Live app:** [premium-tracker.vercel.app](https://premium-tracker.vercel.app)

---

## 🤔 What's the point?

You're a tour manager. You hit a city. You set up. You give free stuff away to people who walk by. At the end of the day someone needs a report telling them **exactly how many items you handed out** — and you've been too busy refilling bins and answering questions to keep count.

This is your calculator. ✨

You tell it:
- 📦 What you started the day with
- 🔄 What restocks came in (and when)
- 🛏️ What's left at the end

…and it tells you exactly what was given out. No napkin math at 11pm in a hotel room.

---

## 🚀 Features

- 📁 **Event folders** — organize tour stops with optional city + month/year
- 📅 **Day-by-day inventory** — restocks logged with timestamps
- 🧮 **Auto-calculated totals** — given-out math handled for you
- 🔒 **Close-out lock** — finalize a day so numbers don't drift (reopen anytime)
- 🏆 **End-of-tour summary** — beautiful shareable card with charts, fun facts, and PNG export
- 🎨 **3 themes** — Light, Dark, and 🌊 Ocean gradient
- 📤 **Export** — copy a day as text or download CSV
- 💾 **100% local** — no accounts, no servers, no tracking, no cookies
- 📱 **Mobile-first** — designed for one-handed use during a busy event

---

## 🎯 How to use it

### 👋 First time

Open the app. You'll see a welcome modal explaining the basics. Read it, check "Don't show again" if you want, tap "Got it" — you're in.

Tap the **ⓘ** icon (top-right of any screen) anytime to see those tips again.

---

### 1️⃣ Create an event 📁

On the home screen, tap **➕ New Event**.

You'll be asked for:
- **Event Name** (required) — e.g. "LA County Fair"
- **City** (optional) — e.g. "Los Angeles, CA"
- **Month/Year** (optional) — pick a month from the picker; displays as `Sep/25` next to the event name

Think of an event as a folder. Every day of that event lives inside it.

---

### 2️⃣ Add a day 📅

Tap into your event, then tap **➕ New Day**.

The app auto-assigns Week 1 · Day 1 (you can tap the header to edit it). Today's date fills in by default. If you're on Day 3 of an event, it'll auto-bump to Week 1 · Day 3.

---

### 3️⃣ Set starting inventory 📦

Tap any item card (👕 T-Shirts, 🛍️ Bags, etc.) to expand it. You'll see:

```
Starting:  [   ]
Leftover:  [   ]
```

Type in how many you started the day with. That's it.

---

### 4️⃣ Log restocks throughout the day 🔄

Got a midday delivery? Tap the item, scroll to the "+ stock amount" field, type the amount, tap **+ Stock**.

You'll get a 🕒 timestamped log of every restock, so you know exactly when those extra 50 bags showed up.

---

### 5️⃣ The Math ✨

Here's the equation under the hood:

```
Total Start  =  Starting  +  All Restocks
Given Out    =  Total Start  −  Leftover
```

**Real example:**

| 🏷️ Event | Amount |
|---|---|
| 📦 Starting T-Shirts | **50** |
| 🔄 Restock at 1:15 PM | +30 |
| 🔄 Restock at 4:00 PM | +20 |
| 🛏️ Leftover at end of day | **12** |

→ Total Start = 50 + 30 + 20 = **100**
→ Given Out = 100 − 12 = **88** ✅

The big amber number on each item card is **Given Out**, updated live as you type. No calculator needed. 🧮

---

### 6️⃣ Close out the day 🔒

Done? Tap **Close Out Day** at the bottom. The day locks so you don't bump numbers by accident.

Need to fix something later? Tap **Reopen Day** — it's not permanent.

---

### 7️⃣ Manage your items library 📚

Tap the **⚙️ gear icon** on the home screen to open Settings → Items Library.

This is your master list of items. When you start a new day, the app pulls from here.

- ➕ **Type a name → tap Add** — the app auto-picks an emoji based on the name (stickers → 🏷️, hats → 🎩, lanyards → 🪢, etc.)
- ✏️ **Pencil** — edit the name and emoji manually (with suggestions)
- 🗑️ **Trash** — remove from library

Default starter items are 👕 T-Shirts and 🛍️ Bags. Customize freely.

---

### 8️⃣ Export a single day 📤

Inside any day, tap the **📄 file icon** (top right) to export:

- 📋 **Copy as Text** — clean recap to your clipboard, paste anywhere
- 💾 **Download CSV** — for Excel / Google Sheets fans

---

### 9️⃣ End your tour 🏆

When the tour wraps, go to **⚙️ Settings** and scroll down to **🏆 End Tour**.

You'll get a gorgeous summary card showing:

- 🎯 Total items given out across the whole tour
- 📅 Days worked
- 📁 Events visited
- 📍 Cities (if you added them)
- 📊 Bar chart of every item, ranked
- 🎲 A random fun fact about your numbers
- 🎉 A congratulatory message

Then:
- 📸 **Save as PNG** — for Instagram, Slack, group texts, end-of-tour bragging rights
- 📋 **Copy Text** — same info, plain text
- 🧹 **Start New Tour** — wipes everything for a fresh start. ⚠️ Save your PNG first!

---

## 🎨 Themes

Tap the theme icon (top right). It cycles through:

🌞 **Light** → 🌙 **Dark** → 🌊 **Ocean** → 🌞 back to Light

The icon shows the **next** theme you're switching to — so in light mode you see 🌙 (tap for dark), in dark you see 🌊 (tap for ocean), and in ocean you see ☀️ (tap for light).

The Ocean theme is a deep teal gradient with cyan accents. Easy on the eyes, looks 🤌 on the End Tour summary.

---

## 🔐 Privacy

Everything lives in **your browser's localStorage**. There's:

- ❌ No signup
- ❌ No backend  
- ❌ No analytics
- ❌ No tracking
- ❌ No cookies (besides what the browser sets itself)

⚠️ **Heads up:** If you clear your browser data, you'll lose your tour history. So if a tour was important, **save the summary PNG** before doing any cleanup.

---

## 🛠️ Tech stack

- Single `index.html` file — no build step
- React 18 via CDN
- Babel Standalone (in-browser JSX)
- Tailwind CSS via CDN
- html2canvas for PNG export
- localStorage for persistence

Open `index.html` in a browser and it works. That's it.

---

## 🚀 Deploy your own copy

1. Fork or clone this repo
2. Connect to [Vercel](https://vercel.com), [Netlify](https://netlify.com), or enable GitHub Pages
3. Auto-deploys on every commit 🎉

**Run locally:**

```bash
# No build step. Just open it.
open index.html
```

Or use VS Code's **Live Server** extension if you want hot reload while you tweak.

---

## ☕ Support

Built by a tour manager, for tour managers. If this saved you from a notebook breakdown at 11 PM in a Holiday Inn:

[**Buy me a coffee →**](https://buymeacoffee.com/Domo326) ☕

---

## 📝 License

MIT. Fork it, customize it, brand it for your own tours. 🙌

---

🎁 Happy tracking, road warriors. 🚌💨
