# 🤖 AI Recruitment Automation

An AI-powered recruitment automation workflow designed to automate the initial CV screening and candidate selection process.

The system receives candidate applications, processes their CVs, analyzes each profile using an AI model, assigns a score based on predefined recruitment criteria, and automatically sends qualified candidate applications to the HR recruiter by email.

## 🚀 Project Demo

🎥 **Demo video:** [Watch the AI Recruitment Automation Demo](https://youtu.be/UjZ4Hb_Wp0Y?si=ggDmqYOvbgNFwt8e)

## 📌 Project Overview

Recruitment teams often spend significant time manually reviewing CVs and comparing candidate profiles with job requirements.

This project automates the initial candidate screening process by combining **AI, workflow automation, and Google APIs**.

The workflow analyzes each candidate's CV according to predefined criteria. After generating a candidate score, the system compares it with a predefined minimum threshold.

* If the candidate's score **meets or exceeds the threshold**, the candidate's application is automatically forwarded to the HR recruiter by email.
* If the score is **below the threshold**, the candidate remains recorded in the recruitment database without being forwarded automatically.

## ⚙️ How It Works

The complete workflow follows these steps:

1. A candidate submits their application through a **Google Form**.
2. The candidate's CV is uploaded and stored in **Google Drive**.
3. The workflow is triggered and retrieves the candidate's information and CV.
4. The CV content is extracted and prepared for AI analysis.
5. The AI analyzes the candidate's profile according to the **job description and predefined recruitment criteria**.
6. The system generates a **candidate score**.
7. The score is compared with a **predefined minimum threshold**.
8. The candidate's information and evaluation are recorded in **Google Sheets using the Google Sheets API**.
9. If the candidate reaches the required score, the complete candidate application is automatically sent to the **HR recruiter by email using the Gmail API**.
10. The recruiter receives the qualified candidate's application without having to manually review every submitted CV.

### Architecture / Workflow

![AI Recruitment Automation Workflow](assets/workflow.png)

## ✨ Key Features

* 📄 Automated CV processing
* 🤖 AI-powered CV analysis
* 🎯 Candidate matching against job requirements
* 📊 Automated candidate scoring
* ⚖️ Predefined score threshold for candidate selection
* 📋 Automatic candidate data management with Google Sheets API
* 📧 Automatic HR notifications using Gmail API
* 📎 Automatic forwarding of qualified candidate applications
* 🔄 End-to-end recruitment workflow automation
* 🐳 Self-hosted workflow execution with Docker

## 🧠 AI-Powered Candidate Evaluation

The project uses a local Large Language Model (LLM) through **Ollama** to analyze candidate CVs.

The AI evaluates the candidate according to predefined job requirements, which can include:

* 🎓 Academic background
* 💻 Technical skills
* 🛠️ Required technologies
* 📚 Relevant experience
* 📌 Job-specific requirements

The evaluation produces a candidate score that is then compared with a predefined threshold.

For example:

```text
Candidate CV
     ↓
AI Analysis
     ↓
Candidate Score
     ↓
Score ≥ Required Threshold?
     ↓
   ┌───────────────┐
   │               │
  YES              NO
   ↓               ↓
Send to HR      Store result
by email        in database
```

The threshold can be adapted according to the recruitment requirements.

## 🔌 Google APIs Integration

The workflow integrates Google services through their APIs to automate the recruitment process.

### Google Forms

Used to collect candidate application information and CV submissions.

### Google Drive API

Used to access and retrieve candidate CV files stored in Google Drive.

### Google Sheets API

Used to automatically store and organize:

* Candidate information
* Evaluation results
* Candidate scores
* Screening status

### Gmail API

Used to automatically send qualified candidate applications to the HR recruiter when the candidate reaches the predefined score threshold.

This allows the workflow to connect the candidate application process directly to the recruiter's email workflow.

## 🛠️ Technologies

| Technology            | Purpose                               |
| --------------------- | ------------------------------------- |
| **n8n**               | Workflow automation and orchestration |
| **Docker**            | Self-hosted execution environment     |
| **Ollama**            | Local LLM execution                   |
| **Llama 3.2**         | AI-powered CV analysis                |
| **Google Forms**      | Candidate application collection      |
| **Google Drive API**  | CV file retrieval                     |
| **Google Sheets API** | Candidate data and evaluation storage |
| **Gmail API**         | Automated HR email notifications      |

## 🔄 End-to-End Recruitment Process

```text
Candidate
    ↓
Google Form
    ↓
CV Upload
    ↓
Google Drive
    ↓
n8n Workflow
    ↓
CV Extraction
    ↓
AI Analysis
    ↓
Candidate Score
    ↓
Compare with predefined threshold
    ↓
 ┌───────────────────────┐
 │                       │
Score ≥ Threshold    Score < Threshold
 │                       │
 ↓                       ↓
Send application      Store result
to HR via Gmail API    in Google Sheets
 │
 ↓
HR Recruiter
```

## 🎥 Demonstration

The demonstration shows the complete automated recruitment process, including:

* Candidate application
* CV processing
* AI-powered CV analysis
* Candidate scoring
* Threshold-based candidate selection
* Google Sheets data storage
* Automatic HR email notification

▶️ [Watch the full demonstration on YouTube](YOUR_YOUTUBE_LINK)

## 🎯 Example Use Case

A company can define a job position with specific requirements such as:

* Bachelor's degree in Computer Science
* Knowledge of HTML, CSS and JavaScript
* Relevant technical skills
* Required academic background

A minimum score can then be defined for the position.

When candidates submit their CVs:

**Candidate A**

```text
AI Score: 85/100
Required Threshold: 70/100
→ Application automatically sent to HR
```

**Candidate B**

```text
AI Score: 55/100
Required Threshold: 70/100
→ Application not forwarded automatically
→ Evaluation stored in Google Sheets
```

This demonstrates how AI can be integrated into an automated recruitment workflow to assist with initial candidate screening.

## 📊 Project Impact

The project demonstrates how **AI, LLMs, APIs and workflow automation** can be combined to automate a real-world recruitment process.

It reduces repetitive manual work during the initial CV screening stage and provides recruiters with structured candidate evaluations.

## 🔮 Future Improvements

Potential future developments include:

* 🧠 More advanced semantic CV-to-job matching
* 📊 Recruiter dashboard and analytics
* 📄 Support for additional CV formats
* 🌍 Multilingual CV analysis
* ⚖️ More configurable scoring criteria
* 🔐 Improved data privacy and security
* 🤖 AI-powered interview pre-screening
* 📈 Recruitment analytics and candidate statistics

## 👨‍💻 Author

**Mohamed Zineddine Rguez**

Computer Science Student — Institut Supérieur d'Informatique (ISI)

Interested in **Artificial Intelligence, LLMs, AI Agents and Automation**.

🔗 [LinkedIn](https://www.linkedin.com/in/mohamed-zineddine-rguez/?skipRedirect=true)
🔗 [GitHub](https://github.com/MohamedZineddineRguez)


