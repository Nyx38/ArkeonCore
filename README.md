# ⚡ Arkeon Core

> Solo-built protocol-level Bitcoin validation engine & interactive 3D mempool visualizer.

An independent, high-performance consensus verification environment designed for deep chain analysis, custom script validation, and real-time transaction tracking.

---

## 🚀 Overview

Arkeon Core is a custom-engineered Bitcoin validation infrastructure built from the ground up. It bypasses standard wrapper constraints to interface directly with protocol-level consensus mechanics, transaction pipelines, and cryptographic validation paths.

### Key Features
* **Full Consensus Verification:** Embedded Script VM with support for Legacy (P2PKH), Native SegWit (P2WPKH), and Taproot (P2TR) pipelines.
* **Advanced Cryptography:** Native Schnorr Signatures / BIP340 execution and verification.
* **Risk & Policy Engines:** Built-in Anomaly Detection Engine and historical memory counter profiling.
* **3D Mempool Visualizer:** High-fidelity graphical interface mapping live network transactions and validation states.

---

## 🎥 3D Mempool Dashboard Demo

*Below is the real-time simulation of the protocol validation engine running on the local network visualizer:*

![Arkeon Core 3D Mempool Visualizer](https://www.youtube.com/watch?v=95U-C3geV6o)

---

## 🖥️ Test Console & Consensus Validation Logs

Arkeon Core includes an independent consensus verification environment (`tests/run_all.py`). Below are the stable execution profiles showing complete test vector compliance:

### 1. Router Routing Test (`tests.test_router`)
```bash
> python -m tests.test_router
[ COMMAND ] python -m tests.test_router
[ RUNNING ] UniversalValidator router test
[ P2PKH ] API test vector loaded
[ CHECK ] ScriptPubKey classification: Legacy P2PKH
[ CHECK ] Script execution: OP_DUP / OP_HASH160 / OP_EQUALVERIFY / OP_CHECKSIG
[ PASS ] P2PKH routed through UniversalValidator
[ PASS ] Risk Engine: LOW
[ PASS ] Policy Engine: ALLOW
[ PASS ] Anomaly Engine: NORMAL
[ PASS ] Historical Intelligence: Profile indexed

[ P2WPKH ] API test vector loaded
[ CHECK ] ScriptPubKey classification: Native SegWit P2WPKH
[ CHECK ] Witness context detected
[ PASS ] P2WPKH routed through UniversalValidator
[ PASS ] SegWit execution pipeline
[ PASS ] Historical Memory: Occurrence counter updated
[ ROUTER TEST PASSED ]

---

## 📸 Core Execution & Test Gallery

Below are the live execution proofs, cryptographic verification checkpoints, and system architecture layers of the validation engine:

![Test 153454](https://github.com/user-attachments/assets/9894a1ca-1caf-4fe5-986d-ec45dccd95eb)

---

![Test 153437](https://github.com/user-attachments/assets/414adbf1-81d4-42b4-96e6-106eb561f577)

---

![Test 153416](https://github.com/user-attachments/assets/6c972026-f32f-499d-90ce-60344f4e899a)

---

![Test 153317](https://github.com/user-attachments/assets/54b9c6f0-696b-4dbd-b951-bdcb4863057b)

---

![Test 153215](https://github.com/user-attachments/assets/cfc0ec27-a7c2-45dc-836d-118c6fff2a46)

---

![Test 153202](https://github.com/user-attachments/assets/0e0a0f09-2aad-4b20-8349-a7bcaed2f4cd)

---

![Test 153121](https://github.com/user-attachments/assets/e51ea890-e479-489f-aadb-17cf8b895e3d)

---

![Test 153038](https://github.com/user-attachments/assets/4844f14d-8618-4ce1-85d5-4d43d629f703)

---

![Test 152959](https://github.com/user-attachments/assets/08eab87c-ee6e-4bd3-afc0-28d8e7880f97)

---

![Test 153654](https://github.com/user-attachments/assets/0fff6f68-f326-48b4-acea-4fb03d7c9bfa)

---

