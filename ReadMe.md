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

```json
{
  "GEMINI_API_KEY": "your_api_key_here"
}
```

### CODE
```bash
import json
import streamlit as st
import google.generativeai as genai
import os

# Load the API key from the config file
def load_api_key():
    try:
        with open('config.json', 'r') as f:
            config = json.load(f)
        return config.get("GEMINI_API_KEY")
    except Exception as e:
        st.error(f"Error loading API key: {e}")
        return None

# Retrieve the API key
api_key = load_api_key()

# Check if the API key is present
if not api_key:
    st.error("API key not found in the config file.")
    st.stop()

# Configure the Gemini API
genai.configure(api_key=api_key)

# Initialize the model
model = genai.GenerativeModel("gemini-1.5-flash")

# Function to summarize text
def summarize_text(text):
    try:
        response = model.generate_content(f"Summarize this text: {text}")
        return response.text if response and hasattr(response, "text") else "No summary generated."
    except Exception as e:
        return f"Error: {e}"

# Streamlit UI
st.title("ThinkGenie - Summarizer")
user_input = st.text_area("Enter text to summarize")

if st.button("Magic ⚡"):
    if user_input.strip():
        summary = summarize_text(user_input)
        st.subheader("Summary")
        st.write(summary)
    else:
        st.warning("Please enter some text before summarizing.")

```

### 🚀 Running the Program
  
🔹 Start the Streamlit App
Run the following command in the terminal:
```bash
streamlit run AI.py
```

### How to Run the App

You will get the following URLs after running the app:

- Local URL: `http://localhost:8501`
- Network URL: `http://192.168.XX.XXX.XXXX`

You can use the app locally using the **local URL** and access it on multiple devices if they are connected to the same network.


