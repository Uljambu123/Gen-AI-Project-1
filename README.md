# 🦜 LangChain: Chat with SQL DB

## Project Overview  
This project is a **Streamlit-based interactive chatbot** that allows users to query an SQL database using **LangChain** and **Groq API**. It supports **SQLite** and **MySQL**, enabling users to select their preferred database and interact with it dynamically.

## Objective  
The main goal of this project is to provide a **user-friendly chat-based interface** for querying structured databases without requiring complex SQL knowledge.

## Key Steps in the Project  

1. **Set up the Streamlit UI**  
   - Configures a sidebar for selecting the database type (**SQLite/MySQL**)  
   - Allows users to enter credentials for MySQL and API keys  

2. **Database Configuration**  
   - Uses `sqlite3` for **SQLite** connections  
   - Uses `mysql-connector-python` for **MySQL** connections  

3. **Initialize the Language Model**  
   - Uses **LangChain’s ChatGroq model** (Llama3-8b-8192) for conversational AI  
   - Implements caching for optimized performance  

4. **Create SQL Agent**  
   - Uses **LangChain’s SQLDatabaseToolkit** to interact with the database  
   - Implements **ZERO_SHOT_REACT_DESCRIPTION** agent for intelligent query handling  

5. **User Interaction via Chat**  
   - Stores chat history in `st.session_state`  
   - Processes user queries and generates dynamic responses  

## Technologies Used  
- **Python**  
- **Streamlit**  
- **LangChain**  
- **SQLite/MySQL**  
- **SQLAlchemy**  
- **LangChain-Groq**  
- **Streamlit Callback Handler**  

## How to Run  

### **1️⃣ Install Dependencies**  
Run the following command to install the required packages:  

```bash
pip install -r requirements.txt

2️⃣ Set Up the SQLite Database
The project comes with a sample database (student.db) that contains a simple student table.
If needed, create the database by running:
python sqlite.py

3️⃣ Run the Streamlit App
Start the Streamlit interface:
streamlit run "Chat with SQL DB.py"

4️⃣ Interact with the Chatbot
Choose SQLite or MySQL from the sidebar
Enter MySQL credentials (if applicable)
Enter your Groq API key
Start chatting with the database!

## Conclusions
This project demonstrates how LLMs can enhance database querying by allowing users to interact with structured databases using natural language.
The chatbot successfully retrieves and processes data using LangChain's SQL agent, making database interactions easier.

## Future Work
🔹 Support for additional database types (PostgreSQL, MongoDB)
🔹 Enhance query optimization techniques
🔹 Enable user authentication and access control
🔹 Improve response explanations using AI-generated summaries
🔹 Add support for advanced analytical queries
