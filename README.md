# Overstock Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Overstock Scraper](https://oxylabs.io/products/scraper-api/ecommerce/overstock?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Overstock website effortlessly. This brief guide showcases how Overstock Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Overstock results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Overstock page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://ooutlet.com/collections/dining-room'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/overstock-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html>\n<html lang=\"en\">\n<head>\n  <meta name=\"facebook-domain-verification\" content=\"yax5zvb ... </html>",
      "created_at": "2024-02-20 12:39:52",
      "updated_at": "2024-02-20 12:39:53",
      "page": 1,
      "url": "https://ooutlet.com/collections/dining-room",
      "job_id": "7165686494198254593",
      "status_code": 200
    }
  ]
}
```
With our Overstock Scraper, you can seamlessly extract public data from any Overstock web page. Gather essential product information such as color options, shipping details, or stock availability in order to craft the most effective marketing strategy and get a competitive edge. For any inquiries, our support team is available through live chat or you can email us at hello@oxylabs.io.