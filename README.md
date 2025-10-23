# Idea-Generator
#### *A Generative AI app that creates structured startup pitches. It uses the LaMini-Flan-T5 LLM to generate a Business Idea, Problem, and Solution based on a user-inputted industry domain. Features an interactive web interface built with Gradio.*

## Overview
This project is a sophisticated **Generative AI** application designed to function as a structured startup idea generator. It leverages a powerful **Large Language Model (LLM)** accessed via the Hugging Face ecosystem to transform a simple industry domain input (e.g., Fintech) into a comprehensive, structured startup pitch. The application is packaged with a user-friendly interface created using **Gradio**.

## Goal
The goal is to demonstrate the practical application of text-to-text generative models for creative and structured content creation, making the complex LLM accessible through a simple, shareable web interface.

## Methodology
The application workflow is defined as follows:
- **Model Loading**: The specialised `MBZUAI/LaMini-Flan-T5-783M` LLM is loaded using the `transformers` pipeline.
- **Prompt Engineering**: A specific system prompt is constructed to compel the LLM to provide output containing the three required sections (Idea, Problem, Solution).
- **Function Definition**: A core Python function handles input, constructs the prompt, executes the LLM inference call, and extracts the generated text.
- **UI Creation**: **Gradio** is used to wrap the function, providing a simple input box for the domain and a display area for the pitch.

## Features
- **Generative AI**: Uses an LLM to generate creative startup pitch ideas.
- **Domain-Based Generation**: Output is customized based on a user-provided industry domain.
- **Structured Output**: Generated ideas include mandatory sections: Business Idea, Problem Statement, and Solution.
- **Web UI**: Provides an interactive, shareable web interface built with Gradio.

## Results and Metrics
The output of the model is qualitative, focusing on **coherence, relevance, and adherence to the prompt structure**. A successful run yields a pitch idea that is logically sound and directly addresses the chosen domain with distinct sections.

## Tech Stack
The core technologies used to build and deploy the generative interface are:
| Tool | Purpose |
|------|---------|
|**Python**|Primary programming language.|
|**Hugging Face**|Used for accessing the pre-trained LLM (`LaMini-Flan-T5`) via the `transformers` library.|
|**Gradio**|Used to create the simple, interactive, shareable web interface.|
|**PyTorch/accelerate**|Backend framework for the model and optimization for faster inference speed.|
|**Model**|`MBZUAI/LaMini-Flan-T5-783M` (Instruction-tuned Text-to-Text LLM).|

## Prerequisites
- **Python 3.x** environment.
- **GPU access** is highly recommended (e.g., in Colab) for faster LLM inference.
- Required Python packages (listed in **Installation**).

## Installation
**Clone the repository and install the necessary deep learning and UI libraries:**

1. #### Clone the repository
```bash
git clone https://github.com/Tanmay2923/Idea-Generator.git
```

2. #### Install dependencies for model loading and UI
```bash
pip install transformers gradio torch accelerate
```

## Running the Application
This project runs locally or in a Colab environment and provides a web interface.
1. Open the file `Idea Generator` in Google Colab.
2. Run all cells. The final cell will execute the Gradio interface, providing a URL (local and public) to access the application.
3. Enter a domain (e.g., "Sustainable Fashion") into the text box and click the submit button to generate a structured pitch.
