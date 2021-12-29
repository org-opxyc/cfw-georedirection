# Geolocation based redirection
Cloudflare Worker for redirecting to appropriate page based on visitors' country/region.

| Visiting from | Redirect to |
| - | - |
| US | BASE_URL/us/ |
| Middle Wast & Africa | BASE_URL/en-mea/ |
| Indonesia | BASE_URL/id/ |
| Japan | BASE_URL/jp/ |
| all others | do not redirect |

If the worker has redirected once, it wont do it again (which is controlled by setting a cookie `__cf_redirected`).

`BASE_URL` is set in wrangler.toml file.

Reference: https://developers.cloudflare.com/workers/get-started/guide