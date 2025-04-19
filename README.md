
# 🧠 LLM-Powered Research Assistant

This is an intelligent research assistant built using [LangChain](https://www.langchain.com/), [Gemini](https://deepmind.google/discover/blog/google-gemini-ai/), and a set of custom tools. It automates the process of gathering information from the web, organizing it into a structured format, and saving it for later use.

---

## 🚀 Features

- 🔍 **Web & Wikipedia Search:** Uses DuckDuckGo and Wikipedia to gather relevant content.
- 🤖 **LLM Integration:** Powered by Google's Gemini via `langchain-google-genai`.
- 📦 **Structured Output:** Organizes results using a custom `Pydantic` model.
- 💾 **Auto Save:** Optionally saves research output to a `.txt` file.
- 🧠 **Tool-Calling Agent:** Employs LangChain's `create_tool_calling_agent` for smart task routing.

---

## 📁 File Structure

- `main.py`: Main script that runs the agent, parses responses, and handles input/output.
- `tools.py`: Contains three custom tools:
  - `search_tool`: Searches the web using DuckDuckGo.
  - `wiki_tool`: Queries Wikipedia using `langchain_community`.
  - `save_tool`: Saves structured results to a file with a timestamp.

---

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/nekytasnim/AI-Agent-Tutorial.git
cd AI-Agent-Tutorial
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

(You’ll need packages like `langchain`, `langchain-community`, `langchain-google-genai`, `python-dotenv`, and `pydantic`.)

### 3. Add Your API Key

Create a `.env` file in the root directory and add your Gemini API key:

```
GOOGLE_API_KEY=your_key_here
```

---

## 🧪 How to Use

Simply run the script:

```bash
python main.py
```

The agent will prompt you for a research query, gather relevant data, and display a structured response. You can choose to save this output to a `.txt` file for future reference.

---

## 📄 Output Format

The final output is parsed into the following fields:

- `topic`: The subject of the research
- `summary`: Condensed research result
- `sources`: Links or citations used
- `tools_used`: Which tools were involved in the process

---

## 💡 Example Use Case

```bash
What can I help you research? 
> Latest advancements in quantum computing
```

The assistant searches the web, queries Wikipedia, summarizes findings, and returns a structured output.

---

## 🧰 Built With

- 🧠 [LangChain](https://www.langchain.com/)
- 💬 [Gemini (Google Generative AI)](https://deepmind.google/discover/blog/google-gemini-ai/)
- 🔧 [Pydantic](https://docs.pydantic.dev/)
- 🌐 [DuckDuckGo](https://duckduckgo.com/) and [Wikipedia](https://www.wikipedia.org/)

---

## 📝 License

MIT License

---

## ✨ Author

**Neky Tasnim Bhuiyan**  
📧 tasnimneky@gmail.com  
🔗 [GitHub](https://github.com/nekytasnim)
