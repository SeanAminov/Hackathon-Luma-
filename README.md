# 🏆 Autonomous On-Chain "Detective Agent"

## Rugpull + Fraud Hunter: AI-Powered Blockchain Security Monitoring

---

## 1. 🌟 Project Overview

The **Autonomous On-Chain Detective Agent** is an S-tier AI system designed to actively monitor live blockchain transactions, predict potential **rugpulls** and **scams**, and provide actionable security intelligence.

It moves beyond simple heuristics by leveraging advanced AI techniques to detect complex, multi-step fraud patterns in real-time, offering a critical defense layer for DeFi investors.

---

## 2. 🔥 Features and Capabilities

* **Live Transaction Monitoring:** Hooks into blockchain nodes (via WebSockets) to analyze transactions as they are mined.
* **Anomaly Detection:** Analyzes abnormal **wallet flows** and detects suspicious **liquidity movements** (e.g., massive withdrawal/deposit pairs).
* **Risk Prediction:** Predicts **rugpull probability** in real-time.
* **Contract Flagging:** Identifies and flags risky smart contracts (e.g., contracts with hidden backdoors or unusually high owner permissions).
* **Pattern Learning:** Learns and evolves by analyzing historic exploits (Flash Loans, exit scams, honeypots, etc.).

---

## 3. 💡 Output and Deliverables

The agent provides clear, actionable intelligence to the user:

* **Risk Score (0–100):** A quantifiable measure of the immediate threat.
* **Explanation:** A concise, human-readable summary of the detected threat (e.g., "Owner pulled 70% of liquidity in 2 minutes").
* **Timeline of Events:** A chronological list of suspicious on-chain activity.
* **Recommended Action:** Clear guidance (`sell`, `hold`, `avoid`, `blacklist`).
* **Alert Bot:** Real-time notifications via **Discord/Telegram**.

---

## 4. 🛠️ Technical Stack

### 4.1. Core Technologies

* **Blockchain Connection:** `web3.py` (Python Library) for interaction.
* **Data Source:** Etherscan / Alchemy WebSocket API for live data feeds.
* **Frontend:** `Streamlit` for an interactive dashboard.
* **Alerting:** Python Telegram Bot API.

### 4.2. Multi-Agent System Architecture

The system is built on a multi-agent design for robust analysis: 

* **Reasoner Agent:** Processes raw data and forms logical deductions.
* **Pattern Matcher Agent:** Identifies known exploit signatures.
* **Exploit Library:** A historical database of scam patterns and contract vulnerabilities.
* **Risk Agent:** Computes the final Risk Score based on inputs from all other agents.

### 4.3. AI/ML Component

* A light **Graph Neural Network (GNN)** or a dedicated **Anomaly Detector** model is used to analyze complex, non-linear relationships in wallet-to-wallet transactions and liquidity pool dynamics.

---

## 5. 🚀 Getting Started

### 5.1. Prerequisites

* Python 3.9+
* Alchemy/Infura WebSocket Endpoint
* Telegram Bot Token (for alerting)

### 5.2. Installation

```bash
git clone [https://github.com/YourUsername/DetectiveAgent.git](https://github.com/YourUsername/DetectiveAgent.git)
cd DetectiveAgent
pip install -r requirements.txt
