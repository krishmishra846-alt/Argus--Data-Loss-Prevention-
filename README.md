# 🛡️ Argus DLP: Zero-Trust Document Integrity & AI Redaction Engine

**Argus DLP** is an enterprise-grade document security and Data Loss Prevention (DLP) platform. It seamlessly integrates **Web3 Cryptography**, **Optical Character Recognition (OCR)**, and **Large Language Models (LLMs)** to create a zero-trust environment for handling highly sensitive documents. 

This repository serves as a public showcase of the Argus DLP architecture and its real-time forgery detection capabilities.

---

## 🎥 The Forgery Detection Demo (Video Walkthrough)

*(Drop your video file here so it embeds directly into the README)*

In the demo video above, we showcase a real-world scenario of **Absolute Cryptographic Integrity**. Human eyes and standard file size checks cannot detect micro-tampering, but Argus DLP catches it instantly.

### 🧪 The Setup
We use two visually identical PDF files:
* 📄 **`Argus DLP.pdf` (Authentic File)** - Size: 66 KB
* 📄 **`Argus DLP (1).pdf` (Forged File)** - Size: 66 KB *(A malicious actor has secretly altered a single digit in a credit card number).*

### 🔄 Step-by-Step Breakdown of the Demo

**1. Secure Web3 Authentication**
* The System Admin connects their MetaMask wallet to establish a cryptographic identity. The system operates on a zero-trust model—without a secure Web3 connection, access to the vault is denied.

**2. Establishing the Master Hash (Source of Truth)**
* The Admin uploads the authentic `Argus DLP.pdf`.
* Under the hood, the Argus Engine generates a highly secure **SHA-256 cryptographic hash** of the file's exact binary composition.
* This Master Hash is stored in our localized ledger, and the document is tagged as `WAITING FOR STUDENT APPROVAL`.

**3. The Forgery Attempt & Detection**
* A user attempts to verify the tampered document: `Argus DLP (1).pdf`.
* Although the file size remains exactly 66 KB and the visual layout is identical, the single modified digit completely alters the file's underlying binary structure.
* The system recalculates the hash and compares it against the Master Hash in the ledger. 
* **Result:** The system instantly catches the discrepancy and throws a strict **`REJECTED (HASH MISMATCH)`** alert, blocking the file from entering the secure vault.

**4. Successful Verification & AI Redaction Sweep**
* The user then uploads the authentic `Argus DLP.pdf`. The hashes match perfectly.
* **Result:** The document is **`VERIFIED`**.
* The file is instantly pushed through our **AI Extraction Layer** (EasyOCR + LLaMA-3.3-70b). The AI intelligently reads the text, extracts basic non-sensitive demographics (Name, DOB), and ruthlessly hunts down PII.
* Passwords, Aadhaar numbers, PAN cards, phone numbers, and emails are entirely stripped and replaced with secure tags like `[REDACTED_SENSITIVE]` and `[REDACTED_PAN]`.

**5. Smart Vault Routing & Audit Report**
* Based on the context and filename, the AI categorizes and routes the verified file to a heavily encrypted physical directory (e.g., *Medical Records Vault*).
* Finally, it generates a downloadable **Security Audit PDF**, giving the admin a 100% transparent view of the Risk Score, the verification status, and the completely sanitized text.

---

## 💻 Technical Architecture
* **Frontend:** Next.js, Tailwind CSS, Lucide Icons, MetaMask (`window.ethereum`)
* **Backend:** Python, FastAPI, EasyOCR, PyPDF
* **AI & Intelligence:** Groq API routing LLaMA-3.3-70b-versatile
* **Security Layer:** SHA-256 Cryptographic Hashing, Localized JSON Ledgers, Regex-based PII Pattern Matching

---

## 📩 Want the Source Code? Let's Connect!

This repository contains the architecture breakdown and demonstrations. The core proprietary backend, AI prompts, and frontend integration code are kept in a separate, private repository.

If you are a recruiter, or just want to discuss Web3 & AI systems, feel free to reach out to me!

* 💼 **LinkedIn:** [Krish Mishra](https://www.linkedin.com/in/krish-mishra-b37732399)
* ✖️ **X (Twitter):** [@KrishM2898AD](https://x.com/KrishM2898AD)
* 📸 **Instagram:** [@_krish1250](https://www.instagram.com/_krish1250)

*(Drop a message mentioning Argus DLP!)*
