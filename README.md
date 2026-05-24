# sys-design

Hands-on system design practice. Each problem is a self-contained Jupyter notebook — schema, API, and test calls all in one place, no server required.

## Problems

| Notebook | Problem | Time-box |
|---|---|---|
| `twitter.ipynb` | Microblog (Twitter / X) | 45–60 min |
| `url_shortener.ipynb` | URL shortener (bit.ly) | 30–45 min |
| `uber.ipynb` | Ride-hailing (Uber / Lyft) | 45–60 min |

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

## How it works

- **Schema** — write your `CREATE TABLE` statements inline and re-run the cell to get a fresh in-memory SQLite database.
- **API** — define FastAPI endpoints that write directly to `conn`. No server spins up; calls go through `TestClient`.
- **Demo** — call endpoints with `call("post", "/users", json={...})` and inspect results with `df("table")` or `show_all()`.
