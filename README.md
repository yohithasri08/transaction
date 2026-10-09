# Proposed Solution:Adaptive cybersecurity framework for real time fraud prevention


**OPCODE IMPACT 2026 | Hackathon Submission**


**Track >>>>>>   Post Quantum Technology**

**Team ID:** OPC002

## 1. Problem Statement
Financial transactions are increasingly exposed to evolving and sophisticated fraud patterns. Traditional rule-based systems may struggle to adapt to changing transaction behaviour, while AI models can produce uncertain predictions. Therefore, a multi-stage security system is needed to detect suspicious transactions, verify uncertain cases, and maintain tamper-evident audit records.

## 2. Solution Title
Q-Sentinel – AI-Driven Multi-Stage Financial Transaction Security

## 3. Solution Description
Q-Sentinel is an AI-driven financial fraud detection system that uses XGBoost to analyse transaction behaviour and generate fraud-risk scores. Transactions with low-confidence predictions are selectively verified using a Variational Quantum Circuit (VQC). Based on the assessment, the system automatically approves or blocks transactions and generates alerts. Blockchain is used to maintain tamper-evident records of final transaction decisions, improving traceability and auditability.

## 4. Architecture Diagram

![Q-Sentinel Architecture Diagram](https://github.com/user-attachments/assets/ea29f44f-0a77-4dd8-843a-dfbfb9d97529)


Transaction details are captured using an ESP32 and RC522 NFC module with an NFC card/tag to simulate transaction input. XGBoost evaluates the transaction and generates a fraud-risk score. High-confidence predictions proceed according to the system's decision logic, while uncertain cases are sent to VQC for secondary verification. The system then makes an approval or blocking decision, and the final decision is recorded on the blockchain for tamper-evident auditing.


## 5. Technology Stack
- Frontend: Streamlit
- Backend: Python
- Database: Blockchain-based audit records
- Other Technologies:
 -XGBoost: Initial fraud-risk detection.
-Variational Quantum Circuit (VQC): Secondary verification of uncertain transactions.
-Blockchain: Tamper-evident logging of final decisions.
-ESP32: Captures and processes transaction-related input.
-RC522 NFC Module: Reads NFC-based transaction information.
-NFC Card/Tag: Simulates financial transaction input.
-Python Environment: Implements transaction processing and fraud detection.

## 6. Quick Start Guide
**Prerequisites:**
Python 3.10 or later

Git

pip (Python package manager)

Arduino IDE or PlatformIO (for ESP32 firmware)

ESP32 DevKit V1

RC522 RFID/NFC reader module

13.56 MHz RFID/NFC card

OLED display, RGB LED, buzzer, and optional push buttons

USB data cable for ESP32

**Installation & Execution:**
```bash
# 1. repository
https://github.com/yohithasri08/transaction


# 2. Create and activate a virtual environment
python -m venv venv

# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate

# 3. Install backend dependencies
pip install -r requirements.txt


# 5. Train or load the fraud-detection model
python train_model.py


# 6. Start the backend server
python app.py
(or)
uvicorn main:app --reload

cd c:\Users\anish\OneDrive\Desktop\AWS_HACk\quantumLedger\backend                                 
>> $env:RFID_SERIAL_PORT = "COM13"                                                                                                             
>> $env:RFID_SERIAL_BAUD = "115200"                                                                                                            
>> python app.py(Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned) ; (& c:\Users\anish\OneDrive\Desktop\AWS_HACk\.venv\Scripts\Activate.ps1)
```

## 7. Output Screenshots
![Output Screenshot](docs/output.png)

[Briefly describe the output.]

## 8. Future Scope
Q-Sentinel can be extended into a more scalable, adaptive, and reliable financial fraud detection framework through the following enhancements:

Advanced Fraud Detection: Integrate diverse real-world transaction datasets and explore advanced machine learning techniques to identify evolving fraud patterns and improve detection performance.

Enhanced Quantum Machine Learning: Experiment with different Variational Quantum Classifier (VQC) architectures and compare their performance against classical models to evaluate their effectiveness in handling uncertain fraud predictions.

Adaptive Confidence-Based Routing: Develop dynamic confidence thresholds to route uncertain transactions for additional verification while balancing fraud detection, false positives, and processing time.

Advanced Blockchain Auditing: Extend the tamper-evident audit trail with transaction hashes, timestamps, and decision metadata to improve traceability, transparency, and investigation support while protecting sensitive information.

Real-Time Transaction Integration: Explore integration with payment gateways, banking APIs, and transaction simulators to evaluate the system under realistic transaction-processing conditions.

Enhanced Hardware Integration: Expand the ESP32 and RFID/NFC prototype with additional transaction inputs, improved status indicators, and secure communication between the hardware terminal and backend.

Performance Monitoring Dashboard: Develop a dashboard to visualize transaction activity, fraud-risk scores, system decisions, model confidence, and audit records.

Model Monitoring and Adaptation: Introduce data-drift monitoring, periodic model evaluation, and controlled retraining strategies to adapt to changing fraud patterns.

Privacy and Security Enhancements: Implement secure communication, authentication, access control, and privacy-preserving audit mechanisms to protect transaction information.

Comprehensive Evaluation: Evaluate the framework using precision, recall, F1-score, ROC-AUC, false-positive rate, inference latency, and resource utilization. Compare the complete system with classical-only baselines to measure the actual contribution of each component.

### Long-Term Vision

The long-term goal is to evolve Q-Sentinel from a prototype into a modular financial transaction security platform that combines AI-based risk assessment, experimental quantum-assisted verification, and blockchain-backed auditability. Further development and rigorous testing can help assess its suitability for applications in digital payments, banking, and other transaction-based systems.

## 9. Team Contributions
| Yuvasri | quantum model |
| Anishika| ML model |
| Sahana sree  | backend |
| yohitha sri | frontend |

## 10. Tools Used
| Tool / Platform                   | Purpose / Why Used                                                                                                                                                                           
| Python                        | Main programming language for implementing the fraud detection pipeline and backend logic.                                                                                                   
| XGBoost                       | Used for primary machine learning-based transaction fraud-risk assessment.                                                                                                                   
| PennyLane                     | Used to develop and experiment with the Variational Quantum Classifier (VQC) for secondary assessment of uncertain predictions.                                                              
| Flask                         | Used to build API endpoints for communication between the frontend, hardware interface, and fraud detection backend.                                                                         
| Blockchain-Based Audit Logging| Uses a custom SHA-256 hash-chain mechanism in Python to link transaction decision records through cryptographic hashes, supporting tamper detection, data integrity verification, and transparent audit trails.
                                                                                         
| ESP32 DevKit V1               | Used as the microcontroller for the physical transaction demonstration.                                                                                                                      
| MFRC522 RFID/NFC Reader       | Used to read compatible RFID/NFC cards to simulate transaction initiation.                                                                                                                   
| OLED Display                  | Used to display transaction status and system responses during the hardware demonstration.                                                                                                                                                                                             
| Git & GitHub                  | Used for version control, source-code management, documentation, and project collaboration.                                                                                                  
| AI-Assisted Development Tools | Used for brainstorming, understanding technical concepts,  AI-generated suggestions were reviewed and adapted to the project requirements. 
