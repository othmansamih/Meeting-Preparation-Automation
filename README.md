# Meeting Preparation Automation

## Overview

This project automates meeting preparation by utilizing a set of intelligent agents and tasks. These components work together to research meeting participants, analyze industry trends, develop strategic talking points, and create a comprehensive briefing document for successful meetings.

## Features

- **Research Specialist**: Gathers information on meeting participants and companies.
- **Industry Analyst**: Analyzes industry trends, challenges, and opportunities.
- **Meeting Strategy Advisor**: Develops strategic talking points and discussion angles.
- **Briefing Coordinator**: Compiles all insights into a concise briefing document.
- Integration with **ExaSearchToolset** for advanced web search and content retrieval.

---

## Project Structure

```bash
bash
Copy code
├── components/
│   ├── __init__.py       # Initialization for components
│   ├── agents.py         # Definition of agent roles
│   ├── tasks.py          # Task creation and configuration
│   ├── tools.py          # Tools for web search and content retrieval
├── .env                  # Environment variables
├── .gitignore            # Files and directories to ignore in git
├── main.py               # Entry point for the application
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation

```

---

## Installation

### Prerequisites

- Python 3.10 or higher
- API keys for OpenAI, Exa, and LangChain.

### Steps

1. Clone the repository:
    
    ```bash
    git clone https://github.com/yourusername/meeting-preparation-automation.git
    cd meeting-prep-automation
    ```
    
2. Install dependencies:
    
    ```bash
    pip install -r requirements.txt
    ```
    
3. Set up environment variables in `.env`:
    
    ```makefile
    OPENAI_API_KEY="your_openai_api_key"
    EXA_API_KEY="your_exa_api_key"
    OPENAI_MODEL_NAME="gpt-4o-mini"
    LANGCHAIN_TRACING_V2=true
    LANGCHAIN_API_KEY="your_langchain_api_key"
    LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
    LANGCHAIN_PROJECT="your_project_name"
    ```
    
4. Run the application:
    
    ```bash
    python main.py
    ```
    

---

## Usage

1. Start the application:
    
    ```bash
    python main.py
    ```
    
2. Follow the prompts to:
    - Enter meeting participants' emails.
    - Provide meeting context and objectives.
3. The application will:
    - Create agents and assign tasks.
    - Perform research and analysis.
    - Generate a meeting briefing document.

---

## Key Components

### Agents

Defined in `agents.py`, these agents specialize in specific roles:

- `research_agent`: Conducts participant and company research.
- `industry_analysis_agent`: Analyzes trends and challenges in the relevant industry.
- `meeting_strategy_agent`: Develops strategic angles for the meeting.
- `summary_and_briefing_agent`: Consolidates all insights into a briefing document.

### Tasks

Defined in `tasks.py`, tasks assign actionable objectives to agents:

- `research_task`: Gathers detailed participant/company information.
- `industry_analysis_task`: Provides an industry overview.
- `meeting_strategy_task`: Creates talking points and strategies.
- `summary_and_briefing_task`: Prepares the final briefing document.

### Tools

Defined in `tools.py`, `ExaSearchToolset` provides:

- Web search functionality.
- Content retrieval and similarity analysis.

---

## Dependencies

- `crewai`: Core framework for agents and tasks.
- `exa_py`: Web search and retrieval tools.

---

## Improvements

- Add more specialized agents for specific industries.
- Integrate calendar APIs for automated meeting scheduling.

---
