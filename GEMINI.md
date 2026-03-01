# Directory Overview

This directory contains a simple static website for the domain `cociekawe.pl`. The purpose of the site is to inform visitors that the domain is for sale and that the original site has moved to a new domain, `biohac.pl`. It also handles redirecting old URLs to their new locations.

# Key Files

*   `index.html`: This is the main landing page. It displays a message indicating that the domain is for sale and that the site has moved. It features a 10-second countdown timer that automatically redirects users to `biohac.pl`. The page is styled using Tailwind CSS and includes custom JavaScript for the timer functionality.

*   `.htaccess`: This is an Apache server configuration file. It contains a series of `RedirectMatch` and `RewriteRule` directives to permanently redirect (301) specific old product and category URLs from `cociekawe.pl` to their new counterparts on `biohac.pl`. It also appends UTM tracking parameters to the redirect URLs. The file includes basic security settings to deny access to the `.htaccess` file itself, and it configures GZIP compression and browser caching for better performance.

# Usage

The files in this directory are intended to be hosted on a web server configured to handle the `cociekawe.pl` domain. When a user visits the root of the domain, they will see the `index.html` page and be redirected after 10 seconds. If a user tries to access an old URL, the `.htaccess` file will redirect them to the corresponding new page on `biohac.pl`.
