# SmartHire AI 🧐

SmartHire AI is a lightweight AI-powered tool that evaluates the compatibility between a resume and a job description using semantic similarity. It leverages a state-of-the-art NLP model from Hugging Face to compute the match score.

---

## 🌐 Live Environment

This project runs entirely in Google Colab and requires no paid services or API keys.

---

## 🚀 Features

* Computes **semantic similarity** between resume and job description
* Provides a **match score (0-100%)**
* Gives **personalized feedback** based on the score
* Uses the **MiniLM-L6-v2** transformer model for fast and accurate results

---

## 📚 Technologies Used

* Python 3
* Sentence-Transformers (Hugging Face)
* Google Colab (for execution)

---

## 📃 Example Usage

```python
from sentence_transformers import SentenceTransformer, util

model = SentenceTransformer('all-MiniLM-L6-v2')

resume = """
Experienced software engineer with a strong background in Python, data science, machine learning, and cloud technologies.
Worked on NLP-based applications using Flask and Django.
"""

job_description = """
We are hiring a Python developer with expertise in ML, NLP, Flask/Django, and AWS.
"""

embedding_resume = model.encode(resume, convert_to_tensor=True)
embedding_jd = model.encode(job_description, convert_to_tensor=True)

similarity = util.cos_sim(embedding_resume, embedding_jd).item() * 100
print(f"Match Score: {similarity:.2f}%")
```

---

## 🏆 Output Example

```
🧐 SmartHire AI - Resume Match Score: 87.23%
👌 Excellent match! Your resume is a strong fit for the job.
```

---

## 🚪 How to Run It

1. Open the Colab notebook: [SmartHire\_AI\_Colab.ipynb](https://github.com/your-username/SmartHire-AI/blob/main/SmartHire_AI_Colab.ipynb)
2. Replace the sample `resume_text` and `job_description` with your own.
3. Run all cells.
4. View your resume match score!

---

## 🚑 Ideal For

* Internship/placement preparation
* Resume tailoring
* Career guidance platforms
* Capstone/AI mini-projects

---

## 💼 Author

**Devi Bala**
B.Tech Computer Science Student
\[LinkedIn Profile] http://www.linkedin.com/in/devi-bala-1010b8300

---

## 🔧 Future Improvements

* Streamlit web UI
* File upload support (PDF parsing)
* Job recommendation engine

---

## 💌 License

MIT License - free to use and modify.

---

### ✨ SmartHire AI: Let your resume speak AI.

---

