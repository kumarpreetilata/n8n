# Email Classification and Scheduling Workflow

## Overview
This workflow automates the classification, summarization, and scheduling of emails using n8n. It integrates Gmail, Groq AI models, and Google Calendar to streamline email processing and event scheduling.

## Workflow Steps

### 1. **Gmail Trigger**
- The workflow starts when a new email is received in Gmail.
- The trigger captures the sender's details, subject, and email body.

### 2. **Condition Check (IF Node)**
- The email content is analyzed to determine the next step.
- If the email meets certain criteria (e.g., scheduling required), it proceeds to event creation; otherwise, it moves to classification.

### 3. **AI-Powered Email Classification**
- The AI Agent (Groq Chat Model) processes the email content and classifies it into one of three categories:
  - **Urgent**
  - **Follow Up**
  - **General**
- The AI model also extracts the sender’s details, summarizes long emails, and suggests a refined subject if necessary.

### 4. **Handling Classification Results**
- If the email requires a follow-up, an automated response is generated and sent using Gmail.
- If scheduling is required, the workflow proceeds to the next step.

### 5. **Event Creation in Google Calendar**
- If the email content indicates a meeting request, the AI Agent extracts relevant details.
- A structured event is created in Google Calendar with extracted information such as date, time, and description.

### 6. **Structured Output Parsing**
- The email classification results and scheduling details are parsed into a structured JSON format.
- This output can be further used for logging or integrations.

## Features
- **Automated Email Categorization:** Uses AI to classify emails into relevant categories.
- **Intelligent Summarization:** Extracts key information from lengthy emails.
- **Smart Subject Refinement:** Generates a clearer subject line if needed.
- **Automated Scheduling:** Creates Google Calendar events based on email content.
- **Follow-up Email Automation:** Sends appropriate responses based on classification.

## Usage
1. Ensure that your Gmail account is connected and has appropriate permissions.
2. Configure the AI Agent to optimize email classification.
3. Adjust the IF condition logic to refine when events should be scheduled.
4. Review structured output logs for insights into email handling.

## Technologies Used
- **n8n** for workflow automation
- **Gmail API** for email processing
- **Groq AI Chat Model** for email classification
- **Google Calendar API** for event scheduling

This workflow enhances productivity by automating repetitive email handling tasks while ensuring that urgent communications and scheduling needs are efficiently managed.

