# P2P Call

Voice, screen share and chat between two browsers, sent directly over WebRTC. No backend.

**Use it:** https://pdcamargo.github.io/p2p-call/

GitHub Pages only serves the page. The call itself goes straight between the two browsers.

## Connect

1. One of you clicks **Start a call** and sends the invite code.
2. The other clicks **Join a call**, pastes it, and sends back the reply code.
3. The first person pastes the reply and clicks **Connect**.

Codes are around 1,500 characters, so they fit in a Discord message. Swap them within a minute or two. The status bar shows whether you're connected over the local network or the internet.

Allow the mic when Chrome asks, even if you plan to stay muted. Chrome only shares your local network addresses with pages that have mic permission.

If it never connects, one of you is probably behind carrier-grade NAT. Both join the same Tailscale network and try again.

## Run locally

Browsers only allow mic and screen capture on secure pages, and `localhost` counts:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000 in Chrome.

## Test alone

Open two tabs and connect them to each other. Wear headphones or mute one side to avoid echo. Share a single window rather than the whole screen so you don't get a hall of mirrors.
