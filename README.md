# Muslim Companion Universal Offline Content Packages

Dedicated public content distribution repository for [Muslim Companion](https://github.com/MS-DevX/muslim-companion).

This repository contains verified, offline-first SQLite content packages for canonical Hadith collections, Quran translations, and classical Tafsirs.

## Package Architecture & Integrity

Every package is distributed as an independently verifiable gzipped SQLite database (`.db.gz`).
Before installation into Muslim Companion, the application enforces:
1. **Archive SHA-256 Verification** prior to decompression.
2. **Database SHA-256 Verification** on the uncompressed SQLite database.
3. **SQLite Schema & Pragma Integrity Verification** (`PRAGMA integrity_check`).
4. **Non-blocking Automatic First-Install Delivery** for the 6 canonical Hadith collections.

## Package Catalog Overview (23 Packages)

### 1. Canonical Hadith Collections (Automatic First-Install Download)
- **Sahih al-Bukhari** (`bukhari-ar.db.gz`) — 7,558 Hadiths
- **Sahih Muslim** (`muslim-ar.db.gz`) — 2,921 Hadiths
- **Sunan Abi Dawud** (`abudawud-ar.db.gz`) — 5,274 Hadiths
- **Jami` at-Tirmidhi** (`tirmidhi-ar.db.gz`) — 3,951 Hadiths
- **Sunan an-Nasa'i** (`nasai-ar.db.gz`) — 5,756 Hadiths
- **Sunan Ibn Majah** (`ibnmajah-ar.db.gz`) — 4,335 Hadiths

*Total Transfer Volume:* ~31.0 MB compressed (~160.7 MB extracted database).

### 2. Quran Translations & Tafsir (On-Demand / Optional)
- **Tafsir Ibn Kathir (English)** (`quran-en-ibn-kathir.db.gz`)
- **Tafsir Ibn Kathir (Urdu)** (`quran-ur-ibn-kathir.db.gz`)
- **Tafsir Al-Jalalayn (English)** (`quran-en-jalalayn.db.gz`)
- **Translations:** Urdu, French, Spanish, Italian, Dutch, Portuguese, Russian, Turkish, Persian, Bambara, Koshur, Greek.

## Manifests
- Unified Manifest: [`distribution_manifest.json`](distribution_manifest.json)
- Hadith Manifest: [`assets/data/hadith/manifest.json`](assets/data/hadith/manifest.json)
- Quran Manifest: [`assets/data/quran/quran_package_manifest.json`](assets/data/quran/quran_package_manifest.json)

## License and Attribution
- Hadith texts derived from Open-Hadith-Data (shamela.ws / hadith-islamware concordance) under ODbL 1.0 / DbCL 1.0.
- Quran translations and Tafsir datasets sourced from verified open scholarly repositories.
- Disclaimers: Translations and grading should be verified with qualified Islamic scholars.
