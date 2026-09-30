# ⚖️ LegalEase – AI-Powered Legal Assistant

**LegalEase** is an AI-powered legal assistance platform developed as a student project to demonstrate how **Generative AI, FastAPI, React.js, and Google Gemini API** can be integrated to provide accessible legal information and document-generation assistance.

> ⚠️ **Disclaimer:** LegalEase is an educational project. AI-generated responses are for informational purposes only and should not be considered professional legal advice. For specific legal matters, consult a qualified legal professional.

---

## 📌 Project Overview

LegalEase provides a simple web-based interface where users can enter legal-related requirements and receive AI-generated assistance.

The application is designed to demonstrate:

* 🤖 Generative AI integration
* ⚖️ Basic legal information assistance
* 📝 AI-assisted legal document generation
* 🌐 Full-stack web application development
* 🔗 REST API integration
* 🔐 Basic API security practices

---

## ✨ Key Features

| Feature                   | Description                                              |
| ------------------------- | -------------------------------------------------------- |
| 🤖 AI Legal Assistant     | Provides AI-generated responses to legal-related queries |
| 💬 Legal Query Assistance | Users can enter questions and requirements               |
| 📝 Document Generation    | Generates structured legal document content              |
| 🧠 Gemini AI              | Uses Google Gemini Generative AI                         |
| ⚡ FastAPI Backend         | Provides fast REST API services                          |
| 🌐 Web Interface          | User-friendly frontend interface                         |
| 📱 Responsive UI          | Designed for desktop and mobile-friendly usage           |
| 🔐 Environment Security   | API credentials are stored using environment variables   |

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │        User         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   LegalEase Web UI  │
                    │     React.js        │
                    └──────────┬──────────┘
                               │
                         REST API Request
                               │
                               ▼
                    ┌─────────────────────┐
                    │    FastAPI Server   │
                    │      Python         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Gemini AI API     │
                    │  Generative AI      │
                    └──────────┬──────────┘
                               │
                         AI Response
                               │
                               ▼
                    ┌─────────────────────┐
                    │    FastAPI Server   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   LegalEase UI      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │        User         │
                    └─────────────────────┘
```

---

# 🛠️ Technologies Used

## Frontend

* HTML5
* CSS3
* JavaScript
* React.js
* Vite

## Backend

* Python
* FastAPI
* Uvicorn
* Pydantic

## Artificial Intelligence

* Google Gemini API
* Generative AI

## Development Tools

* Visual Studio Code
* Git
* GitHub
* Python Virtual Environment
* npm

---

# 📂 Project Structure

```text
LegalEase/
│
├── backend/
│   ├── __init__.py
│   ├── main.py
│   ├── routes.py
│   ├── models.py
│   │
│   ├── services/
│   │   ├── __init__.py
│   │   └── gemini_service.py
│   │
│   └── requirements.txt
│
├── frontend/
│   ├── public/
│   │
│   ├── src/
│   │   ├── components/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── package.json
│   └── vite.config.js
│
├── .env.example
├── .gitignore
├── README.md
└── requirements.txt
```

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/LegalEase.git
```

## 2. Open the Project

```powershell
cd LegalEase
```

---

# 🐍 Backend Setup

## 3. Create Python Virtual Environment

```powershell
python -m venv .venv
```

## 4. Activate Virtual Environment

For Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks script execution:

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Then activate the environment:

```powershell
.\.venv\Scripts\Activate.ps1
```

After successful activation, the terminal should look similar to:

```text
(.venv) PS C:\Users\...\LegalEase>
```

---

## 5. Install Backend Dependencies

From the project root:

```powershell
pip install -r backend\requirements.txt
```

---

# 🔑 Gemini API Configuration

Create a `.env` file inside the project root:

```env
GEMINI_API_KEY=your_api_key_here
```

Example:

```text
LegalEase/
│
├── .env
├── backend/
├── frontend/
└── README.md
```

### 🔒 Important

Never upload your actual API key to GitHub.

Your `.gitignore` should contain:

```gitignore
.env
.venv/
__pycache__/
*.pyc
node_modules/
dist/
```

You can provide a template through:

```text
.env.example
```

Example:

```env
GEMINI_API_KEY=your_api_key_here
```

---

# ▶️ Run the Backend

From the **LegalEase project root**:

```powershell
uvicorn backend.main:app --reload --port 8000
```

A successful server should display something similar to:

```text
Uvicorn running on http://127.0.0.1:8000
```

Open the backend:

```text
http://127.0.0.1:8000
```

Swagger API documentation:

```text
http://127.0.0.1:8000/docs
```

Alternative ReDoc documentation:

```text
http://127.0.0.1:8000/redoc
```

---

# 💻 Frontend Setup

Open a **new VS Code terminal**.

Go to the frontend:

```powershell
cd frontend
```

Install npm dependencies:

```powershell
npm install
```

Start the development server:

```powershell
npm run dev
```

Vite will display a URL similar to:

```text
http://localhost:5173
```

Open that URL in your browser.

---

# 🔄 Running the Complete Application

You need **two terminals**.

### Terminal 1 – Backend

```powershell
cd C:\Users\acer\Desktop\LegalEase
.\.venv\Scripts\Activate.ps1
uvicorn backend.main:app --reload --port 8000
```

### Terminal 2 – Frontend

```powershell
cd C:\Users\acer\Desktop\LegalEase\frontend
npm run dev
```

Then open:

```text
http://localhost:5173
```

---

# 🔗 Application Workflow

```text
User enters legal requirement
            │
            ▼
      React Frontend
            │
            ▼
       FastAPI API
            │
            ▼
       Gemini AI API
            │
            ▼
    AI-generated response
            │
            ▼
       FastAPI API
            │
            ▼
      React Frontend
            │
            ▼
          User
```

---

# 🧩 Main Functionalities

## 1. 💬 Legal Query Assistance

Users can enter a legal-related question or requirement.

The application sends the request to the backend, which processes it using Gemini AI.

---

## 2. 📝 Legal Document Generation

Users can provide relevant information and requirements.

LegalEase generates structured document content using Generative AI.

---

## 3. 🤖 AI-Powered Assistance

The Gemini API processes user requests and generates responses based on the supplied information.

---

## 4. 📄 Document Output

The generated content can be displayed in the application and prepared for further use.

---

# 🧪 API Testing

Start the backend:

```powershell
uvicorn backend.main:app --reload --port 8000
```

Open:

```text
http://127.0.0.1:8000/docs
```

The Swagger interface can be used to:

* View API endpoints
* Enter request data
* Send API requests
* View responses
* Test backend functionality

---

# 🔐 Security

LegalEase follows basic security practices:

* 🔑 API keys are stored in `.env`
* 🚫 `.env` is excluded from Git
* 🔒 Sensitive credentials should never be committed
* ✅ User input should be validated
* 🌐 CORS should be configured appropriately
* 🛡️ Production deployments should use proper authentication and HTTPS

---

# 👥 Team – Group 7

| No. | Team Member         | Role        |
| --: | ------------------- | ----------- |
|   1 | **Nikkath Khatoon** | Team Leader |
|   2 | **Arfana Begum K**  | Team Member |
|   3 | **Snehan**          | Team Member |
|   4 | **Joel**            | Team Member |
|   5 | **Nowfel**          | Team Member |

---

# 🎓 Project Purpose

LegalEase was developed as a **student project** to demonstrate the practical application of Generative AI in the legal-assistance domain.

The project demonstrates knowledge of:

* Artificial Intelligence
* Generative AI
* Google Gemini API
* REST APIs
* FastAPI
* React.js
* Frontend Development
* Backend Development
* API Integration
* Document Generation
* Git & GitHub

---

# ⚠️ Disclaimer

LegalEase is an **educational and informational project**.

The application generates AI-assisted information and document content. It does **not** establish an attorney-client relationship and should not be treated as professional legal advice.

For legal matters that require professional interpretation or representation, users should consult a qualified legal professional.

---

# 🚀 Future Enhancements

Planned improvements may include:

* 🌍 Multi-language legal assistance
* 📄 PDF document generation
* 🔐 User authentication
* 👤 User profiles
* 💾 Document history
* 🎙️ Voice-based legal queries
* 📱 Mobile application
* ⚖️ More legal document templates
* 🗃️ Legal information database
* 👨‍⚖️ Lawyer consultation integration
* 🔎 Improved legal information retrieval
* ☁️ Cloud deployment
* 📊 Admin dashboard

---

# 📈 Future Architecture

```text
                    LegalEase
                       │
       ┌───────────────┼────────────────┐
       │               │                │
       ▼               ▼                ▼
   React Web       FastAPI          Gemini AI
   Application      Backend          Service
       │               │                │
       └───────────────┼────────────────┘
                       │
              ┌────────▼────────┐
              │ Legal Knowledge  │
              │    Database     │
              └────────┬────────┘
                       │
                       ▼
                Document Storage
```

---

# 📜 License

This project is developed for **educational purposes**.

The project may be modified and improved according to academic and development requirements.

---

# ⭐ Support

If you find **LegalEase** useful, consider giving the repository a ⭐ on GitHub.

---

## ⚖️ LegalEase

**Making Legal Assistance Smarter with AI.**

> Built with ❤️ by **Group 7**
