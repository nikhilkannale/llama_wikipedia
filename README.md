# RAG-Powered Web Q&A using Groq Llama 3 & Hugging Face

An AI-powered web question-answering application that extracts content from any webpage and allows users to ask questions about it using **Retrieval-Augmented Generation (RAG)**. The application uses Groq's Llama 3 model for fast AI responses, Hugging Face embeddings for semantic search, and Streamlit for an interactive chat interface.

## 🚀 Features

- **Web Content Extraction:** Extracts text content from websites using BeautifulSoup.
- **AI-Powered Question Answering:** Ask questions based on extracted webpage content.
- **Retrieval-Augmented Generation (RAG):** Retrieves relevant information before generating answers.
- **Groq Llama 3 Integration:** Uses Groq API for fast LLM-powered responses.
- **Hugging Face Embeddings:** Uses `all-MiniLM-L6-v2` for converting text into vector embeddings.
- **Vector Search:** Uses LlamaIndex to create and retrieve relevant document information.
- **Interactive Chat Interface:** Provides a conversational interface using Streamlit.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Web application interface |
| Groq API | AI-powered response generation |
| Llama 3 | Large Language Model |
| LangChain | LLM integration |
| LlamaIndex | RAG pipeline and vector indexing |
| Hugging Face | Text embedding generation |
| Sentence Transformers | Semantic embeddings |
| BeautifulSoup | Webpage content extraction |
| Requests | HTTP requests |
| Python Dotenv | Environment variable management |

## 🏗️ Project Architecture

```text
                User
                  |
                  v
          Enter Website URL
                  |
                  v
          Fetch Webpage Content
                  |
                  v
          BeautifulSoup Parser
                  |
                  v
          Extract Text Content
                  |
                  v
          Hugging Face Embeddings
                  |
                  v
          LlamaIndex Vector Index
                  |
                  v
          User Asks a Question
                  |
                  v
          Retrieve Relevant Context
                  |
                  v
          Groq Llama 3 Model
                  |
                  v
          Generate AI Response
                  |
                  v
          Display Answer in Streamlit
```

## 📂 Project Structure

```text
RAG-Web-QA/
│
├── app.py                 # Main Streamlit application
├── .env                   # API key configuration
├── .gitignore             # Files excluded from Git
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
└── Untitled design.png    # Application image
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the Project Folder

```bash
cd RAG-Web-QA
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Configure Groq API Key

Create a `.env` file in the project root directory.

Add your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Get your API key from:

https://console.groq.com/keys

**Important:** Never upload your `.env` file or expose your API key on GitHub.

### 6. Run the Application

```bash
streamlit run app.py
```

The application will open in your browser, usually at:

```text
http://localhost:8501
```

## 💻 How to Use

1. Launch the Streamlit application.
2. Enter the URL of a webpage.
3. Click the appropriate action or press Enter to process the URL.
4. Wait for the webpage content to be extracted and indexed.
5. Enter your question in the chat input.
6. Receive an AI-generated answer based on the webpage content.
7. Continue asking questions about the same webpage.

## 🧠 Core Concepts

### 1. Retrieval-Augmented Generation (RAG)

RAG combines information retrieval with large language models. Instead of relying only on the model's pretrained knowledge, the application retrieves relevant information from the webpage to support its answers.

### 2. Hugging Face Embeddings

The application uses:

`sentence-transformers/all-MiniLM-L6-v2`

This model converts text into numerical vector representations that support semantic similarity search.

### 3. LlamaIndex

LlamaIndex manages document indexing and retrieval, helping identify relevant webpage information for user queries.

### 4. Groq Llama 3

Groq provides fast inference for the Llama 3 language model, which generates responses using the retrieved information.

## 🔐 Security

- Store API keys in environment variables.
- Never commit `.env` files.
- Use `.gitignore` to exclude sensitive configuration files.
- Validate URLs before fetching webpage content.
- Use request timeouts to avoid hanging requests.

## 🔮 Future Enhancements

- Support multiple webpage URLs.
- Add PDF and document-based question answering.
- Implement conversation memory.
- Add source citations for generated answers.
- Improve webpage extraction and text cleaning.
- Introduce persistent vector database storage.
- Support multiple LLM providers.
- Deploy the application using cloud hosting platforms.
- Add URL validation and SSRF protection.

## 👨‍💻 Author

**Nikhil Kannale**

Computer Science Engineering (Data Science)

GitHub: https://github.com/nikhilkannale

LinkedIn: https://www.linkedin.com/in/nikhil-kannale-497978396/

## 📜 License

This project is licensed under the MIT License.

---

⭐ If you find this project useful, consider giving it a star on GitHub!
