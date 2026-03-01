# Directory Overview

This directory contains a simple static website for the domain `cociekawe.pl`. The site informs visitors that the domain is for sale and that the original store has moved to `biohac.pl`. It is hosted on **Vercel** and handles automatic redirects for old product and category URLs.

# Key Files

*   `index.html`: The main landing page with a "Domain for sale" message and a 10-second countdown timer that redirects to `biohac.pl`. Built with Tailwind CSS.
*   `vercel.json`: The configuration file for Vercel. It contains **301 permanent redirects** with UTM tracking parameters for all old URLs (products, categories, etc.), replacing the previous `.htaccess` logic.
*   `.htaccess`: Legacy Apache configuration file (kept for historical reference, not used by Vercel).

# Deployment & Domain Setup

The project is deployed on **Vercel** using the `master` branch.

### Domain Configuration (Cyberfolks DNS)
To point `cociekawe.pl` to Vercel, the following DNS records are set in the Cyberfolks panel:
*   **A Record (@):** Points to `76.76.21.21` (Vercel IP).
*   **A Record (www):** Also points to `76.76.21.21` (alternatively CNAME `cname.vercel-dns.com` if supported by the panel).

In the Vercel dashboard, `www.cociekawe.pl` is configured to automatically redirect to the root domain `cociekawe.pl`.

# Usage

When a user visits `cociekawe.pl`, they see the landing page and are redirected after 10 seconds. Any access to old product or category paths (e.g., `/produkt/...`) is immediately handled by Vercel's edge network via `vercel.json` and redirected to the corresponding page on `biohac.pl`.
