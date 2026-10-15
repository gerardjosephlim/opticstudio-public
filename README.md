# OpticStudio CAD (Supabase Multi-User Web Release)

This repository hosts the web distribution for **OpticStudio CAD** with Supabase Multi-User Authentication and AES-256-GCM In-Memory Decryption.

## Security Architecture

- `app.bundle.enc`: AES-256-GCM encrypted binary package.
- `loader.js`: Obfuscated in-memory decryptor with control-flow flattening.
- **Supabase Authentication**: Users sign in with their personal email and password.
- **Row-Level Security (RLS)**: Only authenticated users can retrieve the simulation decryption key.
- Decryption occurs entirely **in-memory** in volatile browser RAM.
- No plaintext optical prescriptions or source code exist in this public repository.

## Running Locally

```bash
python3 -m http.server 8088
open http://localhost:8088/
```
