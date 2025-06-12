# Bless Network Automation Bot

Automates:

* Bless Network account creation
* hCaptcha solving via CapSolver
* Email verification via MailSlurp
* Referral code submission
* Node simulation using Bless Chrome extension

## 🔧 Requirements

* Python 3.9+
* Google Chrome + Chromedriver
* VPS/Server (Contabo tested)

## 📦 Installation

```bash
pip install -r requirements.txt
```

## 🚀 Usage

### Step 1: Register Accounts

```bash
python bless_register.py
```

> Creates an account, verifies email, and saves `b7s_auth_token` to `accounts.json`

### Step 2: Launch Nodes with Extension

1. Download and unzip the Bless Chrome extension
2. Replace `--load-extension=bless_extension/` in `bless_node_launcher.py` with the correct path
3. Add proxies to `proxies.txt`

```bash
python bless_node_launcher.py
```

> Launches Chrome with proxy, adds 5 nodes, and saves output in `accounts_nodes.json`

## 📂 File Structure

```
bless_network_bot/
├── bless_register.py
├── bless_node_launcher.py
├── proxies.txt
├── accounts.json
├── accounts_nodes.json
├── requirements.txt
└── README.md
```

## 🧩 Proxy Format (in `proxies.txt`)

```
ip:port
user:pass@ip:port
```

## 🧪 Output (accounts\_nodes.json)

```json
[
  {
    "Token": "your_b7s_auth_token",
    "Nodes": [
      {"PubKey": "..."},
      {"PubKey": "..."},
      {"PubKey": "..."},
      {"PubKey": "..."},
      {"PubKey": "..."}
    ]
  }
]
```

## 👤 Referral Code Used

```
QQQ5UH
```

---

Made for educational use. Use responsibly.
