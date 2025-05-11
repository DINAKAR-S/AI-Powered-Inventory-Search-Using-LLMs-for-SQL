# AI Powered Inventory Search Using LLM for SQL

This project provides an AI-powered inventory search solution utilizing Language Models (LLMs) to execute SQL queries. It allows data analysts to perform complex searches on an inventory database without manually writing SQL queries, making it optimal for faster, easier data retrieval.

### Real-Time Use Case:
This project is designed for data analysts who need to perform quick searches on large datasets. Rather than manually crafting every SQL query, the system uses LLMs like Google Gemini to interpret user queries and return accurate SQL results. The model can also generate complex queries and optimize search results using techniques like Few-Shot Learning.

Though LLMs are powerful, sometimes they may generate incorrect queries. To address this, we use the Few-Shot method to guide the model by providing example queries, improving its accuracy in handling complex queries.

## Features:
- AI-powered search for inventory data using Google Gemini LLM.
- Handles complex queries without needing to write SQL manually.
- Integrates with MySQL database to fetch and process data.
- Optimized using Few-Shot Learning to handle complex queries.
- User-friendly interface with Streamlit.

## File Structure:
```plaintext
AI-Powered-Inventory-Search/
├── chroma/                  # Folder for Chroma database
├── database/                # Folder for SQL database scripts
├── .env                     # Environment file to store API keys
├── few_shots.py             # Contains few-shot examples for complex queries
├── langchain_helper.py      # Helper functions for LangChain setup
├── main.py                  # Main application file (Streamlit)
├── requirements.txt         # Python dependencies
````

## Requirements:

Before running the application, ensure the following dependencies are installed:

* Python 3.8+
* MySQL or MariaDB
* Google Gemini API Key (from [Google AI Studio](https://aistudio.google.com/app/apikey))

### Dependencies:

* `streamlit`
* `langchain`
* `chromadb`
* `google-generativeai`
* `pymysql`
* `python-dotenv`
* `huggingface-hub`

## Setup Instructions:

### 1. Clone the Repository:

Clone the repository to your local system using Git:

```bash
git clone https://github.com/DINAKAR-S/AI-Powered-Inventory-Search-Using-LLMs-for-SQL.git
```

### 2. Navigate to the Project Directory:

```bash
cd AI-Powered-Inventory-Search
```

### 3. (Optional) Create and Activate a Virtual Environment:

It’s recommended to use a virtual environment to isolate the project dependencies.

* Create a virtual environment:

  ```bash
  python -m venv venv
  ```

* Activate the virtual environment:

  * On Windows:

    ```bash
    .\venv\Scripts\activate
    ```
  * On macOS/Linux:

    ```bash
    source venv/bin/activate
    ```

### 4. Install Dependencies:

Install all the required libraries using the following command:

```bash
pip install -r requirements.txt
```

### 5. Set Up Google Gemini API Key:

Go to [Google AI Studio](https://aistudio.google.com/app/apikey) to obtain your Google Gemini API key. Then, create a `.env` file in the root directory of your project and add your API key:

```plaintext
GOOGLE_GEMINI_API_KEY=your_api_key_here
```

### 6. Set Up MySQL Database:

1. Open the `database` folder and run the SQL scripts in MySQL Workbench or your preferred SQL client.
2. Make sure that the MySQL server is running and accessible.

### 7. Run the Application:

Once everything is set up, run the application using Streamlit:

```bash
streamlit run main.py
```

This will launch the web application in your browser, where you can ask natural language queries to retrieve inventory data.

## Example Queries:

1. **How many t-shirts do we have left for Nike in XS size and white color?**
2. **How much is the total price of the inventory for all S-size t-shirts?**
3. **If we have to sell all the Levi’s T-shirts today with discounts applied, how much revenue will our store generate?**
4. **How many white color Levi's shirts are available in stock?**

## Conclusion:

This project leverages AI-powered language models to make complex SQL database queries easier for data analysts and non-technical users. It is designed to help teams and businesses retrieve crucial data efficiently without the need to write intricate SQL queries. By utilizing Few-Shot Learning, we improve the model's ability to handle more sophisticated and nuanced queries.

### Disclaimer:

Though LLMs are a powerful tool, sometimes they may generate incorrect or suboptimal queries. In such cases, the Few-Shot method helps to guide the model by providing it with examples of complex queries.

## License:

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
