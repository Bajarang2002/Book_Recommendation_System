# 📚 Book Recommendation System

A Machine Learning powered Book Recommendation Web Application built using Flask.  
The system recommends similar books based on collaborative filtering and precomputed similarity scores.

---

## 🚀 Project Overview

This project uses a similarity matrix to recommend books similar to the one selected by the user.

The application:

- Displays popular books on the homepage
- Allows users to enter a book name
- Recommends top 5 similar books
- Displays book title, author, and cover image

---

## 🚀 Live Demo

https://book-recommendation-system-2-xvwp.onrender.com/


## 🛠️ Tech Stack

- Python
- Flask
- NumPy
- Pickle
- HTML / CSS
- Gunicorn (for deployment)

---

## 📂 Project Structure

```
Book-Recommendation-System/
│
├── app.py
├── popular.pkl
├── books.pkl
├── pt.pkl
├── similarity_scores.pkl
├── requirements.txt
│
├── templates/
│   ├── index.html
│   └── recommend.html
│
└── static/
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone <your-repository-url>
cd Book-Recommendation-System
```

### 2️⃣ Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If you don’t have `requirements.txt`, install manually:

```bash
pip install flask numpy gunicorn
```

---

## ▶️ Run the Application Locally

```bash
python app.py
```

Then open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## 🌐 Deployment on Render

### Start Command:

```bash
gunicorn app:app --bind 0.0.0.0:$PORT
```

Make sure `gunicorn` is included in your `requirements.txt`.

---

## 🔍 Application Routes

| Route | Method | Description |
|-------|--------|------------|
| `/` | GET | Displays popular books |
| `/recommend` | GET | Recommendation input page |
| `/recommend_books` | POST | Returns recommended books |

---

## 🧠 How Recommendation Works

1. Load preprocessed data files:
   - `popular.pkl`
   - `books.pkl`
   - `pt.pkl`
   - `similarity_scores.pkl`

2. When a user enters a book name:
   - Find its index in the pivot table
   - Retrieve similarity scores
   - Sort books by similarity
   - Return top 5 similar books

The similarity matrix is precomputed for fast response time.

---

## ✨ Features

- Displays trending/popular books  
- Recommends top 5 similar books  
- Shows book title, author & cover image  
- Fast recommendations using similarity matrix  
- Simple and clean UI  
- Deployable on Render  

---

## 🔮 Future Improvements

- Add search autocomplete
- Add user authentication
- Add rating & review system
- Store data in a database (MySQL/PostgreSQL)
- Improve UI using Bootstrap or Tailwind
- Add Docker support

---

## 👨‍💻 Author

Developed as a Machine Learning + Flask Web Project.

---

## 📜 License

This project is for educational purposes only.
