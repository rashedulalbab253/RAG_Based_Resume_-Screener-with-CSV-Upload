# 📄 RAG-Based Resume Screener with CSV Upload

This project provides an intuitive, GPT-powered resume screening tool built using Gradio. It allows HR professionals or recruiters to upload a CSV file containing candidate resumes, specify a job role and required skills, and automatically receive a list of shortlisted candidates who best match the criteria.

---

## 🚀 Features

- **CSV Upload**: Upload a CSV file containing resumes (must have a `resume` column).
- **AI Screening**: Uses OpenAI's GPT model to evaluate each resume based on the job role and must-have skills you specify.
- **Shortlisting**: Returns only the candidates who are a good match, along with a short explanation.
- **No Coding Needed**: Simple Gradio web interface—no need to write code to use it!

---

## 🛠️ Installation & Setup

1. **Clone the Repository**  
   ```
   git clone <repo-url>
   cd <repo-directory>
   ```

2. **Install Required Packages**  
   The following Python packages are required:
   - openai==0.28.0
   - gradio
   - pandas
   - PyPDF2

   You can install them with:
   ```bash
   pip install openai==0.28.0 gradio pandas PyPDF2
   ```

3. **Set OpenAI API Key**  
   Edit the notebook and set your OpenAI API key:
   ```python
   openai.api_key = "YOUR_OPENAI_API_KEY"
   ```

4. **Run the Notebook**  
   Open `RAG_Based_Resume__Screener_with_CSV_Upload.ipynb` in Jupyter or Google Colab and run all cells.

---

## 📥 Usage

1. **Prepare Your CSV File**
   - Your CSV must have a column named `resume` with the full text of each candidate's resume.
   - Example:
     | name         | resume                        |
     |--------------|------------------------------|
     | Alice Smith  | Experienced data scientist...|
     | Bob Johnson  | Sales leader with 10+ years...|

2. **Launch the App**
   - The Gradio interface will appear with three inputs:
     - **Upload CSV with 'resume' Column**: Select your CSV file.
     - **Job Role**: Enter the role (e.g., "Data Scientist").
     - **Must-Have Skills**: List required skills, comma-separated (e.g., "Python, Machine Learning, SQL").

3. **View Results**
   - The tool will return a list of candidates marked as "MATCH" by the AI, including reasons and resume snippets.

---

## ⚙️ How it Works

- For each resume, the app sends a prompt to GPT-3.5-turbo asking whether the candidate is a match for the given role and skills.
- The AI replies with "MATCH" or "NO MATCH" and a short explanation.
- Only candidates with "MATCH" in the response are shown.

---

## 💡 Example Prompt to GPT

> "You are a smart HR assistant. Based on the job role 'Data Scientist' and these required skills: Python, Machine Learning, SQL, decide if this resume is a good match.

> Resume: [resume text here]

> Reply with 'MATCH' or 'NO MATCH' and a short reason why."

---

## 📝 Notes

- **Privacy**: This tool processes sensitive resume data. Ensure compliance with relevant data privacy regulations.
- **API Costs**: Each resume is evaluated via the OpenAI API, which may incur costs depending on your API usage.

---

## 📚 Dependencies

- [OpenAI Python SDK](https://pypi.org/project/openai/)
- [Gradio](https://gradio.app/)
- [Pandas](https://pandas.pydata.org/)
- [PyPDF2](https://pypi.org/project/PyPDF2/)

---



```
