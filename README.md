<div align="center">

# 🌐 Cloudbit Classic (CDBC) API

[![Website](https://img.shields.io/badge/Official-cdbc.io-success?style=flat-square)](https://cdbc.io/api)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Website](https://img.shields.io/badge/Official-cdbc.io-success?style=flat-square)](https://cdbc-api.vercel.app)

*Robust, scalable, and secure REST API for the Cloudbit Classic ecosystem.*

</div>

---

## 🚀 Introduction

Welcome to the official repository for the **Cloudbit Classic (CDBC) API**. This API is designed to provide developers, exchanges, and community members with a powerful interface to interact seamlessly with the CDBC blockchain. Whether you are building a wallet, integrating a payment gateway, or analyzing blockchain data, the CDBC API offers the reliable endpoints you need.

## ✨ Features

- **⚡ High Performance:** Optimized for low latency and high throughput.
- **🔒 Secure:** Industry-standard security practices and rate limiting.
- **📊 Comprehensive Data:** Access transaction histories, wallet balances, and network statistics.
- **🛠 Easy Integration:** RESTful architecture with standard JSON responses.

## 📖 Table of Contents

- [Getting Started](#-getting-started)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [API Endpoints](#-api-endpoints)
- [Usage Examples](#-usage-examples)
- [Contributing](#-contributing)
- [License](#-license)

## 🏁 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### 📋 Prerequisites

- [Node.js](https://nodejs.org/) (v16.x or higher)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
- A running Cloudbit Classic node (or access to the public RPC)

### 💻 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Cloudbit-Global/cdbc-api.git
   cd cdbc-api
   ```

2. **Install dependencies:**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure environment variables:**
   Create a `.env` file in the root directory and add your configurations:
   ```env
   PORT=3000
   RPC_URL=https://rpc.cdbc.io
   API_KEY_SECRET=your_secret_key_here
   ```

4. **Start the server:**
   ```bash
   npm run start
   # or for development
   npm run dev
   ```

## 📡 API Endpoints

### Base URL
`https://cdbc.io/api`

| Endpoint | Method | Description |
| :--- | :---: | :--- |
| `/api/cdbc/total-supply` | `GET` | Plain text total supply. |
| `/address/{address}` | `GET` | Retrieves the balance and details of a specific wallet address. |
| `/tx/{hash}` | `GET` | Fetches details of a specific transaction by its hash. |
| `/tx/send` | `POST` | Broadcasts a signed transaction to the network. |

*For full API documentation, please visit [cdbc-api.vercel.app](https://cdbc-api.vercel.app).*

## 💡 Usage Examples

### Fetch Address Balance (cURL)

```bash
curl -X GET "https://api.cdbc.io/v1/address/0xYourWalletAddress" \
     -H "Accept: application/json"
```

### Broadcast a Transaction (Node.js/Axios)

```javascript
const axios = require('axios');

async function sendTx(signedTx) {
  try {
    const response = await axios.post('https://api.cdbc.io/v1/tx/send', {
      rawTransaction: signedTx
    });
    console.log('Transaction successful:', response.data.txHash);
  } catch (error) {
    console.error('Error broadcasting transaction:', error);
  }
}
```

## 🤝 Contributing

We welcome contributions from the community! If you'd like to help improve the CDBC API, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

Please make sure to update tests as appropriate.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
<div align="center">
  <sub>Built with ❤️ by the <a href="https://github.com/Cloudbit-Global">Cloudbit Team</a></sub>
</div>
