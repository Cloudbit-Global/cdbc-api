<div align="center">
  <a href="https://cdbc.io/api">
    <img src="https://raw.githubusercontent.com/Cloudbit-Global/core/main/assets/cdbc-logo-256.png" alt="Cloudbit Classic API Logo" width="135" height="135" />
  </a>
  <h1>Cloudbit Classic Public API (<code>cdbc.io/api</code>)</h1>
  <p><strong>Real-Time Supply, Circulating Metrics &amp; OpenAPI 3.1 Specification for Market Data Aggregators</strong></p>
  <p>
    <a href="https://cdbc.io/api/supply.json">supply.json</a> &bull;
    <a href="https://cdbc.io/api/total.json">total.json</a> &bull;
    <a href="https://cdbc.io/api/circulating.json">circulating.json</a> &bull;
    <a href="https://cdbc.io">cdbc.io</a> &bull;
    <a href="https://cloudbitex.com">cloudbitex.com</a>
  </p>
</div>

---

## Production Endpoints

| Endpoint | Method | Description | Expected Output |
| :--- | :--- | :--- | :--- |
| `https://cdbc.io/api/supply.json` | `GET` | Full tokenomics & primary BSC contract metadata | `200000000` (`CDBC`) |
| `https://cdbc.io/api/total.json` | `GET` | Fixed maximum & total supply endpoint | `{"total_supply": "200000000"}` |
| `https://cdbc.io/api/circulating.json` | `GET` | Circulating supply endpoint for CMC & CoinGecko | `{"circulating_supply": "200000000"}` |

### Specifications &amp; Hosting
* **OpenAPI 3.1 Definition:** [`openapi.yaml`](https://github.com/Cloudbit-Global/cdbc-api/blob/main/openapi.yaml)
* **IONOS CORS &amp; UTF-8 Config:** [`.htaccess`](https://github.com/Cloudbit-Global/cdbc-api/blob/main/.htaccess) (`Access-Control-Allow-Origin: *`, `application/json; charset=utf-8`)
* **Automated CI Validation:** Every push to `main` is verified by `.github/workflows/validate-api.yml`.

---

## Official Cloudbit-Global Ecosystem Repositories
* **[`Cloudbit-Global/core`](https://github.com/Cloudbit-Global/core)** – Core architecture, multichain contract registry, verified ABIs, and brand assets.
* **[`Cloudbit-Global/cdbc-dex`](https://github.com/Cloudbit-Global/cdbc-dex)** – Official CloudbitDEX multichain decentralized exchange and listing portal (`cloudbitex.com`).
* **[`Cloudbit-Global/cdbc-app`](https://github.com/Cloudbit-Global/cdbc-app)** – Official main project portal and Android APK (`cdbc.io`).
* **[`Cloudbit-Global/cdbc-api`](https://github.com/Cloudbit-Global/cdbc-api)** – Public supply endpoints and OpenAPI 3.1 specifications (`cdbc.io/api`).
* **[`Cloudbit-Global/cdbc-bot`](https://github.com/Cloudbit-Global/cdbc-bot)** – Official Telegram GameFi & Tap2Earn Bot (`@cloudbit_ai_bot` / `cloudbit.to`).