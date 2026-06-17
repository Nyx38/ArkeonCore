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




