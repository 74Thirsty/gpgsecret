# 🔒 GPG Secret Manager CLI

A lightweight, interactive Python CLI for securely managing secrets using GPG encryption. Secrets are stored in a structured `service/secret.gpg` format and can be added, listed, removed, and decrypted — all from a simple terminal interface.

---

## 📦 Features

- 🔐 Encrypt secrets using your GPG key
- 📁 Store secrets as `secrets/service/secret.gpg`
- 🧾 List all stored secrets
- 🗑️ Remove secrets
- 🔓 Decrypt and view secret values
- 🧠 No external dependencies or keyring libraries
- 🖥️ Fully interactive — no command-line flags required

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/gpg-secret-manager.git
cd gpg-secret-manager
```

### 2. Set your GPG identity
Edit the script and set your GPG key name or ID:
```python
GPG_ID = "your-key-name"
```

### 3. Run the CLI
```bash
python3 gpg_secrets.py
```

---

## 🧪 Example Usage

```
🔒 GPG Secret Manager
1️⃣ Add secret
2️⃣ Remove secret
3️⃣ List secrets
4️⃣ Decrypt secret
5️⃣ Exit
Choose an option:
```

### Add a secret
- Service name: `servicename`
- Secret name: `keyname`
- Secret value: `secret`

Stored as:
```
secrets/aes/AAVE_SUBGRAPH.gpg
```

### Decrypt a secret
- Service name: `servicename`
- Secret name: `keynae`

Output:
```
🔓 Decrypted value:
secret
```

---

## 🔧 Requirements

- Python 3.6+
- GPG installed and configured
- A valid GPG key (run `gpg --list-keys` to confirm)

---

## 🛠️ Notes

- The script uses `subprocess` to call GPG directly — no `keyring`, no desktop dependencies.
- If your GPG key requires a passphrase, make sure loopback mode is enabled:
  ```bash
  echo "allow-loopback-pinentry" >> ~/.gnupg/gpg-agent.conf
  gpgconf --kill gpg-agent
  gpgconf --launch gpg-agent
  ```

---

## 📄 License

MIT — do whatever you want, just don’t blame me if you lose your secrets.

---

Let me know if you want a logo, badges, or GitHub Actions wired in. I can also help you publish it as a pip-installable package.
