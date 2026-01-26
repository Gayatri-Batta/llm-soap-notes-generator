# LLM SOAP Notes Generator

A Natural Language Processing (NLP) tool that utilizes Large Language Models (LLMs) to automatically generate structured **SOAP notes** (Subjective, Objective, Assessment, Plan) from unstructured patient-doctor conversation transcripts.

This project is designed to streamline clinical documentation by extracting key medical information from text-based transcripts.

## About the Project
Medical documentation is time-consuming. This repository contains a Jupyter Notebook that demonstrates how to automate the creation of SOAP notes using Generative AI. It takes a raw text transcript of a clinical consultation and outputs a professionally formatted note using the **Llama3-Med42-8B** model.

## Features
* **Medical Domain Model:** Uses `m42-health/Llama3-Med42-8B`, fine-tuned for medical reasoning.
* **Why this model?** It is fine-tuned specifically for medical reasoning, offering higher accuracy for clinical tasks compared to generic LLMs.
* **Memory Efficient:** Implements 8-bit quantization to reduce VRAM usage.
* **Structured Formatting:** Automatically segments information into Subjective, Objective, Assessment, and Plan categories.
* **Batch Processing:** Capable of iterating through multiple transcript files in a single run.

## Prerequisites
Before running this project, ensure you have the following installed:
* **Python 3.8+**
* **GPU** with at least 12GB VRAM (Tested on Google Colab T4 GPU)
* **Jupyter Notebook** (or access to Google Colab)

## Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/Gayatri-Batta/llm-soap-notes-generator.git
    cd llm-soap-notes-generator
    ```

2.  **Create a virtual environment**
    ```bash
    python -m venv venv
    # Windows:
    venv\Scripts\activate
    # Mac/Linux:
    source venv/bin/activate
    ```

3.  **Install required dependencies**
    ```bash
    pip install -U bitsandbytes accelerate transformers torch sentencepiece tqdm
    ```

## Usage

1.  **Add Transcripts**
    Place your transcript text files (e.g., `encounter_1.txt`) inside the `data/raw-transcripts` folder.

2.  **Launch Jupyter Notebook**
    ```bash
    jupyter notebook
    ```
    *Or upload the `.ipynb` file to Google Colab.*

3.  **Configure Paths**
    Open `soap-notes-generator.ipynb` and verify the input/output directory variables:
    ```python
    TRANSCRIPTS_INPUT_DIR = "./data/raw-transcripts"
    SOAP_OUTPUT_DIR = "./data/processed-soap-notes"
    ```

4.  **Run the Cells:** Execute the cells in order to load the quantized model and process the transcripts.

## Project Structure

```text
llm-soap-notes-generator/
├── data/
│   ├── processed-soap-notes/    # Output folder where generated SOAP notes are saved
│   └── raw-transcripts/         # Input folder containing .txt files of patient encounters
├── soap-notes-generator.ipynb   # Main Jupyter Notebook containing the logic
├── README.md                    # Project documentation
