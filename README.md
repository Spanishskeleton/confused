# Confused

A simple static website. The only visible page text is **Confused**. Title, description, social link preview metadata, and preview image also say **Confused**.

## Publish on GitHub Pages (free)

1. On GitHub, create a **public** repository such as `confused-site`.
2. Upload the **contents of this folder** into the repository root (not the zip itself).
3. Go to repository **Settings → Pages**, choose **Deploy from a branch**, `main`, and `/ (root)`, then Save.
4. GitHub will show your default Pages URL. You can view the website there without a custom domain.

## Use `confused.is-a.dev`

This package prepares the canonical link and social image for `https://confused.is-a.dev/`, but it **does not register or verify the domain**. The subdomain must actually be registered to you, and its DNS must point to the Pages site.

- If you own/are approved for that subdomain, create an is-a.dev DNS record that points to your GitHub Pages host (see https://docs.is-a.dev/guides/github-pages/ ).
- In GitHub repository **Settings → Pages → Custom domain**, add `confused.is-a.dev`. Enable HTTPS when available.
- The `index.html` file is already set to use `https://confused.is-a.dev/preview.png` as its social preview image.
- If you use **another** domain, edit the 4 full `https://confused.is-a.dev/` links inside `index.html` first. (The page itself will still work with the wrong links, but the link preview image may not.)

**Important**: is-a.dev currently requires a reasonably complete developer/personal project website, and a one-word page may not satisfy its domain registration rules. A different domain provider may be needed if your existing application is not approved.

## Connect a domain to Discord profile

1. In Discord open **User Settings → Connections → View more → Domain** (globe icon).
2. Enter the domain you own.
3. Discord generates a TXT verification token. Add that token in your domain provider's DNS configuration to the `_discord` record.
4. Verify the connection in Discord after the DNS change has propagated.

For an is-a.dev subdomain, follow their specific TXT-file instructions: https://docs.is-a.dev/guides/discord-verification/ . The TXT string is unique to your Discord account and is **not** included here.

**Note**: Discord's verified profile domain label is controlled by Discord and the domain; website metadata affects link previews when the URL is shared in chat, not the actual verified domain label.

No external resources, scripts, analytics, tracking, or ChatGPT branding are used.
