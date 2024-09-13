# Open Source Recruitment Website

This is an open-source recruitment website designed to match resumes with job descriptions using Large Language Models (LLMs) like GPT or Gemini. The system automates the classification and analysis of resumes and job requirements to assist with candidate-job matching.

## Features

- **Job Listing Management**: Allows users to post and manage job listings.
- **Resume Submission**: Candidates can submit their resumes for analysis.
- **LLM-Powered Analysis**: Uses GPT to analyze and match resumes to job descriptions.
- **User Authentication** (optional): Secure user registration and login for both employers and candidates.
  
## Tech Stack

- **Backend**: Python (Flask)
- **Frontend**: HTML, CSS, JavaScript
- **LLM Integration**: GPT-3.5 (via OpenAI API)
- **Database**: SQLite (development) or PostgreSQL/MySQL (production)
- **Hosting**: Local/Cloud (Heroku, AWS, etc.)
  
## Getting Started

### Prerequisites

Before setting up the project, ensure you have the following installed:

- Python 3.8+
- Git
- Visual Studio Code (or any code editor)
- OpenAI API key (for GPT integration)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/recruitment-website.git
   cd recruitment-website
   ```

2. **Set up a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Linux/macOS
   venv\Scripts\activate  # For Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your OpenAI API key:**
   - Get an API key from OpenAI by signing up at [OpenAI](https://beta.openai.com/signup/).
   - Create a `.env` file in the project root and add your key:
     ```bash
     OPENAI_API_KEY=your-openai-api-key
     ```

### Running the Application

1. **Run the Flask server locally:**
   ```bash
   flask run
   ```

2. Open your browser and go to `http://127.0.0.1:5000/` to access the recruitment website.

### LLM API Integration

The application uses OpenAI's GPT-3.5 for resume and job description analysis. You can modify the prompt used for classification in the `app.py` file.

```python
response = openai.Completion.create(
    engine="gpt-3.5-turbo",
    prompt=f"Analyze this resume: {resume_text} and match with job description: {job_description}",
    max_tokens=150
)
```

### Frontend Integration

The front end includes a simple form for users to paste resumes and job descriptions. It submits this data to the backend for LLM-powered analysis.

You can customize the frontend in the `templates/` directory, where HTML and JavaScript files are located.

### Deployment

You can deploy the website using platforms like Heroku, AWS, or any cloud provider.

For **Heroku** deployment:

1. Install the Heroku CLI and log in:
   ```bash
   heroku login
   ```

2. Create a Heroku app:
   ```bash
   heroku create
   ```

3. Deploy to Heroku:
   ```bash
   git push heroku main
   ```

4. Open the app:
   ```bash
   heroku open
   ```

### Contributing

We welcome contributions! Here’s how you can help:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-branch
   ```
5. Submit a pull request.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

