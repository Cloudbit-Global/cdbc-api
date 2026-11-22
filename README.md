<div align="center">
  <a href="https://cdbc-api.vercel.app/api/cdbc/supply">
    <img src="https://raw.githubusercontent.com/Cloudbit-Global/core/main/assets/cdbc-logo-256.png" alt="Cloudbit Classic API Logo" width="135" height="135" />
  </a>
  <h1>Cloudbit Classic Public API (<code>cdbc-api.vercel.app</code>)</h1>
  <p><strong>Real-Time Supply, Circulating Metrics &amp; OpenAPI 3.1 Specification for Market Data Aggregators</strong></p>
  <p>
    <a href="https://cdbc-api.vercel.app/api/cdbc/supply">supply</a> &bull;
    <a href="https://cdbc-api.vercel.app/api/cdbc/total-supply">total-supply</a> &bull;
    <a href="https://cdbc-api.vercel.app/api/cdbc/circulating-supply">circulating-supply</a> &bull;
    <a href="https://cdbc.io">cdbc.io</a> &bull;
    <a href="https://cloudbitex.com">cloudbitex.com</a>
  </p>
</div>

---

## Production Endpoints

| Endpoint URL | Method | Description | Expected Output |
| :--- | :--- | :--- | :--- |
| `https://cdbc-api.vercel.app/api/cdbc/supply` | `GET` | Full tokenomics & primary BSC contract metadata | `200000000` (`CDBC`) |
| `https://cdbc-api.vercel.app/api/cdbc/total-supply` | `GET` | Fixed maximum & total supply endpoint | `200000000` |
| `https://cdbc-api.vercel.app/api/cdbc/circulating-supply` | `GET` | Circulating supply endpoint for CMC & CoinGecko | `200000000` |

### Specifications &amp; Architecture
* **Deployment Infrastructure:** Serverless Edge API hosted on Vercel (`https://cdbc-api.vercel.app`).
* **OpenAPI 3.1 Definition:** [`openapi.yaml`](https://github.com/Cloudbit-Global/cdbc-api/blob/main/openapi.yaml)
* **Primary Contract Reference:** BNB Smart Chain (BEP-20) `0xaf8b1b1bb4a47f537932968C7DE6E251dd50C6a9` (`0% Buy Tax / 0% Sell Tax`).

---

## Official Cloudbit-Global Ecosystem Repositories
* **[`Cloudbit-Global/core`](https://github.com/Cloudbit-Global/core)** – Core architecture, multichain contract registry, verified ABIs, and brand assets.
* **[`Cloudbit-Global/cdbc-dex`](https://github.com/Cloudbit-Global/cdbc-dex)** – Official CloudbitDEX multichain decentralized exchange and listing portal (`cloudbitex.com`).
* **[`Cloudbit-Global/cdbc-app`](https://github.com/Cloudbit-Global/cdbc-app)** – Official main project portal and Android APK (`cdbc.io`).
* **[`Cloudbit-Global/cdbc-api`](https://github.com/Cloudbit-Global/cdbc-api)** – Public supply endpoints and OpenAPI 3.1 specifications (`cdbc-api.vercel.app`).
* **[`Cloudbit-Global/cdbc-bot`](https://github.com/Cloudbit-Global/cdbc-bot)** – Official Telegram GameFi & Tap2Earn Bot (`@cloudbit_ai_bot` / `cloudbit.to`).