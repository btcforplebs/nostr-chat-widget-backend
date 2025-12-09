# Nostr Chat Widget Backend

A minimal backend/front-end runner for the Nostr Chat Widget. This repository provides a simple HTML host page (`index.html`) that loads and displays the Nostr chat widget so you can embed it anywhere.

## How to Use

### 1. Clone the repo
```bash
git clone https://github.com/btcforplebs/nostr-chat-widget-backend.git
cd nostr-chat-widget-backend
```

### 2. Serve `index.html`
You can host it **anywhere** that can serve static files:

- Nginx  
- Apache  
- GitHub Pages  
- Cloudflare Pages  
- Vercel / Netlify  
- Or simply open `index.html` locally while testing

### 3. Configure your widget
Inside `index.html`, you’ll see script tags for loading the Nostr Chat Widget.  
If the widget has configurable options (relays, pubkey, chat room ID), you can set them in the JS snippet.

Example:
```html
<script>
  new NostrChatWidget({
    relay: "wss://relay.damus.io",
    pubkey: "your_widget_pubkey_here"
  });
</script>
```

(Adjust to whatever configuration your widget requires.)

### 4. Embed into your site (optional)
If you want to put the widget on another webpage, copy the embed snippet from `index.html` into your site.

Example:
```html
<div id="nostr-chat-widget"></div>

<script src="https://your-host.com/nostr-chat-widget.js"></script>
<script>
  NostrChatWidget.mount("#nostr-chat-widget");
</script>
```

### 5. Deploy
Once `index.html` is online, the chat widget is active anywhere that page is loaded.

## Customizing

- Edit the HTML/CSS directly in `index.html`
- Replace relay URLs
- Add branding or custom positioning
- Wrap it in an iframe if you want to embed it cleanly on external websites

## Folder Structure

```
nostr-chat-widget-backend/
└── index.html   # Main host file that loads the chat widget
```

## Purpose

This repo acts as a tiny “backend host” so you can self-host the Nostr chat widget and embed it in your own applications without needing a full server.
