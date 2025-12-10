🚀 Research Assistant – Browser Extension + Spring Boot API  
A lightweight browser extension that lets you summarize any selected text on the web using a local Spring Boot backend, with the option to store summaries for later use.


🧠 Project Overview  
Research Assistant is a dual-layer project consisting of:
1. A Chrome/Browser Extension – Detects selected text and displays summaries inside a side panel UI.
2. A Spring Boot Backend – Processes incoming text and returns structured summarized output.
This tool is designed for developers, students, researchers, and content consumers who need fast, distraction-free text summaries directly while browsing.

🏗️ Project Architecture
<img width="388" height="316" alt="image" src="https://github.com/user-attachments/assets/d2f907d5-9e15-46e2-88e7-bce9cc15490e" />
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/bc7ee58f-98ca-4b73-9ca5-289ad6a64035" />

High-Level Flow
1. User selects any text on a webpage
2. The extension’s content script captures the selection
3. background.js sends it as a POST request to the Spring Boot API
4. Backend performs summarization and returns a JSON response
5. Output is displayed inside sidepanel.html
6. User can optionally save the summary locally

🔄 Data Flow Diagram  
[Webpage Selected Text]
          │
          ▼
   [Content Script]
          │
          ▼
   [Background.js] --> API --> [Spring Boot Controller]
                                │
                                ▼
                         [Summarization Service]
                                │
                                ▼
                     [JSON Response to Extension]
                                │
                                ▼
                       [Sidepanel Summary UI]


✨ Key Features  

⚡ Instant text summarization directly from any webpage
🔗 Browser extension communicating with a local Spring Boot backend
💾 Save summaries for future reference
🎯 Clean, minimal, responsive UI
🔐 Fully local processing (no cloud dependency required)
🧩 Easy to extend with custom AI models or additional tools  

🧰 Tech Stack  
Backend (API)

Java
Spring Boot
REST Controller
MVC Architecture
Maven

Frontend (Extension)  
HTML
CSS
JavaScript
Chrome Manifest v3
Side Panel + Background Service Worker  

📁 Project Folder Structure  
research-assistant/
│── src/main/java/com/research_assistant/
│     ├── ResearchAssistantApplication.java
│     ├── ResearchController.java
│     ├── ResearchService.java
│     ├── ResearchRequest.java
│     └── GeminiResponse.java
│
│── src/main/resources/
│
│── background.js
│── sidepanel.html
│── sidepanel.css
│── sidepanel.js
│── manifest.json
│── pom.xml
│── README.md

👨‍💻 Author

Piyush Pal  
📍 Dewas, Indore, Madhya Pradesh  
📫 thepeeyushyadav0@gmail.com  

🔗 LinkedIn: https://www.linkedin.com/in/piyush-pal-751067306?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app  
📸 Instagram: https://www.instagram.com/thepeeyushyadav?igsh=dW9tYmp4czgya2hj  
🎥 YouTube (ThinkCodeX): https://youtube.com/@thinkcodex?si=2kfSX2hmIxPrKudl 
