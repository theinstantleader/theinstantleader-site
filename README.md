# The Instant Leader website (Cloudflare Pages)

A simple one-page site for **theinstantleader.com**. Hosting is free on Cloudflare Pages. Booking stays on Book Like A Boss.

## What this folder is

These are the files that make up the live homepage. Open `index.html` in a browser to preview locally. The `assets/` folder holds the logos.

## Plain English: GitHub and Cloudflare

Think of this folder as a project drawer.

- **Repository (repo):** the shared drawer on GitHub (or Cursor Origin) that stores these files and every past version.
- **Commit:** a saved snapshot, with a short note such as "update homepage headline".
- **Push:** sending that snapshot up so Cloudflare can see it.
- **Deploy:** Cloudflare Copies the files to the web. Every push can publish a new version automatically. You get a preview URL first; the real domain only changes when you say so.

You do not need to be a developer. I edit the files. You create the free accounts once and approve the DNS change when you are ready.

## Cost

- Cloudflare Pages Free: **$0** hosting
- GitHub (or Cursor Origin) free account: **$0**
- Domain renewal at Names.co.uk: whatever you already pay for `theinstantleader.com`
- Book Like A Boss: unchanged

## DNS stays at Names for now

DNS is still managed at **Names.co.uk**. We have **not** changed any records yet. Kajabi and Framer stay live until you approve a switch.

When you are happy with the preview:

1. Create a free Cloudflare account and a Pages project pointed at this repo (build output = this folder, or `/` if the repo root is this site).
2. Attach `theinstantleader.com` (and optionally `www`) in Pages.
3. At Names, add the CNAME / A / AAAA records Cloudflare shows you for Pages. Do **not** move nameservers unless we decide to later.
4. After HTTPS is green on the new site, cancel Framer, then Kajabi once anything you still need is exported.

The `_redirects` file is ready to send `www` to the apex once both hostnames are attached in Pages.

## Local preview

From this folder:

```bash
python3 -m http.server 8787
```

Then open http://127.0.0.1:8787/

## Booking link

Every "Book a free 20-minute call" button goes to:

https://book.andylee.me/lite/free-20-minute-call

## Still to add before you go fully live

- Portrait photos of Andy (hero and About)
- Podcast episode player embed
- Privacy and Terms pages (footer links exist; pages do not yet)
- Company number / registered address in the footer if you want them public
