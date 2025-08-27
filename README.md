# LLM_Smart_Assistant
The LLM Smart Assistant is a multi-level project designed to simulate the evolution of an intelligent assistant, gradually increasing in complexity. Each level introduces new capabilities, moving from a simple chatbot to an agent capable of handling multi-step reasoning and tool usage. 

## Project Structure

LLM_Smart_Assistant/
├── README.md # Overall project documentation 
├── .env # API keys
├── Level1/
│ ├── chatbot.py 
│ ├── README.md # Level 1 instructions
│ └── logs/
│ └── level1_interaction.log
├── Level2/
│ ├── chatbot_with_tool.py 
│ ├── calculator_tool.py # Basic arithmetic tool
│ ├── README.md # Level 2 instructions
│ └── logs/
│ └── level2_interaction.log
├── Level3/
│ ├── full_agent.py 
│ ├── calculator_tool.py 
│ ├── translator_tool.py 
│ ├── README.md # Level 3 instructions
│ └── logs/
│ └── level3_interaction.log



## Levels Overview

### Level 1 — Basic Chatbot
- Uses an LLM (OpenAI/Gemini) to answer user queries.
- Input: Free text query.  
- Output: LLM-generated response.  
- **File:** `Level1/chatbot.py`  

### Level 2 — Tool-Augmented Chatbot
- Extends Level 1 by integrating a **calculator tool**.  
- Detects arithmetic tasks (e.g., “add 10 and 20”).  
- Routes such tasks to `calculator_tool.py`, else defaults to LLM.  
- **File:** `Level2/chatbot_with_tool.py`  

### Level 3 — Full Agent
- Fully agentic AI with **multi-step reasoning**.  
- Breaks complex queries into sub-tasks.  
- Can call multiple tools (`calculator_tool.py`, `translator_tool.py`).  
- Maintains simple memory across steps.  
- Example:  
  > “Translate 'Good Morning' into German and then multiply 5 and 6.”  
  - Step 1 → Translation (`Good Morning → Guten Morgen`)  
  - Step 2 → Multiplication (`5 × 6 = 30`)  
- **File:** `Level3/full_agent.py`  



## Setup & Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/gayathrikota02/LLM_Smart_Assistant.git
   cd LLM_Smart_Assistant


# LLM Smart Assistant

## Setup

### 1. Create virtual environment
```bash
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
.venv\Scripts\activate      # Windows
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add your API keys to `.env`

OPENAI_API_KEY=your_api_key_here



## Running the Project

### Run Level 1
```bash
python Level1/chatbot.py "What is the capital of France?"
```

### Run Level 2
```bash
python Level2/chatbot_with_tool.py "Add 12 and 30"
```

### Run Level 3
```bash
python Level3/full_agent.py "Translate 'Good Morning' into German and then multiply 5 and 6."
```



## 📝 Logs

Each level stores logs of all interactions inside its `logs/` folder.  


**Example:**  
Level1/logs/level1_interaction.log



## 👩‍💻 Contributor

**Gayathri**  
mail: 245122748007@mvsrec.edu.in 





