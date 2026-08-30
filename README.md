# Aravind Tools (Android)

A native Android equivalent of the **Aravind Tools** personal financial management and zero-knowledge encryption suite, built using **Kotlin**, **Jetpack Compose**, **Material 3**, and zero-knowledge **AES-256-GCM** encryption.

**Current Release**: Version **1.2.0** (Build 3)

---

## 🛡️ Architecture & Security
- **Zero-Knowledge Encryption**: AES-256-GCM authenticated encryption (`javax.crypto.Cipher`) with PBKDF2 key derivation (100,000 rounds, 128-bit salt, 12-byte IV). Full cryptographic interoperability with iOS `.vaultbackup` archives.
- **Biometric Security**: AndroidX `BiometricPrompt` supporting Fingerprint, Face Unlock, and device credential fallback.
- **Local Isolated Persistence**: SQLCipher / Room Database storing encrypted byte arrays (`encryptedPayload`) and isolated `EncryptedVaultFiles/` filesystem storage.
- **Crash Protection & Graceful Fallback**: Comprehensive defensive error boundaries across all data parsers and file viewers.

---

## 📱 Modules & Features (1:1 with iOS)
1. **Transactions & Communications Hub (v1.2.0)**:
   - Unified chronological financial transaction activity stream with bidirectional income/expense classifications.
   - Real-time & batch SMS parsing extracting amounts, counterparties, types, balances, and reference numbers.
   - Smart instrument auto-tagging linking transactions to verified Bank Accounts and Debit/Credit Cards.
   - Lazy loading pagination (10 items per batch) with instant full-text search and date range filters.
   - Comprehensive SMS detail viewer with custom counterparty renaming and global payee synchronization.
2. **Password-Protected PDF Statement Engine (v1.2.0)**:
   - Print-ready theme-invariant PDF statements for Bank and Non-Banking accounts with 30-day activity aggregation.
   - Standard 128-bit PDF encryption with privacy-first password modal dialog.
   - Native OS document preview with system action bar (Save As, Print, Mail, Share).
3. **Banks**: Bank accounts, nicknames, pinned banks, web credentials, mobile & transaction PINs.
4. **Cards**: Credit & Debit cards rendered with Scheme 1 royal blue & emerald green gradients.
5. **Non-Banking Accounts & Ledgers**: Counterparty ledger accounts, 60-day transaction entries, and balance tracking.
6. **Documents & Files Vault (v1.1.0)**:
   - Encrypted document storage for PDFs, images, and text/log files.
   - Nested hierarchical folders with custom color accents.
   - Built-in multi-page PDF reader, photo viewer with auto-orientation, and monospace text viewer.
   - Strict user-defined tags and long-press contextual operations (Rename, Edit, Move, Delete).
7. **Random Password Generator (v1.1.0)**: In-place cryptographically secure password generator with length and character set customization.
8. **Encrypted Backup & Restore**: Automated rolling backups (`*.at-bkp`) with custom directory storage and cross-platform import/export.
9. **Settings & Customization**: Theme (Light/Dark/System), Dynamic Privacy Balance Masking, Auto-Lock timers, Master Passphrase rotation, and Diagnostics Logger.

---

# Aravind Tools App Releases

Official public release repository for the **Aravind Tools** Android application.

## 📥 Latest Release
- **Release Version**: [2026-Aug-30 13-35](./2026-Aug-30 13-35)
- **Direct Download**: [Download aravind-tools.apk (Latest)](./2026-Aug-30 13-35/aravind-tools.apk)
- **Release Notes**: [View Release Notes](./2026-Aug-30 13-35/release-notes.txt)
