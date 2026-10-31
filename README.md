# 🔬 Multi-Agent Research Assistant

An AI-powered research assistant built with **LangChain, LCEL, and LLMs** that automates web research, website scraping, information extraction, and critical review using a two-agent architecture.

The system takes a research topic from the user, gathers relevant information from online sources, and generates a structured research report with an independent critical analysis.

## 🚀 Project Overview

The project consists of two specialized AI agents:

### 1. Research Agent
Responsible for gathering relevant information about the given research topic.

**Responsibilities:**
- Search the web using Tavily Search.
- Discover relevant websites and articles.
- Scrape website content using BeautifulSoup and Requests.
- Extract meaningful information from collected content.
- Organize research findings with source URLs.

### 2. Critic & Review Agent
Responsible for evaluating and critically analyzing the research collected by the Research Agent.

**Responsibilities:**
- Analyze the collected research.
- Identify strengths and weaknesses.
- Detect contradictions and missing information.
- Evaluate the relevance and reliability of sources.
- Generate an independent critical review.
- Provide suggestions for improving the research.

## 🔄 System Workflow

```text
          User Input
               |
               v
       Research Topic
               |
               v
      +------------------+
      |  Research Agent  |
      +------------------+
               |
         Tavily Search
               |
         Web Scraping
               |
      Information Extraction
               |
               v
      Research Findings
               |
               v
      +------------------+
      | Critic & Review  |
      |      Agent       |
      +------------------+
               |
       Critical Analysis
               |
       Quality Evaluation
               |
               v
        Final Research
             Report
               |
               v
       Markdown Output
```

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | Agent and LLM integration |
| LCEL | Chain composition and execution |
| ChatGroq | Large Language Model |
| Tavily Search | Web research |
| BeautifulSoup | Website scraping |
| Requests | HTTP requests |
| Pydantic | Structured data validation |
| Python-dotenv | Environment configuration |

## 📂 Project Structure

```text
research_assistant/
│
├── src/
│   ├── agents/
│   │   ├── research_agent.py
│   │   └── critic_agent.py
│   │
│   ├── tools/
│   │   ├── search_tool.py
│   │   └── scraper_tool.py
│   │
│   ├── chains/
│   │   ├── research_chain.py
│   │   └── review_chain.py
│   │
│   ├── prompts/
│   │   ├── research_prompt.py
│   │   └── critic_prompt.py
│   │
│   ├── config/
│   │   └── settings.py
│   │
│   └── main.py
│
├── outputs/
├── .env
├── .gitignore
├── requirements.txt
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd research_assistant
```

### 2. Create Virtual Environment

```bash
python -m venv venv
```

Activate on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

### 5. Run the Application

```bash
python