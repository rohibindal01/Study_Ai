# 🎓 Study Buddy AI

An interactive AI-powered quiz generation platform built using **Streamlit**, designed to help users generate, attempt, and evaluate quizzes dynamically based on selected topics, difficulty levels, and question types.

---

## 📌 1. Basic Flow of the Project

1. The application starts from `application.py`.
2. Environment variables are loaded using `.env`.
3. Streamlit initializes the web interface and session state variables.
4. User selects quiz preferences:
   - Question Type (MCQ / Fill in the Blank)
   - Topic
   - Difficulty Level
   - Number of Questions
5. On clicking **"Generate Quiz"**:
   - A `QuestionGenerator` object is created.
   - Questions are generated and stored using `QuizManager`.
6. The quiz is displayed to the user:
   - User attempts all questions interactively.
7. On clicking **"Submit Quiz"**:
   - Answers are evaluated.
   - Results are generated and displayed.
8. User can:
   - View score and correctness
   - Download results as a CSV file

---

## 🛠️ 2. Technologies Used

### 🔹 Frontend
- Streamlit – Interactive UI and state management

### 🔹 Backend Logic
- Python – Core programming language
- Custom modules:
  - `QuestionGenerator` – Generates quiz questions
  - `QuizManager` – Manages quiz lifecycle (generation, evaluation, results)

### 🔹 Utilities
- python-dotenv – Environment variable handling
- pandas (likely used in result generation)
- os – File handling

---

## 🏗️ 3. Flow Architecture
        ┌────────────────────┐
        │   application.py   │
        │ (Streamlit App)    │
        └─────────┬──────────┘
                  │
                  ▼
     ┌──────────────────────────┐
     │ User Inputs (Sidebar)    │
     │ Topic, Difficulty, Type  │
     └─────────┬────────────────┘
               │
               ▼
    ┌───────────────────────────┐
    │ QuestionGenerator         │
    │ (Generate Questions)      │
    └─────────┬─────────────────┘
              │
              ▼
    ┌───────────────────────────┐
    │ QuizManager               │
    │ (Store + Manage Quiz)     │
    └─────────┬─────────────────┘
              │
              ▼
    ┌───────────────────────────┐
    │ User Attempts Quiz        │
    └─────────┬─────────────────┘
              │
              ▼
    ┌───────────────────────────┐
    │ Evaluate Answers          │
    └─────────┬─────────────────┘
              │
              ▼
    ┌───────────────────────────┐
    │ Results + Score Display   │
    └─────────┬─────────────────┘
              │
              ▼
    ┌───────────────────────────┐
    │ Save & Download CSV       │
    └───────────────────────────┘

---

## 📖 4. Information About the Project

**Study Buddy AI** is an intelligent quiz-based learning tool that allows users to:

- Generate quizzes dynamically based on any topic
- Choose difficulty levels and question formats
- Attempt quizzes interactively
- Get instant feedback and scoring
- Download results for further analysis

### ✨ Key Features

- ✅ Dynamic quiz generation using AI-based logic  
- ✅ Multiple question formats (MCQ & Fill in the Blank)  
- ✅ Real-time evaluation and feedback  
- ✅ Session-based state management  
- ✅ CSV export functionality for results  
- ✅ Clean and interactive UI using Streamlit  

### ⚙️ How It Works

- The app uses **Streamlit session state** to persist quiz data.
- `QuestionGenerator` creates questions dynamically.
- `QuizManager` handles:
  - Question storage
  - User responses
  - Evaluation logic
  - Result formatting
- Results are displayed with:
  - Correct/incorrect indicators
  - User vs correct answers
- Users can download their performance as a CSV file.

---

## ▶️ How to Run the Project

```bash
# Install dependencies
pip install -r requirements.txt

# Run the Streamlit app
streamlit run application.py
