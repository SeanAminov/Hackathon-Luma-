\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{hyperref}
\usepackage{verbatim}
\usepackage{geometry}
\geometry{a4paper, margin=1in}

% Define a custom command for the title block
\newcommand{\projecttitle}[2]{
    \begin{center}
    \vspace*{1cm}
    {\Huge \textbf{#1}} \\
    \vspace{0.5cm}
    {\large #2}
    \vspace{1cm}
    \hrule
    \end{center}
}

\title{}
\author{}
\date{}

\begin{document}

\projecttitle{Autonomous On-Chain ``Detective Agent''}
{🏆 Rugpull + Fraud Hunter: AI-Powered Blockchain Security Monitoring}

\section*{1. 🌟 Project Overview}

The **Autonomous On-Chain Detective Agent** is an S-tier AI system designed to actively monitor live blockchain transactions, predict potential rugpulls and scams, and provide actionable security intelligence. It moves beyond simple heuristics by leveraging advanced AI techniques to detect complex, multi-step fraud patterns in real-time, offering a critical defense layer for DeFi investors.

\section*{2. 🔥 Features and Capabilities}

\begin{itemize}
    \item \textbf{Live Transaction Monitoring:} Hooks into blockchain nodes (via WebSockets) to analyze transactions as they are mined.
    \item \textbf{Anomaly Detection:} Analyzes abnormal \textbf{wallet flows} and detects suspicious \textbf{liquidity movements} (e.g., massive withdrawal/deposit pairs).
    \item \textbf{Risk Prediction:} Predicts \textbf{rugpull probability} in real-time.
    \item \textbf{Contract Flagging:} Identifies and flags risky smart contracts (e.g., contracts with hidden backdoors or unusually high owner permissions).
    \item \textbf{Pattern Learning:} Learns and evolves by analyzing historic exploits (Flash Loans, exit scams, honeypots, etc.).
\end{itemize}

\section*{3. 💡 Output and Deliverables}

The agent provides clear, actionable intelligence to the user:

\begin{itemize}
    \item \textbf{Risk Score (0--100):} A quantifiable measure of the immediate threat.
    \item \textbf{Explanation:} A concise, human-readable summary of the detected threat (e.g., ``Owner pulled 70\% of liquidity in 2 minutes'').
    \item \textbf{Timeline of Events:} A chronological list of suspicious on-chain activity.
    \item \textbf{Recommended Action:} Clear guidance (\texttt{sell}, \texttt{hold}, \texttt{avoid}, \texttt{blacklist}).
    \item \textbf{Alert Bot:} Real-time notifications via \textbf{Discord/Telegram}.
\end{itemize}

\section*{4. 🛠️ Technical Stack}

\subsection*{4.1. Core Technologies}
\begin{itemize}
    \item \textbf{Blockchain Connection:} \texttt{web3.py} (Python Library) for interaction.
    \item \textbf{Data Source:} Etherscan / Alchemy WebSocket API for live data feeds.
    \item \textbf{Frontend:} \texttt{Streamlit} for an interactive dashboard.
    \item \textbf{Alerting:} Python Telegram Bot API.
\end{itemize}

\subsection*{4.2. Multi-Agent System Architecture}
The system is built on a multi-agent design for robust analysis:
\begin{itemize}
    \item \textbf{Reasoner Agent:} Processes raw data and forms logical deductions.
    \item \textbf{Pattern Matcher Agent:} Identifies known exploit signatures.
    \item \textbf{Exploit Library:} A historical database of scam patterns and contract vulnerabilities.
    \item \textbf{Risk Agent:} Computes the final Risk Score based on inputs from all other agents.
\end{itemize}

\subsection*{4.3. AI/ML Component}
\begin{itemize}
    \item A light \textbf{Graph Neural Network (GNN)} or a dedicated \textbf{Anomaly Detector} model is used to analyze complex, non-linear relationships in wallet-to-wallet transactions and liquidity pool dynamics.
\end{itemize}

\section*{5. 🚀 Getting Started}

\subsection*{5.1. Prerequisites}
\begin{itemize}
    \item Python 3.9+
    \item Alchemy/Infura WebSocket Endpoint
    \item Telegram Bot Token (for alerting)
\end{itemize}

\subsection*{5.2. Installation}
\begin{verbatim}
git clone https://github.com/YourUsername/DetectiveAgent.git
cd DetectiveAgent
pip install -r requirements.txt
\end{verbatim}

\subsection*{5.3. Configuration}
Create a \texttt{.env} file in the root directory and populate it:
\begin{verbatim}
WEB3_WS_URL=wss://eth-mainnet.alchemyapi.io/v2/YOUR_API_KEY
TELEGRAM_BOT_TOKEN=YOUR_TELEGRAM_BOT_TOKEN
TELEGRAM_CHAT_ID=YOUR_CHAT_ID
\end{verbatim}

\subsection*{5.4. Running the Agent}
\begin{verbatim}
# Start the core AI agent for monitoring
python agent_main.py

# Start the Streamlit dashboard
streamlit run dashboard.py
\end{verbatim}

\section*{6. 🌟 Bonus Shockers (Future/Advanced Integrations)}

\begin{itemize}
    \item \textbf{Autonomous Mitigation:} Connect the Risk Agent to a custom smart contract that is authorized to \textbf{auto-lock/revoke spending permissions} on user funds if the risk score for a monitored token exceeds a defined threshold ($\text{Risk} > 90$).
    \item \textbf{SpoonOS Integration:} Integrate with the SpoonOS agent environment for decentralized, autonomous, and continuous monitoring, allowing the agent to function independently on a distributed infrastructure.
\end{itemize}

\end{document}
