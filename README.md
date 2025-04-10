
# Research Paper Summarization Multi-Agent System

This project is a multi-agent system designed to help researchers stay updated on research across multiple fields by summarizing relevant research papers and converting them into accessible audio summaries. The system can search for papers, process them, classify topics, generate summaries, synthesize information across multiple papers, and convert summaries into audio podcasts.

## Features

1. **Search for Research Papers**: Search academic repositories like arXiv, Google Scholar (or others in the future) based on user-defined topics.
2. **File Uploads**: Accepts academic papers in PDF format for processing.
3. **Topic Classification**: Classifies papers into topics provided by the user.
4. **Summary Generation**: Uses Hugging Face transformers to generate paper summaries.
5. **Cross-paper Synthesis**: Generates a synthesized summary based on multiple papers.
6. **Audio Generation**: Converts the generated summaries into an audio format using gTTS.

## Setup Instructions

### Prerequisites

1. Python 3.8 or later
2. Install required packages:
```bash
!pip install requests beautifulsoup4 transformers gTTS scholarly PyPDF2
```

### Run the Code in colab

## System Architecture

- **Paper Search**: Uses web scraping (BeautifulSoup, requests) to fetch data from academic sources like arXiv and Google Scholar.
- **Topic Classification**: Uses Hugging Face's zero-shot classification model to classify paper topics based on a user-defined list.
- **Text Summarization**: BART transformer model is used to summarize research papers.
- **Audio Conversion**: Converts the textual summary into an audio file using gTTS.

## Paper Processing Methodology

- **Text Extraction**: Extracts text from PDFs using the `PyPDF2` library.
- **Web Scraping**: Fetches paper metadata from repositories like arXiv using BeautifulSoup and requests.
- **DOI Handling**: Extracts DOI references from paper links and summaries.

## Audio Generation Implementation

- **gTTS**: Text-to-Speech conversion is done using the Google Text-to-Speech (gTTS) API.

## Limitations and Future Improvements

- Currently, only arXiv and Google Scholar are supported for paper searches.
- Audio generation might be slow for large summaries.
- Further integration with more academic repositories is planned.
