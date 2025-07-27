# AWS Bedrock-Powered LLM Applications: Blog Generation & QA Chatbot

This repository showcases two production-ready applications leveraging Amazon Bedrock:

1. **Blog Generator** - Uses Claude via Bedrock and AWS Lambda to generate 200-word blogs on a given topic and save the output to an S3 bucket.
2. **QA Chatbot on PDFs** - A Streamlit web app that enables users to query uploaded PDFs using a Retrieval-based QA pipeline powered by FAISS and Titan Embeddings from Bedrock.

---

## 🚀 Features

### ✍️ Blog Generator using Lambda + Bedrock
- Uses `anthropic.claude-v2:1` to generate blogs on custom topics.
- Triggered via an AWS Lambda function.
- Blog content is stored in an S3 bucket (`aws_bedrock_course1`) for persistence.

### 📚 QA Chatbot for PDF using Bedrock
- Ingests PDFs from the `/data` folder.
- Splits and indexes content using LangChain + FAISS.
- Embedding powered by `amazon.titan-embed-text-v2:0` via Bedrock.
- Answers user questions with contextually relevant, detailed responses using `anthropic.claude-v2:1`.

---

## 📁 Project Structure

AWS-Bedrock-LLM-Apps/
├──Amazon BedRock/                        # QA chatbot using Bedrock + Streamlit
│   ├── aws_bedrock-app.py
│   ├── data/                          # Folder to store PDFs
│   ├── faiss_index/                   # Auto-generated FAISS index
│   └── requirements.txt               # Dependencies for Streamlit app
│
├──aws_Lambda/            # Blog generator using Bedrock + Lambda
│   ├── app.py                         # Lambda-compatible script
│   ├── requirements.txt
