# GenAI App - AI Code Reviewer

This is a Streamlit web application that uses Google Generative AI (Gemini-Pro) to review Python code, identify issues, and suggest improvements.

## Features
- Accepts Python code input via a text area.  
- Provides detailed code reviews with suggestions and corrected snippets.  
- Displays warnings and error handling with retries for API requests.  

## Prerequisites
- Python installed on your system.  
- A valid Google Generative AI API Key.  

## Installation

1. **Clone the repository:**  
   ```bash
   git clone https://github.com/yourusername/genai-code-reviewer.git
   cd genai-code-reviewer
   ```

2. **Install dependencies:**  
   Ensure you have `pip` installed, then run:  
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up secrets:**  
   Create a `secrets.toml` file in the `.streamlit` directory with your Google API key:  
   ```toml
   GOOGLE_API_KEY = "your-api-key-here"
   ```

## Usage

1. **Run the application:**  
   ```bash
   streamlit run app.py
   ```

2. **Enter your Python code** in the provided text area.  
3. **Click "Review Code"** to receive feedback on bugs and suggestions.  

## Requirements

The following packages are necessary to run the app:  
- `streamlit`  
- `google-generativeai`  

*(Dependencies are listed in `requirements.txt`)*  

## File Structure
```
📂 project-folder/
   ├── app.py               # Main Streamlit application
   ├── requirements.txt     # Python dependencies
   └── secrets.toml         # Google API Key (add in .streamlit/ folder)
```

## Notes
- The app uses exponential backoff to handle API errors gracefully.  
- API Key should be kept secure and not shared publicly.  
