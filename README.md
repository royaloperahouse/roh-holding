# roh-holding

## The holding page to use in a major outage

The `index.html` file in this repo is intended to be used as an emergency holding page, in cases where the whole ROH website is inaccesible.

It's automatically deployed at https://roh-outage.netlify.app from the main branch of this repository.

[![Netlify Status](https://api.netlify.com/api/v1/badges/53b1d50a-9e28-4a07-b5f0-6529a74590d5/deploy-status)](https://app.netlify.com/sites/roh-outage/deploys)

### In case of an outage

1. Reduce TTL for www subdomain as soon as the incident starts, e.g. to 1 minute
2. If clear that issue is likely to continue for longer than x minutes, point the CNAME for www to the Netlify subdomain, https://roh-outage.netlify.app
3. Trigger DNS verification in the Netlify admin UI so they provision a TLS certificate, as documented here: https://docs.netlify.com/domains-https/custom-domains/configure-external-dns/#configure-a-subdomain
