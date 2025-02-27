# MEDIBOT-SOCIAL HEALTH INSURANCE CHATBOT PROJECT
![_Mastering the Art of Storytelling_ Tips for Aspiring Writers 📖_](https://github.com/user-attachments/assets/602c7177-7c69-4073-83ba-ebec3aaf2f96)


This project uses sentiment analysis of Twitter data, combined with the FAQ on SHA and the SHA Act, to understand public views on the Social Health Authority (SHA) and its Social Health Insurance Fund (SHIF). MediBot, a medical chatbot, simplifies SHA regulations, enhances engagement, and drives informed decisions in Kenya’s healthcare landscape.

## Overview
The introduction of Social Health Authority(SHA) as a replacement of National Health Insurance Fund(NHIF) has caused confusion among Kenyans due to a lack of clear, timely and accessible information.
This has led to misinformation, low enrollment and difficulties in registration and claims. As a result, customer service centers are overwhelmed, healthcare access is delayed, and trust in the new scheme is declining.

## Objectives
- Develop an AI Chatbot aimed at promoting understandingand increased adoption of SHA in the country by providing accurate, instant and accessible information about the
scheme.
- Implement an NLP model to understand about the scheme eligibility, benefits, contributions, claim procedures and the enrollment process.
- Implement and deploy a web-based chatbot that ensures user interactivity.
- Develop an accurate chatbot model that closes SHA’s info gap, supporting with timely, clear healthcare details efficiently.

  
## Data Source 
[Social Health Insurance (General) Regulations, 2023](https://www.health.go.ke/sites/default/files/2023-11/SOCIAL%20HEALTH%20INSURANCE%20%28GENERAL%29%20REGULATIONS%20%2C2023.pdf)

[SHA FAQ's](http://localhost:8888/files/data/Frequently-Asked-Questions-FAQs-on-Social-Health-Authority-SHA-.pdf)

## Data Understanding
Data cleaning removed duplicates, handled missing values, and normalized text (e.g., lowercase, tokenization). Preprocessing prepared Twitter and SHA data for modeling, focusing on intents, entities, and sentiment. Analysis revealed public frustration with SHA/SHIF, with frequent terms like “failing,” “scam,” and “dying,” and sentiment showing 350 negative, 150 neutral, and 50 positive tweets, indicating a need to address dissatisfaction.

## Data Visuaization
The following three visualizations are used:
- Sentiment Analysis – Categorizes tweets into negative, neutral, and positive sentiments.
  

  ![PHOTO-2025-02-26-20-33-31 (2)](https://github.com/user-attachments/assets/493e3604-f0d4-41c8-8321-04b25d519ec7)
  

- Tweet Volume Over Time – Tracks tweet activity from October 2024 to February 2025, showing fluctuations in public engagement based on SHA-related events or announcements.
  

  ![PHOTO-2025-02-26-20-33-32 (3)](https://github.com/user-attachments/assets/051527f5-67c2-4a2f-9b6d-9909eb0c0e56)
  

- Word Cloud – Shows the most frequent terms, with negative words like “failing,” “scam,” indicating frustration, while “working” and “great” suggest some positive sentiment.
  

  ![PHOTO-2025-02-26-20-33-32 (1)](https://github.com/user-attachments/assets/c9b5d56b-db41-4632-b9e6-69d726b43314)
  

## Modeling
- XGBoost
  Processes structured data to predict user intents but low accuracy(approximately 65%) in intent recognition.
- BERT Model
  Performs well in understanding text semantics, achieving high accuracy(approximately 85%), but faces computational challenges. Its deep architecture causes slow response 
  times (2–3 seconds per query), making it unsuitable for realtime conversations.
- RASA Model
  Integrates NLU and dialogue management, achieving high accuracy (approximately 88%) and fast response times (under 0.5 seconds per query).

## Model Comparison
RASA excels with 88% accuracy, fast response times (under 0.5 seconds), and built-in dialogue management. It is selected as the best option for SHA’s chatbot due to its efficiency, speed, and conversational capabilities, ensuring smooth and responsive interactions.

## Deployment
Flask was chosen for its simple architecture and flexibility, providing fast response times, enabling RESTful API integration for seamless connectivity with SHA’s digital platforms, and offering scalability to efficiently handle user interactions.

## Conclusion
The SHA chatbot project successfully integrates RASA for natural languageunderstanding and dialogue management, ensuring efficient, real-time userinteractions.
Deployed via Flask, the chatbot provides seamless accessibility through SHA’s digitalplatforms while maintaining security and compliance with regulatory requirements.

## Recommendations
- Continuously refine the chatbot’s training data to improve intent recognition and entity extraction.
- Implement real-time monitoring and feedback mechanisms to enhance response accuracy.
- Expand deployment channels to include SMS and WhatsApp for broader accessibility.

## Next Steps
- Conduct user testing to evaluate chatbot performance and refine responses based on feedback. User testing engages SHA users (e.g., beneficiaries, staff) to assess the RASA chatbot’s accuracy,speed, and conversation flow. Feedback on response clarity and relevance helps refine intentrecognition and dialogue, ensuring alignment with SHA’s needs.

- Automate dataset updates to incorporate evolving SHA policies and user concerns. Automating updates keeps the chatbot current by integrating new SHA policies (e.g., eligibilitychanges) and user concerns (e.g., funding issues) from sources like X and news, maintainingaccuracy and relevance over time.

