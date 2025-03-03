---
# Leave the homepage title empty to use the site title
title: "Mohamed SENHOURY"
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: static/uploads/resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  - block: markdown
    content:
      title: '🚀 My Work in AI & Data Science'
      subtitle: ''
      text: |-
        I specialize in **Artificial Intelligence, NLP, and Data Science**, with a strong focus on **Generative AI, Large Language Models (LLMs), and automation**.

        My expertise includes:
        - 🔹 **Natural Language Processing (NLP)**: Chatbots, Sentiment Analysis, Named Entity Recognition  
        - 🔹 **Generative AI & LLMs**: Fine-tuning GPT, LangChain, Hugging Face Transformers  
        - 🔹 **Data Science & Analytics**: Data visualization, SQL, Machine Learning  

        I'm passionate about **solving complex problems with AI** and constantly explore **new ways to optimize AI-driven automation**.

        If you're interested in **collaborating on AI projects**, feel free to reach out! 📩

  - block: collection
    id: projects
    content:
      title: AI & Data Science Projects
      text: "Explore my AI & NLP projects, including sentiment analysis, chatbots, and automation."
      filters:
        folders:
          - project
    design:
      view: citation

  - block: markdown
    content:
      title: "📝 Sentiment Analysis Model"
      text: |-
        This project is a **Machine Learning & Deep Learning-based Sentiment Analysis model** designed to classify tweets as **positive or negative**.

        **Key Features:**
        - **Preprocessing**: Tokenization, stopword removal, stemming
        - **Feature Engineering**: TF-IDF vectorization
        - **Models Trained**: Naïve Bayes, SVM, Logistic Regression, and TensorFlow-based Deep Learning
        - **Performance Metrics**: Accuracy, Confusion Matrix, Classification Report

        📊 **Dataset:** Processed tweets with labeled sentiment  
        🏆 **Best Performing Model:** SVM with TF-IDF  
        🚀 **Use Case:** Social media sentiment analysis for brand monitoring  

        📥 **Download the Jupyter Notebook Below!**
      button:
        text: "Download Sentiment Analysis Notebook"
        url: "https://github.com/MSenhoury/Sentiment-Analysis"
      image:
        filename: sentiment-analysis.jpg
        caption: "AI-based Sentiment Analysis using NLP & Machine Learning"

  - block: markdown
    content:
      title: "🎤 My Talk at BIG DATA & AI 2022"
      text: |-
        I presented my **AI Model from Clini'IA** at the **BIG DATA & AI 2022** conference. My work focused on **building an NLP model for intelligent data processing**, showcasing how AI can optimize decision-making in large-scale data environments.

        🔹 **Project Highlights:**
        - Fine-tuning **BERT-based NLP models** for structured data processing
        - AI-driven **automation for medical and industrial applications**
        - Performance benchmarking against traditional NLP solutions

        📢 **Want to learn more? Click below!**
      button:
        text: "Read More About My Talk"
        url: "https://msenhoury.github.io/talks"
      image:
        filename: big-data-ai-2022.jpg
        caption: "Presenting my NLP model at BIG DATA & AI 2022"

  - block: markdown
    content:
      title: "💻 Explore More on GitHub"
      text: |-
        If you're interested in my AI projects, check out my **GitHub repository** where I share open-source implementations of **NLP models, AI automation, and Data Science solutions**.

        🔹 **Recent Projects:**
        - [Document Processing and Summarization System](https://github.com/MSenhoury/document-processing-summarization)
        - [Chatbot](https://github.com/MSenhoury/Chatbot)
      

        **Follow my work on GitHub and contribute!**
      button:
        text: "View My GitHub"
        url: "https://github.com/mohamed-senhoury"

---
