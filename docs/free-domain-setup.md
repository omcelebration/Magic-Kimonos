# Free Domain Setup — Magic Kimonos

## Status
- GitHub Pages live: `https://omcelebration.github.io/Magic-Kimonos/`
- Redirect page ready: `index.html` points to `https://u5bsgd-02.myshopify.com/`
- Preferred free domain: `magickimonos.de5.net` via DNSHE

## Steps to complete
1. Create DNSHE account at `https://my.dnshe.com/register.php`
2. Search for `magickimonos.de5.net` availability
3. Register the domain
4. In DNSHE dashboard, add DNS records for GitHub Pages:
   - Type: `CNAME`
   - Name: `magickimonos`
   - Value: `omcelebration.github.io`
5. In GitHub repo settings, add custom domain: `magickimonos.de5.net`
6. Wait for DNS propagation and HTTPS to activate
7. Update Shopify Admin > Domains to point `magickimonos.de5.net` to the store, or keep the GitHub Pages redirect as the main marketplace page

## Alternative suffixes
- `magickimonos.us.ci`
- `magickimonos.cc.cd`
- `magickimonos.bot.cd`

## Notes
- No credit card required for DNSHE basic free domains
- Renewal is via dashboard/API, not automatic
- Do not commit any DNSHE API tokens or account credentials
