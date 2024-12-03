### **Repository Structure**
```
USTC-RAG-2048-Chatbot
├── README.md
├── requirements.txt
├── app
│   ├── __init__.py
│   ├── main.py
│   ├── templates
│   │   ├── index.html
│   └── static
│       ├── style.css
├── models
│   ├── embed_model.py
│   ├── response_model.py
├── utils
│   ├── pinecone_utils.py
│   ├── langchain_utils.py
├── data
│   ├── ustc_faqs.json
│   ├── course_catalogs.json
│   ├── faculty_bios.json
│   ├── fee_structures.json
├── docs
│   ├── architecture_diagram.png
│   ├── user_manual.pdf
└── tests
    ├── test_models.py
    ├── test_integration.py
   ''''


### **README.md**

**USTC AI Assistance Chatbot**

![Chatbot UI Preview](docs/architecture_diagram.png)

## **Overview**
The USTC AI Assistance Chatbot is a sophisticated solution designed for the **University of Science and Technology Chittagong (USTC)** to automate responses to student queries about admissions, courses, faculty, and academic resources. It utilizes cutting-edge NLP technologies and vector-based search mechanisms for efficient and accurate query resolution.

---
**System Architucture**
![Picture1](https://github.com/user-attachments/assets/6eea724a-7f29-4ccc-a7e9-cf2cac46e271)


## **Key Features**
- **Advanced NLP Models**: Powered by `meta/llama3-70b-instruct` for generating contextual responses.
- **Semantic Search**: Integrated `nvidia/llama-3.2-nv-embedqa-1b-v1` for embedding queries and retrieving relevant information from the Pinecone vector database.
- **LangChain Framework**: Enables chaining and document combination for comprehensive responses.
- **Responsive UI**: Built with Gradio and Flask for a seamless user experience.
- **Scalable Architecture**: Modular design ensures scalability and easy maintenance.

---

## **System Architecture**
The chatbot architecture includes:
1. **Input Query Processing**: User inputs are tokenized and embedded using NVIDIA models.
2. **Document Retrieval**: Pinecone is used to fetch semantically similar documents.
3. **Response Generation**: Meta models generate personalized and context-aware responses.
4. **User Interface**: Gradio provides an interactive web-based frontend.
![Picture1](https://github.com/user-attachments/assets/b7e4a78a-c9b1-4602-9f7f-3c582f42f8aa)

---

## **Setup and Installation**

### **Prerequisites**
- Python 3.8 or above
- Pip package manager
- NVIDIA GPU (optional but recommended for faster processing)

### **Steps**
1. Clone this repository:
   ```bash
   git clone https://github.com/USTC-RAG-2048/USTC-AI-Chatbot.git
   cd USTC-AI-Chatbot
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up Pinecone:
   - Create an account at [Pinecone](https://www.pinecone.io/).
   - Add your API key in a `.env` file:
     ```
     PINECONE_API_KEY=your_api_key
     PINECONE_ENV=your_env
     ```

4. Run the chatbot:
   ```bash
   python app/main.py
   ```

5. Access the web interface at `http://127.0.0.1:5000`.

---
To click local hosting link to show UI: 
![ui](https://github.com/user-attachments/assets/1a940e90-d203-42a4-aa09-e933c39ee565)




## **Usage**
- **User Queries**: Ask questions like:
  - "What are the admission requirements for the CSE department?"
  - "What is the tuition fee for undergraduate programs?"
- **Output**: The chatbot retrieves and synthesizes responses in real-time.
## Output ##
![OUTPUT](https://github.com/user-attachments/assets/9cfb4438-0f98-4cda-b6f9-41592287b496)

---

## **Folder Structure**
- **app**: Contains the Flask application and Gradio integration.
- **models**: Includes the embedding and response-generation models.
- **utils**: Helper functions for Pinecone and LangChain integration.
- **data**: Preprocessed datasets (FAQs, course catalogs, etc.).
- **docs**: Documentation and diagrams for the project.
- **tests**: Unit and integration test scripts.

---
**System Architucture**
![Picture1](https://github.com/user-attachments/assets/6eea724a-7f29-4ccc-a7e9-cf2cac46e271)

## **Future Enhancements**
1. **Multilingual Support**: Enable chatbot responses in multiple languages.
2. **Context-Aware Memory**: Retain conversation history for personalized responses.
3. **Mobile Integration**: Develop native apps for iOS and Android.
4. **Adaptive Learning**: Improve response accuracy using student feedback.

   
**System Diagram**

![Screenshot 2024-12-01 015212](https://github.com/user-attachments/assets/8118b426-4333-4b5f-91ca-28bace3e8990)

---

## **Contributing**
We welcome contributions! Please follow these steps:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit changes and push:
   ```bash
   git commit -m "Add your feature"
   git push origin feature/your-feature-name
   ```
4. Create a pull request.

---

## **License**
This project is licensed under the MIT License. See `LICENSE` for details.

---

## **References**
1. [Pinecone Documentation](https://www.pinecone.io/)
2. [LangChain Documentation](https://python.langchain.com/)
3. [NVIDIA LLaMA 3.2 EmbedQA](https://catalog.ngc.nvidia.com/orgs/nvidia/models/llama-3.2-nv-embedqa-1b-v1)
4. [Meta LLaMA 3](https://ai.meta.com/research/publications/llama/)
5. [Gradio Documentation](https://gradio.app/)

---

This **README.md** should provide comprehensive information for developers, contributors, and users of the chatbot. Let me know if you'd like further refinements!
