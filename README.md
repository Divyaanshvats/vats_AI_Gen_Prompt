# vats_AI_Gen_Prompt
AI-powered Student Performance Feedback System

# Student Feedback Report Generator

This project generates personalized PDF feedback reports for student test performance using AI-powered analysis and visualization.

---

## API Used

- **GroqCloud LLM API** (`llama3-8b-8192` model)  
  I used GroqCloud’s large language model to generate detailed, natural feedback based on student scores and accuracy.  
  > _Note: We chose GroqCloud because it offers more features and better performance compared to the free tiers of OpenAI, Claude, and Gemini, which have limitations on usage and features._

---

## How the Prompt Works

The prompt sends the AI the student’s subject-wise scores, accuracy, and time taken. It asks the AI to:

- Analyze performance per subject, noting trends in scores, accuracy, and time management.  
- Identify strengths and weaknesses clearly.  
- Explain if the student managed time well or rushed.  
- Suggest 2–3 actionable, personalized improvement steps for each subject.  
- End with an encouraging and motivational message.

This helps generate human-like, insightful feedback that feels personal and helpful.

---

## Report Structure

Each PDF report contains:

1. **Performance Summary**  
   - Total score and average accuracy for all subjects.

2. **Personalized Feedback**  
   - Detailed subject-wise analysis from the AI including observations and suggestions.

3. **Visual Plot**  
   - A bar chart showing accuracy percentage across subjects for quick visual insight.

---

## How the Code Works

1. **Load JSON Data**  
   Reads student test data from JSON files.(The 3rd and 4th JSON File are the same but still taken both)

2. **Extract Summary**  
   Pulls out key info: subject names, scores, accuracy, and time taken.

3. **Generate AI Feedback**  
   Sends the summarized data and overall stats to GroqCloud’s LLM with a carefully designed prompt. The AI returns human-like feedback text.

4. **Clean Feedback Text**  
   Fixes any encoding issues so the PDF looks clean and professional.

5. **Plot Accuracy Chart**  
   Creates a visual bar chart of accuracy by subject using seaborn and matplotlib.

6. **Create PDF Report**  
   Uses FPDF to put together the report: header, performance summary, AI feedback, and the accuracy plot.

7. **Process Multiple Files & Zip**  
   Runs the above steps for multiple student files, generates PDFs, and bundles them into a zip file for easy download and sharing.

---

## Why GroqCloud?

- OpenAI, Claude, and Gemini are great but mostly paid and limited in free usage.  
- Some features you need (like longer context windows or certain models) aren’t fully available in their free tiers.  
- GroqCloud offers a powerful `llama3-8b-8192` model with a better mix of features and cost-effectiveness for this project.

---
**So that was my project, THANK YOU**
