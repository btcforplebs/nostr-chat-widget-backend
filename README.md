# Nostr Chat Widget Backend

This repository provides the minimal hosting layer for the [nostr-chat-widget](https://github.com/btcforplebs/nostr-chat-widget).  
It serves a simple `index.html` file that loads the widget, configures it, and makes it easy to embed on any website.

If you are using **nostr-chat-widget**, this repo acts as your “drop-in host” or example backend.

---

## 🚀 Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/btcforplebs/nostr-chat-widget-backend.git
cd nostr-chat-widget-backend
```

### 2. Open or host `index.html`

You can:
- open it locally in a browser, or  
- deploy it to any static host (Vercel, Netlify, Cloudflare Pages, GitHub Pages, Nginx, etc.)

There is **no backend server** required unless you want to add one.

---

## ⚙️ How It Works

`index.html` loads the Nostr Chat Widget script and initializes it.

A minimal version looks like:

```html
<script src="https://unpkg.com/nostr-chat-widget"></script>

<div id="nostr-chat"></div>

<script>
  NostrChatWidget.mount("#nostr-chat", {
    relays: ["wss://relay.damus.io"],
    channel: "global",
    theme: "light"
  });
</script>
```

You can modify all widget options directly inside `index.html`.

---

## 🧩 Embedding on Your Website

Once deployed, you can embed the widget into ANY site via an iframe:

```html
<iframe
  src="https://yourdomain.com/index.html"
  style="width: 100%; height: 600px; border: 0;"
></iframe>
```

OR by copying the initialization snippet from `index.html` into your site.

---

## 🎛️ Configure Your Widget

Any configuration supported by `nostr-chat-widget` is valid here:

- relay list  
- channel / room  
- pubkey identity  
- themes  
- position in page  
- custom CSS  

Just edit the `<script>` in `index.html`.

---

## 📁 Project Structure

```
nostr-chat-widget-backend/
└── index.html    # Loads and configures the chat widget
```

---

## 📦 Deploying

This project is **static**, so deployment is trivial:

```
# Example: Cloudflare Pages
Drag & drop the folder → done
```

or

```
# Example: Nginx
cp index.html /var/www/your-site/
```

Once `index.html` is online, the widget is live.

---

## 📝 Purpose

This repo exists to give developers a ready-to-use hosting entry point for `nostr-chat-widget`.  
Use it as:

- a standalone hosted chat page  
- an embeddable iframe target  
- a template for integrating the widget into your own app  

---

If you want, I can also provide:

✅ full documented config options  
✅ an iframe-safe index.html version  
✅ a version with dark/light theme switching  
Just tell me what you need.
