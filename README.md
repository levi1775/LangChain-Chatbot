# LangChain Chatbot

![LangChain Chatbot](https://img.shields.io/badge/LangChain-Chatbot-blueviolet)
![Cohere Chat Model](https://img.shields.io/badge/Cohere-Chat--Model-green)
![HuggingFace Embeddings](https://img.shields.io/badge/HuggingFace-Embeddings-yellow)

A smart conversational AI built with **LangChain** and the **Cohere Chat Model** that processes documents, creates text embeddings, and maintains context-aware conversations.

---

## Table of Contents

- [🚀 Project Overview](#-project-overview)
- [📂 Data Source](#-data-source)
- [🔧 How It Works](#-how-it-works)
- [🛠 Tech Stack](#-tech-stack)
- [💡 Features](#-features)
- [🤝 Contributing](#-contributing)
- [📧 Contact](#-contact)
- [🎯 Future Improvements](#-future-improvements)

---

## 🚀 Project Overview

This project builds a smart conversational AI that:

- **Reads and processes documents:** Breaks down text from files into manageable chunks.
- **Creates text embeddings:** Converts text into vector representations using **HuggingFace Embeddings**.
- **Maintains context:** Remembers previous interactions to generate context-aware responses.
- **Supports research and education:** Ideal for natural language understanding applications.

---

## 📂 Data Source

The chatbot works with documents stored as `.txt` files. Two dedicated folders help organize content:

- **Research Papers** 📄
- **Lecture Notes** 🎓 ([Stanford CS324 Lectures](https://stanford-cs324.github.io/winter2022/lectures/))

---

## 🔧 How It Works

1. **Loading Data** 📥  
   - Utilizes `DirectoryLoader` to import text documents.

2. **Splitting Documents** ✂️  
   - Uses `RecursiveCharacterTextSplitter` to split texts into chunks of **400 characters** with a **30-character overlap**.

3. **Creating Embeddings** 🤖  
   - Converts text chunks into embeddings with **HuggingFaceEmbeddings** to capture semantic meaning.

4. **Storing Embeddings** 📦  
   - Saves embeddings in a **Chroma vector store** for efficient retrieval.

5. **Retrieval & Response Generation** 🔍  
   - Retrieves the **top 7 similar embeddings** from the Chroma database.
   - Filters context using compression techniques.
   - Sends refined data along with user query and chat history to the **Cohere Chat Model** to generate responses.

---

## 🛠 Tech Stack

- **LangChain** – Framework for building chatbots
- **Cohere Chat Model** – Conversational AI engine
- **Hugging Face Embeddings** – Text vectorization
- **ChromaDB** – Semantic search and vector storage
- **Python** – Core programming language

---

## 💡 Features

- **Context-aware conversation:** Remembers past interactions.
- **Efficient document processing:** Splits documents intelligently for better embedding.
- **Semantic search:** Retrieves the most relevant information quickly.
- **Modular design:** Easy to extend and integrate new features.

---

## 🤝 Contributing

Contributions are welcome! If you’d like to improve the analysis, add new features, or provide additional insights, feel free to fork the repository and submit a pull request. Your input helps make this project even better.

---

## 📧 Contact

For questions or feedback, please reach out:

**Your Name**  
- 📧 Email: [your.email@example.com](mailto:your.email@example.com)  
- 💻 GitHub: [your-username](https://github.com/your-username)  
- 🔗 LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/your-linkedin-profile)

---

## 🎯 Future Improvements

- ✅ **Implement Routing:** Enhance data retrieval accuracy.
- ✅ **Deploy the Chatbot:** Integrate with **Streamlit** for a web-based interface.
- ✅ **Automatic Chat Saving:** Enable persistent storage and retrieval of chat sessions.
