AI-Powered Predictive Hiring & Career Intelligence System
=========================================================

📖 Overview
-----------

The **AI-Powered Predictive Hiring & Career Intelligence System** is an end-to-end platform designed to modernize candidate evaluation and career guidance. By combining traditional machine learning (XGBoost) with Generative AI (Google Gemini), the system automates resume analysis, predicts candidate-role fit, and provides personalized career coaching.

Built to operate on a **hybrid cloud model**, the solution leverages on-premise infrastructure (OpenShift) for data sovereignty while utilizing best-in-class cloud LLMs for reasoning and interaction. This approach allows institutions to scale support to thousands of candidates while maintaining strict control over sensitive personal data.

**Key Value Propositions:**

*   **Operational Efficiency:** Dramatically reduces manual screening time for HR teams.
    
*   **Data-Driven Decisions:** Improves hiring accuracy using predictive modeling and SHAP-based explainability.
    
*   **Candidate Experience:** Offers 24/7 AI career counseling and mock interview practice.
    
*   **Strategic ROI:** Proven TCO reduction through optimized hybrid cloud deployment.
    

🏗️ Architecture Design
-----------------------

<img width="2148" height="1614" alt="Untitled diagram-2025-12-01-075958" src="https://github.com/user-attachments/assets/621fb913-df10-4038-a9f2-1106fdf512d3" />


✨ Key Features
--------------

### 1\. Predictive Hiring Engine  

*   **Automated Resume Parsing:** Extracts key skills, education, and experience from PDF resumes using OCR and LLM extraction.
    
*   **Candidate Fit Prediction:** Utilizes a robust **XGBoost Classifier** to predict the probability of a candidate being hired based on historical data.
    
*   **Explainable AI (XAI):** Integrated **SHAP (SHapley Additive exPlanations)** values to provide transparent reasons behind every prediction (e.g., "High impact: Years of Experience").
    
*   **Executive Dashboard:** Real-time visualization of global hiring trends, demographic breakdowns, and success rates.


### 2\. GenAI Career Counselor & Interviewer

*   **RAG-Based Action Plans:** Generates personalized career development plans by combining candidate data with real-time Google Search results for courses and meetups.
    
*   **Mock Interview Simulator:** An interactive chat interface where an AI persona conducts role-specific interviews, asking follow-up questions based on the candidate's previous answers.
    
*   **Skill Gap Analysis:** Automatically identifies weaknesses in a profile and suggests specific remediation steps.
    

### 3\. Advanced ROI & TCO Calculator  

*   **Hybrid Cloud Comparison:** Simulates costs across **AWS Native, Azure Native, GCP Native**, and **OpenShift (ROSA/ARO/Self-Managed)**.
    
*   **Granular Cost Drivers:** Accounts for:
    
    *   **Infrastructure:** Compute nodes, GPU endpoints, storage, and load balancers.
        
    *   **AI Consumption:** LLM token usage (Input/Output) and training hours.
        
    *   **Labor Costs:** Estimation of engineering teams (DevOps, Data Scientists, PMs).
        
*   **Visual Reports:** Generates detailed Matplotlib charts and breakdown tables for financial decision-making.
    

🛠️ Technology Stack
--------------------

*   **Frontend & UI:** Gradio (Multi-tab interface)
    
*   **Machine Learning:** XGBoost (Classification), Scikit-Learn (Preprocessing Pipelines)
    
*   **Explainability:** SHAP
    
*   **Generative AI:** Google Gemini 1.5 Flash (via Google GenAI API)
    
*   **Data Processing:** Pandas, NumPy, OpenPyXL
    
*   **Visualization:** Matplotlib, Plotly
    
*   **Infrastructure Logic:** Custom Python simulation for Cloud vs. On-Prem pricing


🛠️ Development Cycle
--------------------
<img width="1158" height="893" alt="Hiring_System_Development_Cycle" src="https://github.com/user-attachments/assets/3c5566b9-5516-49dd-8649-75b841f5dbbc" />


🛠️ System Architecture : Hybrid Architecture
--------------------
<img width="1021" height="767" alt="Hiring_System_Architecture_Hybrid" src="https://github.com/user-attachments/assets/675d9d87-1ba2-441a-a340-86df427e4145" />


🚀 Installation & Setup
-----------------------

### Prerequisites

*   Python 3.8 or higher
    
*   Google Cloud API Key (for Gemini LLM features)
    

### 1\. Clone the Repository

git clone [https://github.com/your-username/ai-hiring-system.git](https://github.com/your-username/ai-hiring-system.git)  cd ai-hiring-system   `

### 2\. Install Dependencies

pip install gradio xgboost shap openpyxl httpx pandas numpy scikit-learn matplotlib plotly pypdf   `

### 3\. Environment Configuration

Set your Google API key as an environment variable or within the script secrets configuration (if using Colab).

### 4\. Setup your GOOGLE_API_KEY
In your local environment  export GOOGLE_API_KEY="your_api_key_here"   `

💻 Usage
--------

### Running the Hiring System

This script launches the main application, including the candidate profile evaluation, dashboard, and mock interviewer.

python course4_hiring_system_v1_4.py   `

_Access the UI at http://localhost:7860_

### Running the ROI Calculator

This standalone tool allows stakeholders to estimate the financial impact of the system.

python roi_calculator_advanced_py.py   `

_Access the Calculator at http://localhost:7860_

📊 ROI Study Highlights
-----------------------

The included ROI study (roi\_calculator\_advanced\_py.py) demonstrates the financial viability of the platform. Key findings from the logic include:

1.  **Hybrid Efficiency:** While hyperscaler "Serverless" options offer low entry costs, **OpenShift-based hybrid deployments** become significantly more cost-effective as candidate volume exceeds 5,000/month due to predictable node pricing versus per-request metering.
    
2.  **Labor Optimization:** The calculator quantifies the reduction in manual screening labor (PMs, Recruiters) against the cost of maintaining the AI infrastructure.
    
3.  **Token Economics:** Detailed analysis of RAG (Retrieval-Augmented Generation) costs, factoring in daily query volume and token limits.
    

   

📄 License
----------

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.
