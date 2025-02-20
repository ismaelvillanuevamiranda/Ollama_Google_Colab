# 🦙 Ollama_Google_Colab - Run LLMs Locally on Google Colab  

## 🚀 Overview
**Ollama_Google_Colab** is a Python-based tool for setting up **local LLM models** using [Ollama](https://ollama.com/) on **Google Colab or a local machine**. This project allows you to **install, manage, and interact** with models like **Llama, Mixtral, etc.** without external API dependencies.

With **OllamaManager**, you can:  
✅ Install Ollama automatically  
✅ Start and manage the Ollama server  
✅ Pull and switch between different LLM models  
✅ Interact with local models using OpenAI-compatible API  

---

## 📦 Installation
You can run the script on **Google Colab** or your **local machine**.

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/Ollama_Google_Colab.git
cd Ollama_Google_Colab
```


### 2️⃣ Install Dependencies (Handled Automatically)
The script installs the necessary dependencies, but if you need to do it manually, run:
```bash
pip install openai pandas requests
```

---

## 🏁 Usage

### 1️⃣ **Initialize and Setup Ollama**
```python
from ollama_manager import OllamaManager

# Initialize Ollama with a default model
ollama = OllamaManager(model="llama3.1:latest")
```

### 2️⃣ **List Installed Models**
```python
ollama.list_installed_models()
```

### 3️⃣ **Ask Questions to LLM**
```python
role = "You are a logical reasoning and mathematics assistant."
query = "If I hang 5 shirts outside and it takes them 5 hours to dry, how long would it take to dry 30 shirts?"

answer = ollama.agent.ask_question(query, role)
print("🧠 Response:", answer)
```

### 4️⃣ **Switch Between Models**
```python
ollama.change_model("mistral:7b")  # Switch to a different model
```


---

## 🧠 Example Output
```
🔹 Response from llama3.1:
It will still take 5 hours to dry 30 shirts, assuming the drying conditions remain the same.
```

---

## 📌 Supported Models
- `llama3.1:latest`
- `mistral:7b`
- Any model available in Ollama

---

## 🛠️ Requirements
- **Python 3.8+**
- **Ollama**
- **pip install openai pandas requests** (handled by the script)

---

## ⚡ Troubleshooting
If you encounter issues, try the following:

- **Ensure Ollama is running:**  
  ```bash
  ollama serve
  ```

- **Check installed models:**  
  ```bash
  ollama list
  ```

- **Manually pull a model:**  
  ```bash
  ollama pull llama3.1:latest
  ```

---

## 📌 Notes
- If running in **Google Colab**, make sure you have a **GPU runtime enabled** (`Runtime > Change runtime type > GPU`).
- Ollama runs **entirely locally**, ensuring **privacy and security** when processing queries.

---

## 🔗 Resources
- [Ollama Documentation](https://ollama.com/)
- [Google Colab Guide](https://colab.research.google.com/)

---

## 📜 License
This project is licensed under the **MIT License**.

---

🎉 **Now you can run LLMs locally on Google Colab!**
