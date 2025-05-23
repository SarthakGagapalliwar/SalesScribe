 
## 🛒🛍️ SalesScribe AI
Cold email generator for services company using groq, langchain and streamlit. It allows users to input the URL of a company's careers page. The tool then extracts job listings from that page and generates personalized cold emails. These emails include relevant portfolio links sourced from a vector database, based on the specific job descriptions. 
**Imagine a scenario:** 🔗 [Website-Link](http://65.2.6.179:8501/)

- A company needs a Principal Software Engineer and is spending time and resources in the hiring process, on boarding, training etc
- SalesScribe is Software Development company can provide a dedicated software development engineer to company. So, the business development executive (Sarthak) from SalesScribe is going to reach out to Nike via a cold email.

## Demo Video
 https://github.com/user-attachments/assets/46e04360-2a49-4ff2-ab52-f4c804a97c23/ 


![img.png](images/DemoImg.png)

## AWS Architecture
![img.png](images/SalesScribe.png)

## Workflow Diagram
![img.png](images/architecture.png)

## Set-up
1. To get started we first need to get an API_KEY from here: https://console.groq.com/keys. Inside `app/.env` update the value of `GROQ_API_KEY` with the API_KEY you created. 

2. Clone the Project via Git

   Option 1: Clone via Git
   ```bash
   git clone https://github.com/SarthakGagapalliwar/SalesScribe.git
   ```

   Option 2: Clone via Docker Image
   ```commandline
   docker pull sarthak5109/salesscribe-ai

    ```
       
4. To get started, first install the dependencies using:
    ```commandline
     pip install -r requirements.txt
    ```
   
5. Run the streamlit app hi:
   ```commandline
   streamlit run app/main.py
   ```
