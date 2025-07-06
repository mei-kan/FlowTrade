# 🌀 FlowTrade

**On-Chain DCA + Limit Orders Terminal**
*Built for the Massa Buildathon – Wave 1*

---

## 💡 Project Overview

**FlowTrade** is a concept-stage DeFi terminal designed to run entirely on-chain using **Massa’s Autonomous Smart Contracts (ASC)** and **DeWeb frontend hosting**. The core idea is to provide users with **fully automated, trustless trading tools**—specifically:

* **Limit Orders**: Set-and-forget orders with automatic expiry
* **Dollar-Cost Averaging (DCA)**: Recurring token swaps at predefined intervals

These tools are widely used in both CeFi and DeFi, but are often reliant on bots, off-chain triggers, or external automation services like Gelato or Chainlink Keepers. **FlowTrade removes all such dependencies.**

---

## 🌐 Why Massa?

FlowTrade is only possible because of **Massa’s unique capabilities**:

| Massa Feature                        | How FlowTrade Uses It                                                       |
| ------------------------------------ | --------------------------------------------------------------------------- |
| **Autonomous Smart Contracts (ASC)** | Automate order execution and DCA logic with zero off-chain dependencies     |
| **Deferred Calls**                   | Schedule future operations (e.g., periodic swaps, timed order expiry)       |
| **DeWeb**                            | Host the frontend directly on-chain for a truly unstoppable user experience |

---

## 🔍 Problem Statement

Traditional DeFi automation is not really autonomous. Most protocols rely on:

* Centralized schedulers
* External automation (e.g., Gelato, Chainlink)
* Bots or off-chain scripts

This creates friction, cost, and failure points. It also undermines the principles of decentralization and trustlessness.

---

## 🧠 The FlowTrade Vision

**FlowTrade** aims to become the go-to solution for:

* **Retail investors** wanting to automate DCA strategies securely and easily
* **Traders** needing trustless, non-custodial limit orders
* **Builders** seeking a reference architecture for ASC-based trading tools

---

## 🛠 Key Features (Planned)

| Feature              | Description                                                         |
| -------------------- | ------------------------------------------------------------------- |
| 📈 Limit Orders      | Users can set price-triggered swaps with expiry times               |
| 🔁 DCA Engine        | Automate recurring token purchases or sales (e.g., buy every 24h)   |
| ⏱ Deferred Execution | Deferred calls execute logic on-chain at future timestamps          |
| 🧱 DeWeb Frontend    | Entire UI hosted on-chain—no servers, no IPFS, no downtime          |
| 🔐 No Admin          | Fully autonomous contracts, no upgradable logic or privileged roles |

---

## 🧰 Technical Design (Concept)

### 1. Limit Order Flow

* User sets token pair, target price, expiry timestamp
* Order is stored in a smart contract
* On every relevant trigger (e.g., block event), contract checks condition
* If met, it swaps; if expired, it self-cancels

### 2. DCA Flow

* User defines swap amount, interval, duration
* Contract sets up a schedule using deferred calls
* Each deferred call performs the swap
* Stops when max count/duration is reached

---

## 🔓 Autonomy Goals

FlowTrade is being designed to:

* Operate **indefinitely without intervention**
* Have **no off-chain dependencies**
* Be **fully open-source and reproducible**

In short: a **DeFi protocol that lives and breathes entirely on-chain.**

---

## 📦 Submission Notes

Since FlowTrade is currently in the **ideation phase**, this submission includes:

* ✅ Conceptual README
* ✅ Technical architecture draft (included in `/docs`)
* ❌ Codebase (to be developed in Wave 2/3)
* ❌ Frontend (planned post-prototype)
* ❌ Demo video (not applicable for idea-only submission)
