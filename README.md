#  TCS Capstone Project on Back Office Document Classification and Routing Agent

An AI-powered document classification and routing application built using Python, Streamlit, and Groq LLM.

This project automates the initial handling of back-office business documents by analyzing their content, identifying document types, estimating classification confidence, and recommending the appropriate department using rule-based routing logic.

##  Project Overview

Organizations receive different types of business documents every day, including invoices, purchase orders, contracts, receipts, and employee-related documents.

Manually reviewing and assigning these documents to the correct departments can be time-consuming.

The Back Office Document Classification and Routing Agent simplifies this process using Large Language Model (LLM) capabilities combined with Python-based routing rules.

##  Features

- **Document Upload:** Upload PDF, DOCX, and TXT documents.
- **Text Extraction:** Extract readable content from uploaded documents.
- **AI-Powered Classification:** Use Groq LLM to identify the document type.
- **Confidence Score:** Generate an AI-estimated confidence percentage for classification.
- **Automated Routing Logic:** Apply Python-based rules to recommend the appropriate department.
- **Classification Explanation:** Display a brief explanation for the classification.
- **800-Word Input Limit:** Limit the extracted document content sent to the AI to 800 words.

##  How It Works

1. **Upload Document:** The user uploads a business document.
2. **Text Extraction:** The application extracts text from the uploaded file.
3. **Input Processing:** The extracted text is limited to 800 words.
4. **AI Classification:** The Groq LLM analyzes the document and identifies its type.
5. **Confidence Estimation:** The AI provides an estimated confidence percentage.
6. **Department Routing:** Python routing rules determine the recommended department.
7. **Result Display:** The application presents classification and routing recommendations.

##  Document Routing Rules

| Document Type                | Recommended Department       |
|------------------------------|------------------------------|
| Invoice                      | Finance Department           |
| Receipt                      | Finance Department           |
| Purchase Order               | Procurement Department       |
| Contract                     | Legal Department             |
| Agreement                    | Legal Department             |
| Employee / HR Document       | HR Department                |
| Customer-related Document    | Customer Support Department  |
| Other Documents              | General Administration       |

##  Technology Stack

| Technology          | Purpose                                 |
|---------------------|-----------------------------------------|
| Python              | Core application and routing logic      |
| Streamlit           | User interface                          |
| Groq API            | LLM-powered document classification     |
| GPT-OSS-20B         | AI model used for classification        |
| PyPDF               | PDF text extraction                     |
| python-docx         | DOCX text extraction                    |
| python-dotenv       | Environment variable management         |
| uv                  | Python dependency and project management|

## 📂 Project Structure


document-classification-agent/
│
├── app.py                  # Main Streamlit application
├── pyproject.toml          # Project dependencies and configuration
├── uv.lock                 # Dependency lockfile 
├── .env                    # API key (not uploaded to GitHub)
├── .gitignore              # Files excluded from Git
├── README.md               # Project documentation
│
├── files/                  # Sample business documents
│   ├── invoices/
│   ├── purchase_orders/
│   ├── contracts/
│   └── other/
│
└── .venv/                  # Virtual environment (not uploaded)


##  Installation and Setup

### Prerequisites

- Python 3.10 or later
- Git
- uv
- A Groq API key

### 1. Clone the Repository


git clone https://github.com/YOUR-USERNAME/back-office-document-classification-agent.git


### 2. Navigate to the Project Directory

```bash
cd back-office-document-classification-agent
```

### 3. Install Dependencies

```bash
uv sync
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and add your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Get your API key from [Groq Console](https://console.groq.com/keys).

**Important:** Never commit or share your `.env` file or API key.

### 5. Run the Application

```bash
uv run streamlit run app.py
```

Open the local URL displayed in your terminal, usually:

```text
http://localhost:8501
```

##  Expected Output

For an uploaded invoice, the application produces results similar to:

```text
Document Type: Invoice

Confidence: 96%

Reason:
The document contains billing and payment information.

Recommended Department:
Finance Department

Routing Decision:
Route to Finance Department
```

*The confidence value above is illustrative; actual results depend on the uploaded document and model response.*

##  Project Objectives

- Apply LLM capabilities to business document classification.
- Automate department recommendation through rule-based routing.
- Reduce manual effort in initial document processing.
- Demonstrate the integration of AI and traditional Python programming.

##  Future Enhancements

- Structured classification results using JSON.
- Classification history and document tracking.
- Support for additional document categories.
- Actual document delivery through email or department systems.
- Improved confidence validation and classification evaluation.
- More advanced document search and retrieval capabilities.

##  Author

**Sayan Halder**

Computer Science | AI Enthusiast | Aspiring Software Engineer

Interested in Artificial Intelligence, Generative AI, RAG Systems, and Software Development.

------------------------------------------------------------------------------------------------

⭐ If you find this project interesting, consider giving the repository a star!

