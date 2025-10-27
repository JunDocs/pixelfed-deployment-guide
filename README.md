# Pixelfed Deployment Guide


**Open-source, Instagram-style photo sharing:** Deploy a production‑grade Pixelfed instance on Hetzner + Cloudflare, managed with Yunohost.



## Overview


- **Cloudflare** – DNS management, SSL, and proxying to hide server IP  

- **Hetzner** – Linux cloud server  

- **Yunohost** – App platform that installs and manages Pixelfed


## Prerequisites


- Cloudflare account (domain registered and ready for DNS management)  

- Hetzner account (with access to provision a cloud server)  

- A domain you control (to point at the server)  


## High-level steps


1️⃣ Provision a Linux cloud server (Hetzner).  


2️⃣ Register your domain with Cloudflare and set up DNS records to point to your server’s public IP.  


3️⃣ Install Yunohost on the server (see Yunohost docs for the latest install command).  


4️⃣ Use Yunohost’s app catalog to install Pixelfed.  


5️⃣ Enable HTTPS using Yunohost’s built-in Let’s Encrypt certificate management.  

   - Temporarily set Cloudflare’s proxy to “DNS Only” during certificate setup, then switch back to “Proxied” for privacy.


6️⃣ **Privacy & Security Enhancements:**  

   - Disable search engine indexing (edit `robots.txt` to disallow all bots).  

   - Avoid exposing personal/server details in public profiles or pages.  

   - Keep Yunohost and Pixelfed updated.


7️⃣ Configure Pixelfed profiles for Mastodon verification and social integration.


## License


MIT – feel free to reuse or improve.


## Contact

Questions? Reach me at `JunDocs@pm.me`.
