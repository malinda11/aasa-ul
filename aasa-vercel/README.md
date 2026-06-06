# AASA on Vercel (Free)

This folder is a minimal deploy package for hosting Apple App Site Association (AASA) on Vercel.

## 1) Edit appID

Open `.well-known/apple-app-site-association` and replace:

- `YOURTEAMID` with your Apple Team ID (10 chars)
- `com.example.app` with your iOS Bundle ID

Final appID format:

YOURTEAMID.com.example.app

## 2) Push this folder to GitHub

You can keep it in this repo or copy into a dedicated repo.

## 3) Import to Vercel and deploy

- Vercel dashboard -> Add New -> Project
- Select the GitHub repo
- Root Directory: set to `aasa-vercel` if this is a monorepo
- Deploy

## 4) Verify links

Replace YOUR_DOMAIN with your Vercel domain:

- https://YOUR_DOMAIN/.well-known/apple-app-site-association
- https://YOUR_DOMAIN/apple-app-site-association

Expected:

- HTTP 200
- No redirect
- JSON body

## 5) Fill WeChat Universal Links

Use:

https://YOUR_DOMAIN/

Or a business path prefix:

https://YOUR_DOMAIN/wx/

Ensure your app actually handles the same prefix.
