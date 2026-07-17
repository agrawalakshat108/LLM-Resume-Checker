# LLM Resume Checker

## Overview

LLM Resume Checker is an AI-powered resume analysis system that automates candidate screening by comparing resumes against job descriptions using a Large Language Model (LLM). The application extracts structured information from resumes, identifies relevant qualifications, and generates standardized JSON output that can be integrated into Applicant Tracking Systems (ATS) or recruitment workflows.

The project demonstrates the practical application of prompt engineering, structured output generation, schema validation, and LLM-based information extraction for recruitment automation.

---

## Features

- Automated resume parsing using a Large Language Model
- Structured extraction of candidate information
- Job description analysis
- Schema-constrained JSON generation using Pydantic
- Fast inference through the Groq API
- Robust validation of extracted information
- Easy integration with downstream HR applications

---

## Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| LLM Provider | Groq |
| Language Model | Llama 3.3 70B Versatile |
| Data Validation | Pydantic |
| Environment Management | python-dotenv |
| Data Format | JSON |
| Package Manager | uv |

---

## Project Structure

```text
LLM-Resume-Checker/
│
├── resume_parser.py
├── myproject.toml
├── uv.lock
├── README.md
├── .gitignore
└── resumes/
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/agrawalakshat108/LLM-Resume-Checker.git
cd LLM-Resume-Checker
```

### Create a virtual environment

```bash
python -m venv .venv
```

Windows

```bash
.venv\Scripts\activate
```

Linux/macOS

```bash
source .venv/bin/activate
```

### Install dependencies

Using pip

```bash
pip install -r requirements.txt
```

or

```bash
uv sync
```

---

## Configuration

Create a `.env` file in the project root.

```env
GROQ_API_KEY=YOUR_API_KEY
```

---

## Running the Application

```bash
python resume_parser.py
```

---

## Processing Pipeline

```text
Resume PDF
      │
      ▼
Text Extraction
      │
      ▼
Prompt Construction
      │
      ▼
Groq LLM
      │
      ▼
Schema Validation
      │
      ▼
Structured JSON Output
```

---

## Sample Output

```json
{
    "candidate_name": "John Doe",
    "education": [
        "B.Tech Computer Science"
    ],
    "experience": 2,
    "skills": [
        "Python",
        "SQL",
        "Machine Learning"
    ],
    "projects": [
        "Recommendation System"
    ]
}
```

---

## Use Cases

- Resume Screening
- Applicant Tracking Systems (ATS)
- Recruitment Automation
- Candidate Ranking
- Talent Acquisition
- HR Analytics

---

## Security

Sensitive files are excluded from version control through `.gitignore`.

```
.env
__pycache__/
.venv/
resumes/
```

---

## Future Enhancements

- Resume ranking based on job requirements
- ATS compatibility scoring
- Batch resume processing
- Multi-format document support
- Web interface
- PDF report generation
- Semantic similarity scoring
- Interview question generation

---

## Author

**Akshat Agrawal**

GitHub: https://github.com/agrawalakshat108

---

## License

This project is licensed under the MIT License.