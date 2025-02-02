# 🚀 GenieBrain-AI 🧞‍♂️✨  
**Your AI-powered knowledge genie, summarizing text and answering questions effortlessly!**  

## 📝 Overview  
GenieBrain-AI is an **AI-driven assistant** that can:  
✔️ Summarize text quickly and efficiently 📜  
✔️ Answer questions using LLM-powered reasoning ❓🤖  
✔️ Extract key insights from any content 🔍✨  
✔️ Provide structured, easy-to-understand summaries ✅  

---

## 🏗️ Installation  

### 1️⃣ Create a Virtual Environment  
```sh
python -m venv myenv

```
**2️⃣ Activate the Virtual Environment**
On Windows
```sh
myenv\Scripts\activate
```
On macOS/Linux
```sh
source myenv/bin/activate

```
**3️⃣ Install Required Libraries**
```sh
pip install streamlit  
pip install google-generativeai
```
### 🔑 Setting Up API Key
✅ Option 1: Save API Key in config.json (Recommended for Custom Use)

1️⃣ 
Create a config.json file in the project directory with the following structure:

```json
{
  "GEMINI_API_KEY": "your_api_key_here"
}
```
## ✅ Option 2: Permanent API Key Setup (Optional)
1️⃣ Go to System Settings → Environment Variables
2️⃣ Create a new Environment Variable

Variable Name: GEMINI_API_KEY
Variable Value: Paste your API key here
3️⃣ Click OK and restart your terminal
---

###🚀 Running the Program
🔹 Start the Streamlit App
Run the following command in the terminal:
