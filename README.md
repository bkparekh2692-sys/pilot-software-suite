CyberTronix Enterprise: Secure Backend & AI Automation Suite
Overview
This repository contains the core modules of the CyberTronix Enterprise Portal, a Python-based suite of backend tools designed to handle multi-step coordination tasks, secure data processing, and AI-driven predictive modeling. Built with a focus on modular separation and secure-by-design architecture, the application isolates data ingestion, logic processing, and reporting layers to safely operate in live, non-mocked enterprise environments.

System Architecture & Modules
The application is structured into discrete, independent services ensuring robust state management and security:

1. Access Control & Routing (Home.py)
Acts as the central authentication gateway and session manager.

Persistent State: Utilizes session state tracking to manage user authentication and restrict unauthorized access to sensitive logic modules.

Dynamic UI Rendering: Employs CSS injection and conditional rendering to hide system navigation prior to secure access.

2. Transaction Anomaly Detection Engine (Fraud Detector.py)
An unsupervised machine learning module designed to parse and flag suspicious transaction behaviors.

Data Parsing: Ingests raw CSV data and programmatically cleans numerical inputs using regex.

Logic Processing: Implements the IsolationForest algorithm (via scikit-learn) to autonomously detect systemic financial anomalies without labeled data.

Reporting: Generates high-density technical feedback using Plotly scatter plots to visualize boundary violations.

3. AI Staffing Optimization Engine (Future Forecaster.py)
A predictive modeling service handling multi-turn coordination tasks to optimize physical resource allocation.

Time-Series Forecasting: Leverages Facebook's Prophet library to analyze historical sales data and project future demand.

Actionable Outputs: Translates raw predictive data into structured scheduling logic, automatically calculating the exact physical staffing resources required per shift.

4. Identity Guardian (Password_Auditor.py)
A secure API integration module that stress-tests credentials while maintaining strict data privacy.

k-Anonymity Protocol: Employs SHA-1 hashing to ensure plaintext passwords never leave the local environment.

Live API Integration: Uses the requests library to transmit only the first 5 characters of the hash to the Have I Been Pwned API, matching the returned suffixes locally to prevent privacy leaks.

5. Network Vulnerability Scanner (Security Audit.py)
An active adversarial probing tool used to stress-test target architectures.

Multi-Threading: Executes high-speed, concurrent port scans across target IPs using Python's socket and threading libraries to identify exposed attack surfaces.

Threat Identification: Specifically hunts for critical infrastructure vulnerabilities, including exposed RDP (Port 3389) and SMB (Port 445) services.

Tech Stack
Language: Python 3.x

Framework: Streamlit (Frontend/State Management)

Machine Learning: Scikit-Learn (Isolation Forest), Prophet (Time-Series)

Data Processing: Pandas, NumPy

Security & Networking: Hashlib, Socket, Threading, Requests

Installation & Setup
Clone the repository:
git clone [https://github.com/yourusername/cybertronix-enterprise.git](https://github.com/yourusername/cybertronix-enterprise.git)
cd cybertronix-enterprise

Install required dependencies:
pip install -r requirements.txt

Initialize the Application:
streamlit run Home.py

Note: Default access key for the local demo is CT-2026-VIP
