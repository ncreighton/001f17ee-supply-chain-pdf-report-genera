# Supply Chain PDF Report Generation and Branding API

> Stop wasting hours manually formatting supply chain reports for every partner — our API instantly generates branded, professional PDF reports from your data, so your supply chain documentation looks consistent and credible.

This API eliminates the tedious work of report generation and ensures every PDF report you send to suppliers, logistics partners, or internal teams carries your brand identity. With a single API call, you get a fully formatted, ready-to-share PDF that includes your logo, colors, and custom layout — no design skills needed.

## What's Included

- Generate branded PDF reports with your logo, colors, and custom fonts
- Support for supply chain data formats: inventory, shipments, order status, etc.
- RESTful API with simple JSON input — integrate in minutes
- Batch generation for multiple reports at once
- Secure, scalable cloud infrastructure — no servers to manage

## Who Is This For

- Supply chain managers who need to send weekly inventory reports to multiple vendors
- Logistics companies that want to brand their proof-of-delivery PDFs
- E-commerce businesses generating order fulfillment reports for partners
- ERP integrators looking to add automated report generation to their solutions

## How It Works

Send a POST request with your data and branding parameters (logo URL, colors, text). The API returns a download link to the branded PDF within seconds. No complex setup — just an API key and your favorite HTTP client.

## Frequently Asked Questions

**What data formats can I send?**
You can send JSON arrays of objects. We support common supply chain fields like SKU, quantity, date, status, and more. Custom fields can be mapped.

**Can I use my own logo and colors?**
Yes, you provide a logo URL and hex color codes for primary/secondary colors. Our API applies them consistently.

**How many reports can I generate per month?**
The base plan includes 500 reports per month at $32.49. Additional reports can be purchased in packs.

**Is the API secure?**
Yes, all requests are over HTTPS with API key authentication. We do not store your data after generating the PDF — you get the file instantly.

**Can I customize the layout further?**
Currently we offer preset layouts optimized for supply chain reports. Custom layout templates are available on the enterprise plan.

## What You Get

- Instant digital download
- Complete REST API with full documentation
- Free updates for life — pay once, own forever
- Setup guide and usage instructions

**Get instant access to the API and start generating branded supply chain PDFs today — your first 50 reports are free!**

## Features

- Full REST API

## Quick Start

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Configure environment
cp .env.example .env
# Edit .env with your settings

# 3. Run locally
uvicorn main:app --reload --port 8000

# 4. View interactive docs
open http://localhost:8000/docs
```

## Docker Deployment

```bash
# Build and run
docker compose up -d

# Check health
curl http://localhost:8000/health
```

## Authentication

Get a token first:
```bash
curl -X POST "http://localhost:8000/auth/token?username=admin&password=admin123"
```

Use the token in subsequent requests:
```bash
curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8000/items
```

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/health` | System health |
| POST | `/auth/token` | Get JWT token |
| GET | `/items` | List all items |
| POST | `/items` | Create item |
| GET | `/items/{id}` | Get item |
| PATCH | `/items/{id}` | Update item |
| DELETE | `/items/{id}` | Delete item |
| GET | `/stats` | API statistics |

Full interactive docs: `http://localhost:8000/docs`

## Rate Limits

| Endpoint | Limit |
|----------|-------|
| `/auth/token` | 10/minute |
| `GET /items` | 60/minute |
| `POST /items` | 30/minute |
| `DELETE /items` | 20/minute |

## Running Tests

```bash
pip install pytest httpx
pytest tests/ -v
```

## Production Notes

- Change `SECRET_KEY` in `.env` before deploying
- Replace in-memory `_db` with a real database
- Add proper user management to `auth.py`
- Configure `ALLOWED_ORIGINS` for CORS
- Use Nginx/Traefik as reverse proxy

## License

MIT


---

## Free vs Pro

| Feature | Free | Pro |
|---------|:----:|:---:|
| 100 requests/day | Yes | Yes |
| Standard endpoints | Yes | Yes |
| JSON responses | Yes | Yes |
| Unlimited requests | - | Yes |
| Premium endpoints | - | Yes |
| Batch processing | - | Yes |
| Webhook notifications | - | Yes |
| SLA guarantee | - | Yes |
| Priority support | - | Yes |

### Upgrade to Pro

Get the full version with all premium features, priority support, and lifetime updates.

**[Get Pro Version](https://buy.stripe.com/fZueVdcLl2k46xy47qcZg3g)**

- [Buy Now (Stripe)](https://buy.stripe.com/fZueVdcLl2k46xy47qcZg3g)

