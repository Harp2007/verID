# VerID | Blockchain-Based Tamper-Proof Record Verification

[![Vercel Deployment](https://img.shields.io/badge/Deploy-Vercel%20Ready-black?logo=vercel)](https://vercel.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![REVA University](https://img.shields.io/badge/Demo-REVA%20University-orange)](index.html)
[![Cryptography: SHA-256](https://img.shields.io/badge/Cryptography-SHA--256-teal)](index.html)

**VerID** is a zero-dependency, tamper-proof record and document verification platform powered by a custom blockchain built with native Web Crypto SHA-256.

It demonstrates how universities and organizations can issue credentials where only the **256-bit cryptographic fingerprint** is committed to the blockchain, making unauthorized database or document alterations immediately detectable.

---

## 🚀 Live Demo & Key Capabilities

- **🎓 REVA University Degree Certificate Mode:** Issue student academic credentials (Name, USN, Degree, Year, CGPA), commit the fingerprint to the blockchain, forge records in real time, and observe the **VERIFIED (Green)** vs. **TAMPERED (Red)** watermark stamps.
- **📁 Any Document / File Hash Audit Mode:** Drag and drop any raw file (PDF, DOCX, TXT, images) to calculate its byte-level SHA-256 fingerprint, anchor it on the blockchain, and verify authenticity.
- **🔗 Transparent Blockchain Ledger:** Visual chain showing `Block 0 (Genesis)`, `Block 1`, `Block 2` with timestamp, stored fingerprint, previous hash link, and block hash.
- **⚡ Dual Tamper Simulation:**
  1. *Record Tampering:* Changing a student's CGPA or name creates a hash mismatch (`Hashes differ`).
  2. *Ledger Tampering:* Clicking `Tamper with Block` directly alters historical block data, breaking the cryptographic chain link (`chain broken`).
- **🌙 Dark & Light Mode Support:** Built-in theme switcher with high-contrast accessibility.

---

## 📦 Project Structure

```
verID/
├── index.html       # Self-contained, zero-dependency web application
├── vercel.json      # Optimized Vercel static routing configuration
├── .gitignore       # Standard git exclusions
├── LICENSE          # MIT Open Source License
└── README.md        # Documentation and deployment guide
```

---

## ⚡ How to Deploy to Vercel (Step-by-Step)

This repository is **100% Vercel Ready**. It has zero server-side dependencies and deploys in under 10 seconds.

### Step 1: Push Code to GitHub

Open your terminal in this project folder (`verID`) and run:

```bash
# 1. Initialize git repository
git init

# 2. Stage all files
git add .

# 3. Create your initial commit
git commit -m "feat: complete VerID blockchain record verification platform"

# 4. Set main branch
git branch -M main

# 5. Link your GitHub repository (replace with your repo URL)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# 6. Push to GitHub
git push -u origin main
```

---

### Step 2: Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) and log in (or sign up with GitHub).
2. Click the **"Add New..."** button in the top right and select **"Project"**.
3. Select your newly created GitHub repository (`YOUR_REPO_NAME`).
4. In the configuration screen:
   - **Framework Preset:** `Other` (or leave default).
   - **Root Directory:** `./`
   - **Build Command:** Leave empty.
   - **Output Directory:** Leave empty.
5. Click **"Deploy"**.

That's it! Your website will be live in ~5 seconds at `https://YOUR_PROJECT_NAME.vercel.app`.

---

## 💻 Running Locally

You do not need to install Node.js, Python, or external packages. Simply:

- **Option A:** Double-click `index.html` to open it in any modern browser (Chrome, Edge, Safari, Firefox).
- **Option B (Local Web Server):**
  ```bash
  # Using Python (built-in):
  python -m http.server 3000
  ```
  Then visit `http://localhost:3000`.

---

## 🎓 Judge Demonstration Walkthrough

| Scenario | Action | What to Observe |
| :--- | :--- | :--- |
| **1. Issue Record** | Enter student details and click **"Issue record to Blockchain"**. | A new Block is mined and added to the ledger with a unique SHA-256 fingerprint. |
| **2. Verify Authentic** | Click **"Verify record"**. | Green **VERIFIED** stamp appears; uploaded hash matches the block hash exactly. |
| **3. Tamper Record** | Click **"Tamper with record (Change CGPA)"**, then click **"Verify record"**. | Red **TAMPERED** stamp appears; even a 0.1 change in CGPA completely alters the 256-bit hash. |
| **4. Tamper Ledger** | Click **"⚡ Tamper with Block"** on any block in the ledger. | The status badge turns into a red **chain broken** indicator, proving ledger immutability. |
| **5. File Verification** | Switch to the **"Any Document / File Hash Audit"** tab and drop any PDF/file. | Computes SHA-256 from raw bytes and certifies byte-level integrity. |

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).
