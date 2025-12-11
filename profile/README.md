# 🏠 HomeQuest
>25-2 Hanyang University Software Engineering Project
---

## 📌 Project Proposal

   This study addresses the limitations of current smart home services, which primarily provide data and rely on users to take action on their own, making it difficult to promote sustained behavioral change and interaction within the family. To overcome this issue, we propose a family-centered AI challenge system that uses IoT data to deliver personalized behavioral goals and real-time feedback.
 
   The system integrates data from LG ThinQ devices to generate tailored challenges in household chores, energy saving, and wellness, while visualizing each member’s progress through a character-based interface that promotes participation. Users earn points by completing challenges and can view family rankings, and the accumulated data enables the AI to analyze daily patterns and offer targeted insights.
 
   By transforming everyday data into a game-like, immersive experience, the system enhances engagement and achievement within the household and shifts the smart home from an efficiency-focused model to an interactive environment that supports family connection and positive routines.

## 🔧 Architecture Design
<img width="1730" height="965" alt="Slide 16_9 - 5 (1)" src="https://github.com/user-attachments/assets/01d3adf2-d6b8-4710-a8fd-006e2ffed417" />

> - LG ThinQ devices send **appliance usage logs** to Firebase.  
> - These logs are merged with **user & family activity data** from the app and preprocessed on the server.  
> - The processed data is passed to the ML server (FastAPI), where a GBDT model predicts **which user is most likely to complete which challenge**.  
> - Predictions are written back to Firebase and displayed in the app as **personalized challenge recommendations**.  
> - Challenge completions and point updates are stored in Firestore and used for **family rankings, rewards, and marketplace recommendations**.  
> - Activity logs are periodically sent to the OpenAI API to generate **AI weekly reports** (feedback, summary, next-step suggestions).  
> - All accumulated logs contribute to **long-term behavior modeling** and iterative model improvements.


## 🎥 Demo Videos
[![HomeQuest Demo Video](https://img.youtube.com/vi/wRn-Hax9f6s/maxresdefault.jpg)](https://youtu.be/wRn-Hax9f6s)

## Links
Presentation: [HomeQuest Presentation (Miricanvas)](https://www.miricanvas.com/v2/design2/v/1ef211b9-0cb5-4282-abcc-dcda5527c263)
[Uploading CSE_PublicPPT.pdf…]()


Documentation: [HomeQuest.pdf](https://github.com/user-attachments/files/24101862/HomeQuest.pdf)


## 👥 Team Members
| Name | Organization | Email |
|------|-------------|--------|
| Hyeonseo Shim | Department of Information Systems, Hanyang University | hyeonseo321@gmail.com |
| Sihyun Jang | Department of Information Systems, Hanyang University | jjj99nine2@hanyang.ac.kr |
| Jin Yun | Department of Information Systems, Hanyang University | jinijini0402@hanyang.ac.kr |
| Yeonsoo cho | Department of Public Administration, Hanyang University | meriel1010@hanyang.ac.kr |


