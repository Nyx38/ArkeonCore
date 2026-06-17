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

<img width="1890" height="951" alt="Ekran görüntüsü 2026-06-17 153654" src="https://github.com/user-attachments/assets/e2564fa0-0f4f-462b-8a08-cdaae8c9e775" />
<img width="827" height="712" alt="Ekran görüntüsü 2026-06-17 153437" src="https://github.com/user-attachments/assets/456273e6-3908-4730-8156-0b39ba1c6525" />
<img width="1285" height="1016" alt="Ekran görüntüsü 2026-06-17 153416" src="https://github.com/user-attachments/assets/efcffa2f-4194-4b2b-b245-59321c500791" />
<img width="1332" height="887" alt="Ekran görüntüsü 2026-06-17 153317" src="https://github.com/user-attachments/assets/6d819822-6d4a-4544-a8a9-3d7cc1df8d72" />
<img width="1287" height="765" alt="Ekran görüntüsü 2026-06-17 153215" src="https://github.com/user-attachments/assets/07db1b00-a9dd-404d-b2d2-717a2b317dd4" />
<img width="1285" height="247" alt="Ekran görüntüsü 2026-06-17 153202" src="https://github.com/user-attachments/assets/c3edb7c5-0b09-40f3-a2d2-4d6f1a7ae3c6" />
<img width="1283" height="886" alt="Ekran görüntüsü 2026-06-17 153121" src="https://github.com/user-attachments/assets/5ac5cf61-7fdd-49c6-88a4-c31120d2e19c" />
<img width="1277" height="635" alt="Ekran görüntüsü 2026-06-17 153038" src="https://github.com/user-attachments/assets/a97a6a60-ee0e-4d39-9362-fcbf5b76c8ea" />
<img width="1281" height="1017" alt="Ekran görüntüsü 2026-06-17 152959" src="https://github.com/user-attachments/assets/8c915b04-96a1-402b-b81b-dcb17fa3a957" />
<img width="751" height="577" alt="Ekran görüntüsü 2026-06-17 153454" src="https://github.com/user-attachments/assets/8d3a5cbe-9637-41f5-a32c-246268f7b53f" />



<img width="553" height="887" alt="Ekran görüntüsü 2026-06-16 202648" src="https://github.com/user-attachments/assets/b42ca1b5-a179-46d7-bafc-9cd0aa617786" />
<img width="555" height="887" alt="Ekran görüntüsü 2026-06-16 202638" src="https://github.com/user-attachments/assets/b148e277-f972-48bd-aa75-2d794466fc8f" />
<img width="565" height="896" alt="Ekran görüntüsü 2026-06-16 202619" src="https://github.com/user-attachments/assets/0638ab89-64cb-4aee-9b74-d508326e2323" />


