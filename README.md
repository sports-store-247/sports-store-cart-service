# sports-store-cart-service

FastAPI microservice managing shopping carts for the Sports Store platform. Owns the
`cart_db` MongoDB database and calls `catalog-service` (via `CATALOG_URL`) to
validate/enrich cart items with current product data.

## Stack

FastAPI, MongoDB (Motor), pytest.

## Local development

```bash
cp .env.example .env
pip install -r requirements.txt
uvicorn main:app --reload
```

Health check: `GET /health`.

## Branching convention

- `feature/<short-description>` — new functionality
- `bugfix/<short-description>` — non-urgent fixes
- `hotfix/<short-description>` — urgent production fixes

All changes land on `main` via pull request with at least 1 approval (enforced by repository ruleset).
