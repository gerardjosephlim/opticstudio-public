# OpticStudio CAD (Encrypted & Obfuscated Public Web Release)

This repository hosts the web distribution for **OpticStudio CAD** — an interactive 3D/2D optical column CAD and sequential ray-tracing simulator.

## Security Architecture

The core optical algorithms, catalog prescriptions, and ray-tracing engine in this public distribution are **cryptographically protected** using **AES-256-GCM** with **PBKDF2 (100,000 iterations, SHA-256)**:

- `app.bundle.enc`: AES-256-GCM encrypted binary package.
- `loader.js`: Obfuscated in-memory decryptor with control flow flattening and base64 string tables.
- Decryption occurs entirely **in-memory** in the user's browser via the native Web Crypto API upon entering the authorized password.
- No plaintext optical prescriptions or source code exist in this public repository.

## Running Locally

To run this application locally on your computer:

```bash
# 1. Start a local HTTP server in this directory
python3 -m http.server 8088

# 2. Open in your browser
open http://localhost:8088/
```

When the page loads, enter your authorized access password to decrypt the optical engine and launch the CAD simulator.
