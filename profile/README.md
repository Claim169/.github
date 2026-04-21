## 🪪 Claim 169 — Identity Data in QR Codes

**A standard global, interoperable specification for embedding identity data in QR codes using CBOR Web Tokens (CWT).**

---

## 🔍 Overview

**Claim 169** defines a standardized way to represent and encode **identity data of a person** inside a QR code using a compact, secure, and interoperable structure.

It enables:
- **Offline identity verification**
- **Cross-border interoperability**
- **High-assurance authentication without connectivity**

This specification is maintained under the **MOSIP ecosystem** and registered in the **[IANA CWT Registry](https://www.iana.org/assignments/cwt/cwt.xhtml) (Claim Key: 169)**.

Built through a **global, collaborative working group**, Claim 169 continues to evolve with contributions from across the ecosystem.

👉 **[Explore the contributors and start contributing today](https://github.com/Claim169/.github/blob/main/CONTRIBUTORS.md)**!

---

## ❓Why Claim 169?

In many real-world scenarios, especially in remote or low-connectivity environments—online identity verification is not feasible.

Claim 169 solves this by:
- Embedding **identity + photo + biometrics** directly in a QR code  
- Ensuring **data authenticity via digital signatures**  
- Enabling **offline verification without relying on servers**  

> **Example use cases:**
> - Border control & migration  
> - Humanitarian identity systems  
> - National ID cards  
> - Offline service delivery  

---

## 🧠 Core Concepts

### 🧾1. Identity Data as CBOR Map

Claim 169 defines identity data as a **CBOR-encoded map** with structured attributes such as:

- Personal details (name, DOB, gender)  
- Contact info (phone, email, address)  
- Nationality & legal status  
- Photo (embedded binary image)  
- Biometrics (fingerprints, iris, face, etc.)  
- Multi-language support  

All fields are **optional**, allowing flexible implementations.

### 🔐 2. Secure by Design

- Uses **CBOR Web Token (CWT)** for compact encoding  
- Signed using **COSE (e.g., COSE_Sign1)**  
- Supports **encryption for sensitive data (e.g., biometrics)**  
- Public keys discoverable via standard `.well-known` endpoints  

This ensures:
- Integrity (no tampering)  
- Authenticity (trusted issuer)  
- Privacy (optional encryption)  

### ▣ 3. Optimized for QR Codes

Due to QR size constraints, Claim 169:
- Uses **CBOR instead of JSON**  
- Uses **compact cryptography (Ed25519 / ECC)**  
- Supports **compression (zlib)**  
- Encodes final payload in **Base45**  

---

## 🔄 Data Flow

```text
JSON Identity Data
        ↓
Transform to Claim 169 Structure
        ↓
CBOR Encoding
        ↓
CWT Creation (Signed / Encrypted)
        ↓
Compression (zlib)
        ↓
Base45 Encoding
        ↓
QR Code Generation
```

---

## 🧩 Key Features

- ✅ Offline verification (no internet required)  
- ✅ Cross-platform & cross-country interoperability  
- ✅ Multi-language identity support  
- ✅ Extensible attribute model  
- ✅ Supports biometrics (face, fingerprint, iris, voice)  
- ✅ Vendor-specific extensions allowed  

---

## 🛡️ Security Considerations

- All payloads **MUST be signed**  
- **Encryption** is recommended for sensitive fields  
- **Trust** depends on issuer key verification  
- Consumers must **validate**:
  - Signature  
  - Expiry (`exp`)  
  - Issuer (`iss`)  

---

## 🤝 Governance & Contributions

Claim 169 is developed collaboratively by a global working group including:

- MOSIP  
- Inji  
- UNHCR  
- Tech5  
- PwC  
- GIZ  
- OpenSPP  
- Ooru  
- Others

---

## ⭐ Get Involved

Help shape the future of Claim 169 and interoperable digital identity:

- ⭐ Star this repository
- 🛠️ Contribute improvements
- 🌐 Build interoperable identity solutions

**Propose Enhancements:**

- Open an [issue](https://github.com/Claim169/id-claim-169/issues)
- Submit a specification proposal, or
- Join the working group

Head to our [Contributors](https://github.com/Claim169/.github/blob/main/CONTRIBUTORS.md) section to know more!

---

## 📚 Specification

Full specification available here:  
https://docs.mosip.io/1.2.0/readme/standards-and-specifications/mosip-standards/169-qr-code-specification  

---

## 📬 Contact

**Maintainer:**  
Resham Chugani  
📧 resham@mosip.io  

---

## 🪪 About MOSIP

**MOSIP (Modular Open Source Identity Platform)** is an open-source platform that helps governments and organizations implement foundational digital identity systems.

🌐 https://www.mosip.io  

---

> **Claim 169 - Enabling trusted identity — anywhere, anytime, even offline.**
