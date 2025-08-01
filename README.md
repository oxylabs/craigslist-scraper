# Craigslist Scraper
[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=craigslist-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.com/invite/Pds3gBmKMH)

[<u>Craigslist
Scraper</u>](https://oxylabs.io/products/scraper-api/web/craigslist) is
a scraping tool that overcomes advanced anti-bot systems and helps you
gather public data from Craigslist on any scale you need. This guide
will show you how to scrape Craigslist using Oxylabs’ [<u>Scraper
API</u>](https://oxylabs.io/products/scraper-api).

## How it works

You can get Craigslist data by sending a request to our API with the
URLs you want to access and scrape. The API will return the HTML of any
public Craigslist page.

### Python code example

The below code sample sends a request to our service, which uses a
headless browser to execute JavaScript and sends back the HTML of a
Craigslist page:

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
   'source': 'universal',
   'url': 'https://berlin.craigslist.org/search/ela#search=1~gallery~0~0',
   'geo_location': 'Germany',
   'render': 'html'
}

# Get a response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('USERNAME', 'PASSWORD'), #Your credentials go here
    json=payload
)

# Instead of response with job status and results URL, this will return the
# JSON response with results.
pprint(response.json())
```

Visit the
[<u>documentation</u>](https://developers.oxylabs.io/scraper-apis/web-scraper-api)
to find more payload parameters and other details.

### Output sample

```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\">\n<head>
      ...
      </script></body>\n</html>\n",
      "created_at": "2023-09-21 14:26:52",
      "updated_at": "2023-09-21 14:27:10",
      "page": 1,
      "url": "https://berlin.craigslist.org/search/ela#search=1~gallery~0~0",
      "job_id": "7110630468831163393",
      "status_code": 200
    }
  ]
}
```

Oxylabs Craigslist Scraper API will ease your scraping processes
significantly. Use it to gather public data, such as jobs, items,
services, and ads. If you have any questions, feel free to get in touch
with us via [<u>live chat</u>](https://oxylabs.io/) or
[<u>email</u>](mailto:support@oxylabs.io).

Also, check this tutorial on [pypi](https://pypi.org/project/craiglist-scraper-api/)
