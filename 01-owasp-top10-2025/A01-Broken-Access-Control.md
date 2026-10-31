# A01 – Broken Access Control

## Labs (PortSwigger Web Security Academy)

| Lab | Úroveň | Stav | Dátum |
| :--- | :--- | :--- | :--- |
| Unprotected admin functionality | Apprentice | ✅ Solved | 31.10.2026 |
| Unprotected admin functionality with unpredictable URL | Apprentice | ✅ Solved | 31.10.2026 |
| User role controlled by request parameter | Apprentice | ✅ Solved | 31.10.2026 |

## Čo som sa naučil

- **Broken Access Control** znamená, že používateľ môže robiť veci, na ktoré nemá právo.
- **IDOR** (Insecure Direct Object References) je typ, kde sa dá zmeniť parameter v URL a vidieť cudzie dáta.
- **Unprotected admin functionality** – admin stránka je dostupná bez prihlásenia (napr. `/admin`).
- **Unpredictable URL** – aj keď je URL ťažko uhádnuteľná, stále môže byť zraniteľná, ak sa dá nájsť v kóde alebo v histórii.
- **User role controlled by request parameter** – rola používateľa sa dá zmeniť v cookie alebo parametri (napr. `role=admin`).

## Ako to opraviť (best practices)

- **Kontrola prístupu na serveri** – nikdy neveriť klientovi (cookie, parameter).
- **Používať session a role-based access control (RBAC)**.
- **Skryť admin funkcie** – ale nie ako jedinú ochranu.
- **Logovať prístupy** – aby sa dalo odhaliť zneužitie.
