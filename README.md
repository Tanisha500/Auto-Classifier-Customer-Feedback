# Auto-Classifier-Customer-Feedback

This project is a low-code automation built with **n8n** that reads customer feedback from **Google Sheets**, classifies each entry as **Positive**, **Negative**, or **Neutral**, and appends a **summary and sentiment** using a large language model via the **Groq API**.


##  Use Case

> Automatically analyze large volumes of customer reviews and classify them using an AI model — saving hours of manual effort.


##  Tools & Technologies

- **n8n** – Visual workflow automation tool
- **Groq API** – To access LLMs like LLaMA
- **Google Sheets** – Source and destination for feedback
- **Function & Set Nodes** – For prompt creation and result formatting


##  Workflow Overview

> Reads → Classifies → Extracts Sentiment → Updates Sheet

###  Workflow Steps

1. **Execute Workflow Manually**
   - Triggers the process when you click "Execute" in n8n

2. **Google Sheets - Read**
   - Pulls raw feedback from a connected Google Sheet

3. **Function Node**
   - Formats each row into a structured prompt for sentiment classification

4. **Groq API - Classify**
   - Sends feedback to a Groq LLM to detect sentiment and generate a brief summary

5. **Extract Sentiment & Summary**
   - Extracts only the classification and summary from the AI's response

6. **Set Node - Format Output**
   - Prepares fields to write back into the original sheet

7. **Update Google Sheet**
   - Updates each row with sentiment label and AI-generated summary


##  Workflow Screenshot

<img width="1472" height="284" alt="Screenshot 2025-07-13 211449" src="https://github.com/user-attachments/assets/76090cbd-5f28-4884-adc9-acb9477d97d8" />


##  Google Sheet Output

<img width="928" height="194" alt="Screenshot 2025-07-13 214511" src="https://github.com/user-attachments/assets/8735144a-7788-479d-a91b-440a7d3b861d" />
