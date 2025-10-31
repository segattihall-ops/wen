'''
# Bruno Santos - Professional Massage Therapist Website

This repository contains the source code for the professional portfolio website for Bruno Santos, a licensed massage therapist based in Dallas, TX. The website is designed to be clean, professional, mobile-responsive, and SEO-optimized, with a strong focus on creating a safe and welcoming space for the LGBTQ+ community.

## Key Features

-   **LGBTQ+ Friendly Messaging:** Content and design tailored to create a safe and inclusive environment for gay and queer clients.
-   **Mobile-First Responsive Design:** A seamless experience across all devices, from desktops to smartphones.
-   **Live Chat Widget:** A simulated chat feature to engage visitors and encourage booking inquiries.
-   **Multiple CTAs:** Prominent "Book Your Session" and "Call Now" buttons to drive conversions.
-   **Clear Business Information:** Availability (7 AM - 11 PM) and starting price ($150) are clearly displayed.
-   **Professional Credentials:** Highlights Bruno's experience, licensing, and certifications to build trust.
-   **Dynamic Testimonials Section:** Displays 6 reviews initially with a "See More" button to reveal a total of 22 reviews.
-   **SEO Optimized:** Includes schema markup for local business and reviews, and is optimized for relevant keywords like "gay massage Dallas."

## File Structure

```
/bruno-santos-website
|-- /images
|   |-- hero-outdoor.jpg
|   |-- about-studio.jpeg
|   |-- gallery-casual.jpeg
|   |-- gallery-professional.jpg
|-- index.html
|-- privacy.html
|-- terms.html
|-- package.json
|-- README.md
```

## Deployment

This is a static HTML/CSS/JS website and can be deployed to any static hosting provider. Below are instructions for some popular platforms.

### Vercel (Recommended)

Vercel is a great platform for deploying static sites with zero configuration.

1.  **Sign up for Vercel:** Create an account at [vercel.com](https://vercel.com).
2.  **Install Vercel CLI:** Open your terminal and run:
    ```bash
    npm install -g vercel
    ```
3.  **Login to Vercel:** In your terminal, run:
    ```bash
    vercel login
    ```
4.  **Deploy:** Navigate to the `bruno-santos-website` directory in your terminal and run:
    ```bash
    vercel --prod
    ```

Vercel will provide you with a unique URL for your deployed site. To use a custom domain like `www.masseurmatch.com/dallas/massage/brunosantos`, you would typically set this up within the MasseurMatch.com domain's DNS settings to point to the Vercel deployment. This usually involves a reverse proxy or similar setup on the main domain.

### Netlify

Netlify offers a simple drag-and-drop deployment process.

1.  **Sign up for Netlify:** Create an account at [netlify.com](https://netlify.com).
2.  **Drag and Drop:** Zip the `bruno-santos-website` directory and drag the ZIP file into the Netlify dashboard's deployment area.
3.  **Configure:** Netlify will automatically unzip and deploy the site. You can then configure your domain settings.

### GitHub Pages

If you are using Git, you can easily deploy to GitHub Pages.

1.  **Create a GitHub Repository:** Create a new repository on [github.com](https://github.com).
2.  **Push Your Code:** Add the `bruno-santos-website` files to the repository and push them.
    ```bash
    git init
    git add .
    git commit -m "Initial commit"
    git branch -M main
    git remote add origin https://github.com/your-username/your-repo-name.git
    git push -u origin main
    ```
3.  **Enable GitHub Pages:** In your repository's settings, go to the "Pages" section and select the `main` branch as the source. Your site will be deployed at `https://your-username.github.io/your-repo-name/`.

## Local Development

To run the website locally, you can use a simple HTTP server. If you have Python installed, you can run the following command from the `bruno-santos-website` directory:

```bash
# Bruno Santos — Website

This repository contains Bruno Santos' single-page website and a small serverless API for an AI chat assistant.

## Quick overview
- Static site: `index.html`, CSS inlined.
- Serverless API: `api/chat.js` — proxies chat requests to OpenAI. Uses `OPENAI_API_KEY` environment variable.
- Deployment target: Vercel (recommended). `vercel.json` rewrites the site to `/dallas/massage/bruno`.

## Prerequisites
- Node.js 18+ (recommended)
- npm
- Vercel CLI (for local dev or CLI deploy): `npm i -g vercel`

## Local development
1. Install dev dependencies (if you need the static server):

```bash
npm ci
```

2. Recommended: run Vercel's local dev which emulates Serverless Functions and rewrites:

```bash
vercel dev
```

This starts a local server and exposes `/api/*` routes like Vercel will in production.

If you prefer a simple static server for quick previews (no serverless functions), you can run:

```bash
npm start
# or
npx serve .
```

Note: `npm run dev` now runs `vercel dev` (if you have the Vercel CLI installed).

## Environment variables (Vercel)
Set these in your Vercel Project Settings > Environment Variables:
- `OPENAI_API_KEY` — **required**. Never commit this value.
- Optional overrides:
    - `OPENAI_MODEL` (default: `gpt-3.5-turbo`)
    - `OPENAI_MAX_TOKENS` (default: `500`)
    - `OPENAI_TEMPERATURE` (default: `0.6`)

## Deploy to Vercel (from CLI)
If you have Vercel CLI and credentials configured:

```bash
# one-time login
vercel login

# dev (local emulation)
vercel dev

# production deploy
vercel --prod
# or via npm script
npm run deploy:vercel
```

## Hosting at /dallas/massage/bruno
A `vercel.json` is included with rewrites so the site is available at `/dallas/massage/bruno`:
```json
{
    "rewrites": [
        { "source": "/dallas/massage/bruno", "destination": "/index.html" },
        { "source": "/dallas/massage/bruno/:path*", "destination": "/:path*" }
    ]
}
```

## Security: rotating exposed API keys & removing from git
If an OpenAI API key was ever committed, rotate it immediately in the OpenAI dashboard.

To remove a secret from git history consider one of these safe approaches:

1) Using `git filter-repo` (recommended):

```bash
# install (once)
pip install git-filter-repo

# example: remove the string SK-SECRET from the whole history
# create a file "replacements.txt" with lines like: SK-OLD-KEY==>REDACTED
# then run:
git filter-repo --replace-text replacements.txt

# force-push rewritten history to origin (warning: destructive)
git push --force --all
```

2) Using BFG Repo Cleaner (easier):

```bash
# example: remove all text matching the secret
bfg --replace-text replacements.txt
# then follow BFG instructions to clean and force-push
```

If you want me to rewrite history here, I can prepare and run the exact commands — but note this rewrites commits and requires coordination with any collaborators.

## Monitoring & cost controls
- `api/chat.js` includes simple per-IP rate limiting and logs token usage to `chat-usage.log`.
- To reduce cost, lower `OPENAI_MAX_TOKENS`, or use a cheaper model via `OPENAI_MODEL`.

## Need help?
If you'd like, I can:
- Trigger a production deploy now (`vercel --prod`) — I will only run it if you confirm your Vercel credentials are available in this environment.
- Walk through rotating an exposed key and (optionally) rewriting git history to purge it.
- Add a short `README` section showing how to set Vercel environment variables via the Vercel dashboard.


---
Generated: October 31, 2025
