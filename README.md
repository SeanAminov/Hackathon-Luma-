Autonomous On-Chain Detective Agent
A Multi-Agent AI System for Real-Time Rugpull Prediction and Blockchain Fraud Detection
1. Abstract

The Autonomous On-Chain Detective Agent is a real-time, agentic AI security system designed to detect and predict rugpulls, liquidity-based exploits, and malicious on-chain behavior before damage occurs. The system continuously monitors blockchain activity, computes a quantitative rugpull probability score, and generates structured explanations of suspicious events.

𝑅
∈
[
0
,
100
]
R∈[0,100]

This work integrates blockchain analytics, agent-based modeling, anomaly detection, and LLM interpretability into a single coherent framework optimized for decentralized security environments.

2. Introduction

Decentralized finance has introduced new attack surfaces, including liquidity removal attacks, honeypots, privilege exploits, and coordinated wallet manipulations. Existing solutions rely primarily on static analysis or post-exploit forensics.

This project introduces a real-time, predictive, agentic security architecture intended to:

Continuously observe on-chain behavior

Detect abnormal liquidity or wallet flows

Predict rugpull probability

Generate human-readable diagnostic explanations

Alert users before financial damage occurs

3. Multi-Agent System Architecture
𝐴
=
{
𝐴
listen
,
𝐴
pattern
,
𝐴
anomaly
,
𝐴
risk
,
𝐴
explain
,
𝐴
alert
}
A={A
listen
	​

,A
pattern
	​

,A
anomaly
	​

,A
risk
	​

,A
explain
	​

,A
alert
	​

}
3.1 Agent Descriptions
A_{\text{listen}} — Blockchain Listener Agent

Subscribes to WebSocket transaction streams

Observes liquidity movements, swaps, transfers, and owner actions

A_{\text{pattern}} — Pattern Recognition Agent

Identifies classical rugpull indicators

Detects liquidity withdrawal, owner dumping, mint spikes, and privilege misuse

A_{\text{anomaly}} — Anomaly Detection Agent

Computes statistical or ML-based anomaly scores

Supports: Isolation Forest, Z-score, and GNN wallet clustering

A_{\text{risk}} — Risk Scoring Agent

Computes combined rugpull probability:

𝑅
=
40
𝑠
liq
+
30
𝑠
owner
+
15
𝐴
+
15
𝑠
priv
R=40s
liq
	​

+30s
owner
	​

+15A+15s
priv
	​


Normalized to:

𝑅
=
min
⁡
(
100
,
𝑅
)
R=min(100,R)
A_{\text{explain}} — Explanation Agent

Transforms structured signals into natural-language reasoning using LLMs.

A_{\text{alert}} — Notification Agent

Dispatches security notifications via Telegram or Discord.

4. System Pipeline
A_listen → A_pattern → A_anomaly → A_risk → A_explain → A_alert + Dashboard

5. Methodology
5.1 On-Chain Event Stream

Let the event stream be:

𝑇
=
{
𝑡
1
,
𝑡
2
,
…
,
𝑡
𝑛
}
T={t
1
	​

,t
2
	​

,…,t
n
	​

}

The listener agent generates an ordered buffer of blockchain actions for downstream analysis.

5.2 Rugpull Signal Vector

The system maintains a binary event vector:

𝑆
=
[
𝑠
liq


𝑠
owner


𝑠
mint


𝑠
honeypot


𝑠
priv
]
∈
{
0
,
1
}
5
S=
	​

s
liq
	​

s
owner
	​

s
mint
	​

s
honeypot
	​

s
priv
	​

	​

	​

∈{0,1}
5

Each signal corresponds to a high-risk behavior class.

5.3 Anomaly Modeling

Given a feature matrix 
𝑋
X, anomaly score is defined as:

𝐴
=
𝑓
(
𝑋
)
∈
[
0
,
1
]
A=f(X)∈[0,1]

Where 
𝑓
f may represent:

Isolation Forest

Z-score deviation

Basic GNN embeddings

5.4 Risk Assessment

The final rugpull probability score is computed via weighted aggregation of heuristic + model signals.

𝑅
=
𝑤
1
𝑠
liq
+
𝑤
2
𝑠
owner
+
𝑤
3
𝐴
+
𝑤
4
𝑠
priv
R=w
1
	​

s
liq
	​

+w
2
	​

s
owner
	​

+w
3
	​

A+w
4
	​

s
priv
	​


Where:

𝑤
1
=
40
,
𝑤
2
=
30
,
𝑤
3
=
15
,
𝑤
4
=
15
w
1
	​

=40,w
2
	​

=30,w
3
	​

=15,w
4
	​

=15
5.5 Explanation Generation

Given input state:

𝐸
=
{
𝑆
,
𝐴
,
Δ
𝐿
,
Δ
𝑊
,
Δ
𝑆
}
E={S,A,ΔL,ΔW,ΔS}

The explanation agent produces:

Explanation
=
LLM
(
𝐸
)
Explanation=LLM(E)

The resulting narrative is intended to be concise, interpretable, and suitable for end-user consumption.

6. Implementation
6.1 Technologies Used
Component	Technology
Blockchain Interface	Web3.py (Alchemy WebSocket)
Backend	Python, FastAPI
AI Reasoning	OpenAI GPT / Claude / Llama
ML Models	scikit-learn / PyTorch
Visualization	Streamlit
Alerts	Telegram Bot API / Discord Webhooks
Storage	SQLite / Redis
7. Experimental Demonstration

A controlled testnet environment is used to demonstrate the effectiveness of the system:

Deploy ERC-20 token

Provide liquidity

Simulate rugpull behavior

Observe system detection in real-time

During testing, the system produced alerts of the form:

Liquidity decreased by 92% within 2 blocks. Owner transferred a large supply to an unverified wallet. Rugpull probability estimated at 97%.

8. Results

The system demonstrates:

High sensitivity to rapid liquidity withdrawals

Accurate detection of owner-privilege misuse

Effective anomaly identification across transaction flows

Strong interpretability via LLM-generated explanations

9. Conclusion

This project demonstrates the feasibility and value of a multi-agent AI framework for real-time rugpull prediction and fraud detection. By integrating blockchain streaming data, heuristic pattern detection, anomaly modeling, and language-model explanation, the system provides a novel defense layer for decentralized ecosystems.

10. Team

Team Name
2025 Scoop AI Hackathon — Silicon Valley Bowl
Santa Clara, California

11. Keywords

Blockchain Security
Rugpull Detection
Anomaly Modeling
Agentic AI
Smart Contract Forensics
DeFi Risk Analysis

If you want:

A LaTeX PDF version

A Beamer pitch deck

A math-heavy appendix section

Or a supplementary algorithm section
