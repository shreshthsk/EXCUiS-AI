# Excuis AI 🤖🍽️  
**Recipe Generator Chatbot Using AI (with Optional Regional Inputs)**

Excuis AI is a two-phase academic project that builds a chatbot capable of generating Indian and global recipes based on user input. Users can either directly name a dish or specify a region to retrieve relevant recipes. It combines NLP, vector similarity search, and structured data engineering to build a functional, conversational recipe retriever.

---

## 🔍 Overview

This chatbot is designed to **generate recipes**, not recommend dishes.  
Users can interact in two primary ways:
- **By Dish Name** → "Tell me how to make Biryani"
- **By Region** → "Give me something from Kerala"

The system uses FAISS to match user queries with preprocessed recipe embeddings and responds with a complete recipe using a local language model.

---

## 🧱 Project Structure

### 📦 Phase 1: Data Preparation

| Folder                         | Description |
|--------------------------------|-------------|
| `1_Data_Retrieval/`           | Web scraping using BeautifulSoup & Playwright from recipe websites (Tarla Dalal, AllRecipes, etc.) |
| `2_Data_Cleaning_Processing/` | Ingredient normalization, synonym reduction, and standard formatting |
| `3_Exploratory_Data_Analysis/`| Basic flavor distribution analysis done using Python libraries like `seaborn` and `matplotlib` |
| `4_Flavor_Mapping/`           | Constructed ingredient-to-taste profile mappings using text mining sources like *The Flavor Bible* |
| `5_Hypothesis_Testing/`       | Tested regional variation hypotheses based on ingredient frequency and flavor categories |

### 🤖 Phase 2: Chatbot Development

| Folder                         | Description |
|--------------------------------|-------------|
| `1_Feature_Engineering/`      | Ingredient-taste mappings and feature extraction |
| `2_Data_Processing/`          | Data formatting for FAISS and LLM compatibility |
| `3_Chatbot_Development/`      | Recipe generation based on user input (dish name or region) using FAISS + Mistral LLM |

---
```
Excuis-AI/
├── LICENSE
├── README.md
├── Demo/
│   └── chatbot_demo.mp4
├── Docs/
│   ├── ExcuisAI_Project_Presentation.mp4
│   ├── ExcuisAI_Project_Report.pdf
│   └── ExcuisAI_Future_Blueprint.mp4
├── Phase-1_Data_Preparation/
│   ├── 1_Data_Retrieval/
│   ├── 2_Data_Cleaning_Processing/
│   ├── 3_Exploratory_Data_Analysis/
│   ├── 4_Flavor_Mapping/
│   └── 5_Hypothesis_Testing/
└── Phase-2_Modeling_and_Chatbot/
    ├── 1_Feature_Engineering/
    ├── 2_Data_Processing/
    └── 3_Chatbot_Development/
```

## 💬 Demo

🎥 [Watch the Chatbot Demo](./Demo/chatbot_demo.mp4)

**Example 1:**  
> *"How do I make Paneer Butter Masala?"*  
Bot: *Returns full recipe with ingredients and instructions.*

**Example 2:**  
> *"Give me a traditional dish from Gujarat."*  
Bot: *Returns a dish like Dhokla, with its recipe.*

> 🔎 The chatbot works with both **dish name-based** and **region-based** queries.

---

## 📚 Project Documentation

- 🎥 [Excuis AI – Final Project Presentation](./Docs/ExcuisAI_Project_Presentation.mp4)
- 📄 [Excuis AI – Full Project Report (PDF)](./Docs/ExcuisAI_Project_Report.pdf)

These documents cover both the development process and final insights for the Excuis AI chatbot project.


## 🚀 Future Enhancements

- Add a frontend interface (e.g., Streamlit or React) for better user interaction
- Enable multi-turn conversations and user context handling
- Incorporate user feedback for more personalized recipe suggestions
- Expand dataset to include global cuisines and fusion recipes

🎥 **Blueprint Video:** [Watch the Excuis AI Vision Demo](./Docs/ExcuisAI_Future_Blueprint.mp4)

This video illustrates the intended future state of Excuis AI, including UI ideas, interactive flow, and chatbot enhancements.

---

## 🧠 Tech Stack

- **Languages:** Python  
- **Libraries:** BeautifulSoup, Playwright, FAISS, scikit-learn, matplotlib, seaborn  
- **Models:** Agglomerative Clustering, NLP Preprocessing  
- **Tools:** Google Colab, Jupyter Notebooks, Local LLM (Mistral)

---

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](./LICENSE) file for details.

Open for academic and educational purposes. You are allowed to use, modify, and distribute this code under the terms of the Apache 2.0 License.


## 🙏 Acknowledgments

Developed as part of my M.Tech dissertation at the School of Data Science and Forecasting, DAVV (2025).
