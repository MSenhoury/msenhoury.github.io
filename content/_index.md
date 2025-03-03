---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within content/authors/)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/CV_2025_EN.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to assets/media/.
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
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
---