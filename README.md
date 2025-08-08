# Keylime Remote Attestation PoC (Insyde BIOS + TPM + Secure Boot + IMA)

This repository documents a successful Proof of Concept (PoC) implementation of remote attestation using Keylime on an OEM PC platform with the following characteristics:

- ✅ Rust-based Keylime Agent
- ✅ Python-based Verifier, Registrar, and Tenant
- ✅ TPM 2.0 (STMicroelectronics)
- ✅ Secure Boot enabled (Insyde BIOS)
- ✅ IMA (Integrity Measurement Architecture) enabled
- ✅ Ubuntu 22.04 LTS with Kernel 5.15.0-112-generic
- ✅ Fixed UUID: `11111111-1111-1111-1111-111111111111`
- ✅ TPM NV Index: `0x1500016`

---

## 📂 Included Artifacts

- `keylime.conf`: Agent configuration
- `ima-policy`: Integrity measurement rules
- `tpm_quote.log`, `pcr.log`, `ima_appraisal.log`: Logs from the attestation run
- `deploy.sh`: Deployment script (placeholder)
- `uuid_nv_index.txt`: UUID and NV index for reproducibility

---

## 📊 Architecture Overview

Please refer to the attached PDF:
[PoC_Configuration_Diagram.pdf](PoC_Configuration_Diagram.pdf)

---

## 📈 Business Impact

- OEM-level reproducible Remote Attestation
- NIST SP800-155 / SP800-193 compliant
- Suitable for Zero Trust environments
- Demonstrates BIOS-integrated security

---

## 🔧 How to Reproduce

1. Flash Insyde BIOS with Secure Boot enabled
2. Ensure dTPM 2.0 is provisioned and NV index 0x1500016 is defined
3. Install Ubuntu 22.04 and enable IMA
4. Configure Keylime Agent, Verifier, Registrar, and Tenant using provided files
5. Launch Keylime components and observe successful attestation

---

## 👤 Author

Akihiro Hosoya  
Remote Attestation Security Architect  
LinkedIn: [your LinkedIn]  
Email: [your email]
