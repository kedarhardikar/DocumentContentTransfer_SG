# DocumentContentTransfer_SG
The task is to automate the process of content transfer between 2 documents. Given a structured previous year report and an unstructured current year report, replace the older values in the structured report using the updated values

## Document Content Transfer using LLM & PDF Processing

Overview

This project automates the transfer of numerical data from the current year's report into the previous year's report while maintaining the document structure, wording, and formatting. It leverages Python, LangChain, Llama 3.1 (via Groq API), and document processing libraries to ensure seamless data extraction and replacement.

Features

PDF Text Extraction: Extracts text from PDFs using PyMuPDF.

Data Anonymization: Replaces all numerical values in the previous report with placeholders (__).

AI-Powered Content Replacement: Uses an LLM model (Llama 3.1) to identify and replace missing values using corresponding values from the current report.

Maintains Formatting: Converts PDF to DOCX, processes text, and re-converts back to a formatted PDF.

End-to-End Automation: Handles everything from extraction to final document generation.

Installation

Prerequisites

Ensure you have Python 3.8+ and the following dependencies installed:

pip install pymupdf langchain langchain_groq dotenv pdf2docx python-docx docx2pdf

Set up your Groq API Key in a .env file:

GROQ_API_KEY=your_api_key_here

Usage

1. Extract Text from PDFs

The script extracts content from both the previous year's and the current year's reports.

2. Replace Numbers with Placeholders

The extracted previous year's text is processed to replace numerical values with __.

3. Fill Missing Values Using LLM

Using LangChain and Groq, the missing values in the previous year's report are automatically filled with corresponding values from the current year's report.

4. Generate Final Report

The updated document is saved as a DOCX file and then converted back to PDF while maintaining the original formatting.
