# LangChain Chatbot

![LangChain Chatbot](https://img.shields.io/badge/LangChain-Chatbot-blueviolet) ![Cohere-Chat-Model](https://img.shields.io/badge/Cohere-Chat--Model-green) ![HuggingFace-Embeddings](https://img.shields.io/badge/HuggingFace-Embeddings-yellow)

## 🚀 Project Overview
This project builds a smart conversational AI using **LangChain** and the **Cohere Chat Model**. The chatbot reads documents, breaks them into manageable pieces, and creates **text embeddings** for efficient processing. It remembers previous interactions, ensuring **context-aware conversations** and generating accurate, relevant responses.

The chatbot is designed for various **natural language understanding applications**, making it highly suitable for research and educational purposes.

## 📂 Data Source
- **Documents are stored as `.txt` files.**
- Two dedicated folders:
  - **Research Papers** 📄
  - **Lecture Notes** 🎓 (From [Stanford CS324 Lectures](https://stanford-cs324.github.io/winter2022/lectures/))

## 🔧 How It Works
1. **Loading Data** 📥  
   - Text documents are loaded from a directory using `DirectoryLoader`.
2. **Splitting Documents** ✂️  
   - Documents are split into chunks of **400 characters** with a **30-character overlap** using `RecursiveCharacterTextSplitter`.
3. **Creating Embeddings** 🤖  
   - Chunks are converted into embeddings using **HuggingFaceEmbeddings** to capture semantic meaning.
4. **Storing Embeddings** 📦  
   - The embeddings are stored in a **Chroma vector store** and saved in a database.
5. **Retrieval & Response Generation** 🔍  
   - A retriever searches for the **top 7 similar embeddings** in the Chroma database.  
   - Contextual compression filters out irrelevant data.  
   - The refined data, user query, and chat history are sent to the **Cohere Chat Model**.  
   - The model generates **coherent and context-aware responses**.

## 🛠 Tech Stack
- **LangChain** (for structured chatbot development)
- **Cohere Chat Model** (for conversational AI)
- **Hugging Face Embeddings** (for text vectorization)
- **ChromaDB** (for semantic search & vector storage)
- **Python** (Core development language)
  
## Contributing  

Contributions are welcome! If you would like to improve the analysis, add new features, or provide additional insights, please feel free to fork the repository and submit a pull request.  

## 📧 Contact  

For questions or feedback, feel free to reach out:  

**Your Name**  

- 📧 Email: [your.email@example.com](mailto:your.email@example.com)  
- 💻 GitHub: [your-username](https://github.com/your-username)  
- 🔗 LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/your-linkedin-profile)  
 
  

## 🎯 Future Improvements
- ✅ **Implement Routing** for more **accurate data retrieval** 🔀  
- ✅ **Deploy the chatbot** using **Streamlit** 🌐  
- ✅ **Enable automatic chat saving and retrieval** 💾  

