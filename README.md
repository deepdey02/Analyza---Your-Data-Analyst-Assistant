# Analyza---Your-Data-Analyst-Assistant
Analyza is a Flask web application that transforms raw data files (CSV or Excel) into actionable insights using a powerful Large Language Model (LLM). Simply upload your dataset and ask a question in plain English; Analyza uses a Groq-powered backend to generate, execute, and display the resulting Pandas Python code and analysis.

Features
Easy Data Upload: Supports CSV and Excel file formats.

Intelligent Analysis: Leverages a Groq-hosted LLM (like Llama 3.3 70B Versatile) to interpret user questions and generate accurate data analysis code.

Pandas Execution: The generated Python code is executed securely on the server using Pandas, and the result is displayed instantly.

Transparent Process: Users can view the generated code and the data preview before seeing the final result, ensuring clarity and trust in the analysis.

Robust Data Preprocessing: Includes utility functions for automatic data type inference, handling missing values, and date conversion to ensure data quality before analysis.

Modern UI: A clean, responsive, and dark-themed user interface built with Tailwind CSS.

Tech Stack
Backend: Python (Flask)

Data Processing: Pandas

AI/LLM: Groq API (for code generation)

Frontend: HTML, Tailwind CSS, Jinja2 Templates

Getting Started
Prerequisites
Python 3.8+
A valid Groq API Key.

File Upload & Query: The user uploads a file and enters a question via the form (index2.html).
Preprocessing: The utils.preprocess_and_save function cleans the data and loads it into a Pandas DataFrame (df).
Code Generation: The user's query and the df context are sent to the Groq API, which acts as a "Python data analyst" to generate the necessary Pandas code.
Code Execution: The returned Python code is executed safely using exec() with the loaded df.
Result Display: The final result (which can be a DataFrame, series, or single value) is converted to HTML or a string and displayed to the user.
