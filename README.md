# AI-Powered Resume & Cover Letter Generator
A user-friendly Python tool in Google Colab that generates ATS-friendly resumes and cover letters with optional styled templates and Google Drive integration.

## Table of Contents
Overview

Features

How It Works

Getting Started

Usage

Challenges & Solutions

Contributing

## Overview
This project provides a streamlined tool for job seekers to create well-formatted, Applicant Tracking System (ATS)-compatible resumes and cover letters directly within Google Colab. Without requiring manual document editing or external software, users can input their personal and professional data to automatically generate polished PDFs, with options for Google Drive integration for convenient storage.

## Features
Interactive User Prompts: Guided data entry for personal info, education, experience, skills, projects, certifications, and more.

PDF Generation: Choose between a clean ATS-friendly layout or a stylized (fancy) template.

Cover Letter Support: Build custom cover letters using user-provided content.

Google Drive Upload: Seamlessly save generated PDFs to a “MyResumeCVs” folder in your Drive.

Easy Downloads: Download resume and cover letter PDFs with a simple prompt in Colab.

Robust Error Handling: Try-except blocks provide graceful fallbacks for seamless execution.

## How It Works
User Input: The notebook collects essential details via interactive prompts.

Data Structuring: Inputs are organized into resume and cover_letter dictionaries.

PDF Rendering: Uses reportlab to output clean or styled PDFs with layout control via string drawing and vertical positioning.

Download & Upload Options:

Option to download PDFs directly within the Colab environment.

Optional upload to Google Drive (automatically creates the folder if needed).

## Getting Started
### Prerequisites
Google account (for Google Drive integration)
Basic Python environment via Google Colab

### Libraries:
pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib reportlab pillow
Setup & Run
Open the notebook in Google Colab (or via GitHub).
Install dependencies and run the cells to initialize the input forms.
Provide your details as prompted.
Choose whether to use the fancy layout and upload to Drive.
Generate and download the PDFs.
If enabled, files will also be uploaded to your Google Drive under "MyResumeCVs".

## Usage Example
Run the notebook and input information as prompted:

Name, contact details, summary, education, experience, skills, additional sections.

Cover letter details such as job title, company, greeting, body, and closing.

Choose layout style and upload preferences.

Generated outputs: resume.pdf & cover_letter.pdf

Download or upload the files as needed.

After completion, the notebook confirms both generation and (if selected) upload to Drive.

## Challenges & Solutions
Structured data input in CLI environment -> Loop-based prompts with "Enter to stop" logic make input flexible and organized.

Designing a polished PDF layout -> Used precise y-position tracking and modular section rendering (drawString() methods) in ReportLab.

Google Drive integration -> Authenticated Colab user, checked/created target folder, uploaded files with Drive API.

File download and user experience in Colab -> Employed files.download() and clear prompts for smooth interaction.

Error handling for robustness -> Wrapped critical operations in try-except blocks with helpful fallback messages.

## Contributing
Contributions are welcome! You can help by:
-> Enhancing the PDF design (e.g. fonts, colors, layout)
-> Adding forms (e.g. Colab forms or UI widgets) for cleaner input
-> Integrating AI (e.g. using LLMs to generate summaries from minimal input)
-> Refactoring code for modularity and maintainability
-> Improving user experience and error messaging

Please feel free to fork the project and submit a pull request or open an issue if you’d like to propose a feature or improvement!
