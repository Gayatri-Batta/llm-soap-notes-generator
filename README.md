# llm-soap-notes-generator

# LLM SOAP Notes Generator 🩺

A Natural Language Processing (NLP) tool that utilizes Large Language Models (LLMs) to automatically generate structured **SOAP notes** (Subjective, Objective, Assessment, Plan) from unstructured patient-doctor conversation transcripts.

This project is designed to streamline clinical documentation by extracting key medical information from text-based transcripts.

## About the Project
Medical documentation is time-consuming. This repository contains a Jupyter Notebook that demonstrates how to automate the creation of SOAP notes using Generative AI. It takes a raw text transcript of a clinical consultation and outputs a professionally formatted note.

## Features
* **Text Analysis:** Processes raw conversation text between a patient and a provider.
* **Structured Formatting:** Automatically segments information into Subjective, Objective, Assessment, and Plan categories.
* **Custom Prompting:** Uses engineered prompts to ensure the LLM maintains a professional medical tone.
* **Easy Integration:** Code is contained in a single notebook for easy testing and modification.

## Prerequisites
Before running this project, ensure you have the following installed:
* **Python 3.8+**
* **Jupyter Notebook** (or access to Google Colab)
* **OpenAI API Key** (or an equivalent LLM API key)

## Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/Gayatri-Batta/llm-soap-notes-generator.git](https://github.com/Gayatri-Batta/llm-soap-notes-generator.git)
    cd llm-soap-notes-generator
    ```

2.  **Create a virtual environment **
    ```bash
    python -m venv venv
    # Windows:
    venv\Scripts\activate
    # Mac/Linux:
    source venv/bin/activate
    ```

3.  **Install required dependencies**
    ```bash
    pip install openai notebook pandas
    ```

## Usage

1.  **Launch Jupyter Notebook**
    ```bash
    jupyter notebook
    ```
    *Or upload the `.ipynb` file to Google Colab.*

2.  **Open the file:** `soap_generator.ipynb` (or the name of your notebook file).

3.  **Configure API Key:**
    * Locate the cell defining the API key in the notebook.
    * Replace the placeholder with your actual key:
        ```python
        openai.api_key = "sk-..."
        ```
    * *Note: Never commit your actual API key to GitHub.*

4.  **Run the Cells:** Execute the cells in order to process the sample transcript provided in the notebook.

## 📂 Project Structure

```text
llm-soap-notes-generator/
├── soap_generator.ipynb   # Main logic and demonstration
├── README.md              # Project documentation
