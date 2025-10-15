# 🎯 Smart Resume Screener

<div align="center">

**AI-Powered Resume Screening System with Semantic Matching**

[Features](#features) • [Architecture](#architecture) • [LLM Prompts](#llm-integration) • [Installation](#installation) • [API](#api-documentation) • [Demo](#demo)

</div>

---

## 📖 Overview

**Smart Resume Screener** is an intelligent recruitment automation tool that combines PDF parsing with Large Language Model (LLM) technology to revolutionize the hiring process. It automatically extracts structured data from resumes and uses AI to provide objective, detailed candidate evaluations.


### Key Highlights

- ⚡ **90% faster** than manual screening
- 🤖 **AI-powered** semantic matching with Groq's Llama 3.3 70B
- 📊 **Objective scoring** with detailed justifications
- 🎯 **Smart extraction** of skills, experience, and education

---

## ✨ Features

- **PDF Resume Parsing** - Automatic extraction using Apache PDFBox 3.0.3
- **AI Semantic Matching** - Context-aware evaluation beyond keywords
- **Intelligent Scoring** - 1-10 scale with detailed AI justifications
- **Modern Web UI** - Responsive interface with drag-and-drop upload
- **RESTful API** - Complete backend with Spring Boot
- **Batch Processing** - Screen multiple candidates simultaneously

---





## 🛠️ Technology Stack

| Layer | Technology | Version | Purpose |
|-------|-----------|---------|---------|
| **Backend** | Java | 17 | Core language |
| | Spring Boot | 3.3.4 | Application framework |
| | Spring Data JPA | 3.3.4 | Data persistence |
| | Hibernate | 6.5.3 | ORM |
| **AI** | Spring AI | 1.0.0-M3 | LLM integration |
| | Groq API | Latest | LLM provider |
| | Llama 3.3 70B | Latest | Language model |
| **PDF** | Apache PDFBox | 3.0.3 | PDF parsing |
| **Database** | H2 | 2.x | In-memory DB |
| **Frontend** | HTML/CSS/JS | ES6 | Web interface |
| **Build** | Maven | 3.9+ | Build tool |

---

## 🚀 Installation

### Prerequisites

- ☕ Java 17+ ([Download](https://www.oracle.com/java/technologies/downloads/))
- 📦 Maven 3.6+ ([Download](https://maven.apache.org/download.cgi))
- 🔑 Groq API Key ([Free Signup](https://console.groq.com))


### Detailed Setup

**Step 1: Get Groq API Key**
1. Visit https://console.groq.com
2. Sign up (free)
3. Go to "API Keys"
4. Create new key
5. Copy key (starts with `gsk_`)

**Step 2: Configure Application**

Edit `src/main/resources/application.properties`:
spring.ai.openai.api-key=gsk_YOUR_ACTUAL_KEY_HERE
spring.ai.openai.base-url=https://api.groq.com/openai
spring.ai.openai.chat.options.model=llama-3.3-70b-versatile



**Step 3: Run Application**
mvn spring-boot:run



---

## 📖 API Documentation

### Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/upload` | Upload PDF resume |
| `POST` | `/api/match` | Match resumes with job |
| `GET` | `/api/resumes` | Get all resumes |
| `DELETE` | `/api/resumes/{id}` | Delete specific resume |
| `DELETE` | `/api/resumes` | Delete all resumes |

### Example: Upload Resume

**Request:**
curl -X POST http://localhost:8080/api/upload
-F "file=@resume.pdf"



---

## 📁 Project Structure

```
smart-resume-screener/
├── src/
│   ├── main/
│   │   ├── java/com/resumescreener/
│   │   │   ├── SmartResumeScreenerApplication.java
│   │   │   ├── controller/
│   │   │   │   └── ResumeController.java
│   │   │   ├── service/
│   │   │   │   ├── PDFParserService.java
│   │   │   │   └── LLMMatchingService.java
│   │   │   ├── model/
│   │   │   │   ├── Resume.java
│   │   │   │   └── MatchResult.java
│   │   │   └── repository/
│   │   │       └── ResumeRepository.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── templates/
│   │           └── index.html
│   └── test/
├── pom.xml
├── README.md
└── .gitignore
```




---

## 📊 Performance

- **PDF Processing**: < 2 seconds per resume
- **AI Matching**: 3-5 seconds per candidate
- **API Response**: < 500ms (excluding AI)
- **Throughput**: 30 requests/minute (Groq free tier)

---



## 🔐 Security

- ✅ API keys in properties (excluded from Git)
- ✅ Input validation (PDF only, 10MB limit)
- ✅ SQL injection prevention (JPA)
- ✅ XSS protection (Thymeleaf escaping)

---

## 🚧 Future Enhancements

- [ ] DOCX resume support
- [ ] Email notifications
- [ ] Export to Excel/CSV
- [ ] User authentication
- [ ] PostgreSQL for production
- [ ] Docker deployment

---

## 👨‍💻 Author

**Apurva Anand**
- GitHub: [@APURV960](https://github.com/APURV960)
- Email: apurva.anand789@gmail.com

---

## 🙏 Acknowledgments

- Spring AI Team - AI integration framework
- Groq - Free LLM API access
- Apache PDFBox - PDF parsing library

---


<div align="center">


</div>
