# Geolocation based redirection
Cloudflare Worker for redirecting to appropriate page based on visitors' country/region.

| Visiting from | Redirect to |
| - | - |
| US | BASE_URL/us/ |
| Middle Wast & Africa | BASE_URL/en-mea/ |
| Indonesia | BASE_URL/id/ |
| Japan | BASE_URL/jp/ |
| all others | do not redirect |

If a redirection is required, the worker will set a cookie `_redirect_to` with value equal to the url to which redirection is to be done.

Reference: https://developers.cloudflare.com/workers/get-started/guide
