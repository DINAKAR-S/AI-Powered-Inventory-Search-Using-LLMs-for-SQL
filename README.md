# AI-Powered Inventory Search Using LLMs for SQL

This project is designed for real-time use cases where data analysts can perform inventory searches in an optimal manner. Instead of manually figuring out SQL queries for each search, analysts can simply ask natural language questions, and the system will automatically generate the necessary SQL queries to fetch the relevant data. This enhances productivity and allows for faster, more efficient decision-making in inventory management and sales analysis.

## Project Structure

The project follows a simple structure:

```

AI-Powered-Inventory-Search/
│
├── chroma_db/               # Chroma database storage
├── database/                # MySQL database setup
│
├── .env                     # Environment variables (Google Gemini API key)
├── few_shots.py             # Few-shot training data for the model
├── langchain_helper.py      # Helper functions to build the LangChain pipeline
├── main.py                  # Main Streamlit app for querying the inventory
└── requirements.txt         # Python dependencies

````

## Setup Instructions

Follow these steps to set up and run the project locally:

### 1. Install MySQL and MySQL Workbench
Ensure that **MySQL** and **MySQL Workbench** are installed on your system. You will use MySQL Workbench to run SQL queries on the database.

### 2. Setup the Database

1. Open **MySQL Workbench** and navigate to the `database` folder in the project.
2. Inside the `database` folder, you should find the necessary SQL scripts to set up your T-shirt inventory database.
3. Run the SQL script in MySQL Workbench to create the database and necessary tables.

### 3. Install Python Dependencies

Make sure you have Python 3.12 or higher installed. Install the required libraries by running:

```bash
pip install -r requirements.txt
````

### 4. Set Up the Google Gemini API Key

1. Visit [AI Studio Google API](https://aistudio.google.com/app/apikey) to generate your **Google Gemini API key**.
2. Save the generated API key into a `.env` file in the root directory of the project, using the following format:

```plaintext
GOOGLE_GEMINI_API_KEY=your_api_key_here
```

### 5. Run the Application

After setting up the environment and API key, run the application using:

```bash
streamlit run main.py
```

This will launch a **Streamlit web interface** where you can interact with the inventory database by asking natural language queries. The app will convert your questions into SQL queries, fetch the data, and display the answers.

### 6. Example Queries

Here are some example queries you can try once the app is up and running:

* "How many white Levi's T-shirts are in stock?"
* "What is the total price of the inventory for all S-size T-shirts?"
* "How much revenue will the store generate if all large Nike T-shirts are sold after discounts?"

### 7. Folder Details

* **chroma\_db/**: This folder stores the vector database used by LangChain for semantic search. It stores the embeddings and metadata used by the AI model to find relevant examples for query generation.
* **database/**: This folder contains the SQL scripts to set up the T-shirt inventory database.
* **.env**: Store your environment variables, such as the Google Gemini API key, here.
* **few\_shots.py**: Contains the few-shot examples that train the model on SQL query generation from natural language.
* **langchain\_helper.py**: Helper functions to build the LangChain pipeline for SQL database interaction and LLM integration.
* **main.py**: The main Streamlit app that allows users to input natural language queries and fetch results from the database.

## Requirements

* Python 3.12 or higher
* MySQL
* Google Gemini API Key
* Libraries listed in `requirements.txt`

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Use Case

This project is built with **data analysts** in mind who need to perform fast and efficient searches in large databases. Instead of manually constructing SQL queries, they can simply ask questions like "How many white Levi's T-shirts are in stock?" or "What is the total revenue from selling large Nike T-shirts after discounts?" The system will generate the SQL queries for them and fetch the answers in real time, saving time and increasing efficiency in daily tasks.

---

### You can make this as an Template and use it for various other datasets of your company
