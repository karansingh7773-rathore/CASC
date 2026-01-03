## CASC: The Contextual-Aware Security Cam 
CASC isn't just another security camera; it's an intelligent security analyst. While traditional systems just show you a video feed, CASC watches the feed, understands what's happening, and describes it to you in plain English. It transforms your security camera from a passive recorder into an active, conversational security partner.

some commits may not work on your machine

This system goes beyond simple motion alerts by analyzing the context of an event, allowing you to get immediate, detailed insights and even ask follow-up questions.

# What Makes CASC Different?
The problem with most security systems is "alert fatigue"—endless notifications for meaningless events like a cat walking by or a tree branch swaying. CASC solves this by focusing on what matters.

From Motion to Meaning: Instead of just detecting motion, CASC analyzes the frame to understand who is there and what they are doing.

From Video to Vocabulary: It translates complex visual data into a simple, natural language summary. Instead of scrubbing through video, you get an instant report: "An unknown male, appearing to be in his late 20s, was detected near the main door."

From Passive to Interactive: You can ask questions about any security event. Get immediate answers like "Was a person detected?" or "What was their estimated age?" without ever touching the video timeline.

# Key Features
Intelligent Motion Triggering: Uses OpenCV to filter out insignificant movements and only trigger analysis when something important happens.

Advanced Facial & Attribute Analysis: Leverages the powerful DeepFace library to perform deep analysis on detected faces, identifying:

Identity: Recognizes known individuals from a managed database.

Emotion: Detects the emotional state (e.g., happy, neutral, angry).

Age & Gender: Estimates the age and gender of individuals.

Conversational Security Interface: Powered by state-of-the-art LLMs via OpenRouter, it generates human-like summaries and allows for interactive Q&A about security events.

Robust Event Storage: All event data, including summaries, images, and conversations, are stored and indexed in Azure Cosmos DB for reliable, high-speed retrieval.

# Real-World Impact
CASC is more than a technical project; it's a blueprint for the future of accessible security and environmental awareness.

For Home Security: Drastically reduces false alarms and gives homeowners immediate, understandable context during a potential break-in, allowing for faster, more informed decisions.

For Small Businesses: Can provide insights into customer demographics (age, gender) at storefronts or monitor sensitive areas after hours with a higher degree of intelligence.

For Workplace Safety: Can be adapted to monitor restricted zones, ensuring only authorized personnel are present and providing a detailed log of all activity.

# Powerful Technology Stack
This project is built on a foundation of cutting-edge, industry-standard tools:

Backend: Python

Computer Vision: OpenCV

Facial Analysis: DeepFace

Language Models: Various models via OpenRouter (e.g., Llama 3, Gemma)

Database: Microsoft Azure Cosmos DB (NoSQL)

# Setup
1. Install Dependencies
``` Bash

pip install -r requirements.txt
```
2. Configure Credentials
Edit config/config.yaml and add your API keys for OpenRouter and Azure Cosmos DB.

3. Test Your Setup
It is highly recommended to run the connection tests to ensure all services are configured correctly.

Run a full system check:

``` Bash

python test_connections.py
```
Test individual components:

``` Bash

python test_openrouter.py
```
python test_database.py
python test_deepface.py
4. Run the Application
Bash

python src/main.py
