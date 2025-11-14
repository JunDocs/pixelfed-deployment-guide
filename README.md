# Pixelfed Deployment Guide

**Open-source, Instagram-style photo sharing:**  
How to deploy a production-grade Pixelfed instance using Hetzner (cloud server), Cloudflare (DNS and SSL), and Yunohost (app management).

## Overview

- **Cloudflare:** DNS management, SSL, and proxying to hide your server’s IP address  
- **Hetzner:** Linux-based cloud server hosting  
- **Yunohost:** Easy app platform for installing and managing Pixelfed

## Prerequisites

- Cloudflare account (with a registered domain for DNS management)  
- Hetzner account (to provision a cloud server)  
- A domain you control (to point to your server)

## High-Level Steps

1️⃣ Provision a Linux cloud server on Hetzner.

2️⃣ Register your domain with Cloudflare and set up DNS records to point to your server’s public IP.

3️⃣ Install Yunohost on your server (see Yunohost docs for the latest install command).

4️⃣ Use Yunohost’s app catalog to install Pixelfed.

5️⃣ Enable HTTPS with Yunohost’s built-in Let’s Encrypt certificate management.
   - Temporarily set Cloudflare’s proxy to “DNS Only” during certificate setup, then switch back to “Proxied” for privacy.

6️⃣ **Privacy & Security Enhancements:**
   - Disable search engine indexing (edit `robots.txt` to disallow all bots).
   - Avoid exposing personal or server details in public profiles or pages.
   - Keep Yunohost and Pixelfed updated.

7️⃣ Configure Pixelfed profiles for Mastodon verification and social integration.

## License

MIT – feel free to reuse or improve.

## Contact

Questions? Reach me at `JunDocs@pm.me`.
