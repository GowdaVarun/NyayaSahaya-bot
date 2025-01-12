# NyayaSahaya Chatbot ⚖️  

An intelligent legal chatbot specializing in the **Indian Penal Code (IPC)**. This AI-powered assistant provides precise legal information, leveraging a FAISS-based vector database and advanced embeddings for document retrieval.

---

## Features  
- **Legal Expertise**: Accurate responses based on the Indian Penal Code.  
- **Vector Store**: Efficient similarity search using FAISS.  
- **Custom Embeddings**: Powered by Hugging Face's **InLegalBERT** model.  
- **Interactive UI**: Built with Streamlit for user-friendly interaction.  

---

## Installation  

1. Clone the repository:  
   ```bash  
   https://github.com/GowdaVarun/NyayaSahaya-bot.git
   cd NyayaSahaya-bot  
   ```  

2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  

3. Prepare your environment:  
   - Set up a `.env` file with your Together API key:  
     ```env  
     TOGETHER_API_KEY=your_together_api_key  
     ```  

4. Create the FAISS vector store by running:  
   ```bash  
   python Ingest.py  
   ```  

5. Start the chatbot:  
   ```bash  
   streamlit run app.py  
   ```  

---

## Usage  

- **Step 1**: Prepare the `data/` directory with text files containing IPC-related content.  
- **Step 2**: Run `ingest.py` to process and embed the documents into a FAISS database.  
- **Step 3**: Use `app.py` to interact with the chatbot and query legal information.  
- Reset conversations anytime using the **Reset All Chat** button in the interface.  

---

## File Structure  

### `app.py`  
The main application file for the NyayaSahaya chatbot:  
- Initializes the chatbot UI using **Streamlit**.  
- Implements conversational memory and FAISS-based document retrieval.  
- Customizes the response format with a **prompt template**.  

### `ingest.py`  
Prepares the FAISS vector store by:  
- Loading text files from the `data/` directory.  
- Splitting content into manageable chunks using a text splitter.  
- Generating embeddings with **InLegalBERT**.  
- Storing the embeddings in a FAISS index for efficient retrieval.  

---

## Technologies Used  

- **Streamlit**: Interactive UI framework.  
- **FAISS**: Efficient similarity search for document retrieval.  
- **Hugging Face InLegalBERT**: Domain-specific embeddings for legal text.  
- **Ray**: Parallel processing to improve performance.  
- **RecursiveCharacterTextSplitter**: For chunking text efficiently.  

---

## Acknowledgments  

Special thanks to Hugging Face, FAISS, and the developers of the tools that made this project possible.  

---  

Feel free to report issues or contribute to the project! 🚀  
