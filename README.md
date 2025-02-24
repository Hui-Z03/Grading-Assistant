# Grading-Assistant
a web-based application that grading students' assignments and essays
## Overview
AI Grading Assistant is a web-based application that acts as a university professor, automatically grading students' assignments and essays in business-related subjects. The system utilizes **Flask** for the backend, **HTML/CSS/JavaScript** for the frontend, and **Azure OpenAI's language model** to analyze and evaluate the submissions.

## Features
- **Automated Grading**: AI analyzes assignments and provides scores based on predefined criteria.
- **Feedback Generation**: AI gives detailed comments on logic, argument support, structure, and language clarity.
- **File Upload Support**: Allows students to submit assignments via text input or file upload.
- **Customizable Grading Criteria**: Teachers can adjust scoring weights and standards.
- **History Tracking**: Stores previous assignments and grades for reference.

## Tech Stack
- **Frontend**: HTML, CSS, JavaScript (Optional: React.js)
- **Backend**: Python, Flask
- **AI Model**: Azure OpenAI (GPT-4)
- **Database**: SQLite / PostgreSQL (Optional)
- **Cloud Deployment**: Azure App Services / Azure Functions (Optional)

## Installation
### Prerequisites
- Python 3.x
- Virtual environment (optional but recommended)
- Azure OpenAI API Key

### Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/ai-grading-assistant.git
   cd ai-grading-assistant
   ```
2. Create a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   ```sh
   export OPENAI_API_KEY="your-azure-api-key"
   ```
   Or create a `.env` file:
   ```
   OPENAI_API_KEY=your-azure-api-key
   ```
5. Run the Flask server:
   ```sh
   flask run
   ```
6. Open `http://127.0.0.1:5000` in your browser.

## API Endpoints
### 1. Submit Assignment
- **Endpoint**: `POST /grade`
- **Request Body**:
  ```json
  {
    "student_id": "12345",
    "assignment_text": "This is the essay content."
  }
  ```
- **Response**:
  ```json
  {
    "score": 85,
    "feedback": "Your argument is strong, but the conclusion needs improvement."
  }
  ```

## Future Enhancements
- Implement **plagiarism detection**
- Support **PDF/Word document uploads**
- Add **teacher review and adjustments**
- Deploy to **Azure Cloud**
