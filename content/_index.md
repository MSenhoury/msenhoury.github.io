---
# Leave the homepage title empty to use the site title
title: ""
date: 2025-03-02
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Display your profile (set in `content/authors/`)
      username: admin
      text: "Data Scientist | Generative AI & NLP Specialist | AI-Driven Automation"
      # Call-to-action button for CV download
      button:
        text: Download CV
        url: uploads/Mohamed_Senhoury_CV.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  - block: markdown
    content:
      title: '🚀 About Me'
      subtitle: ''
      text: |-
        Passionate about **Artificial Intelligence, Natural Language Processing (NLP), and Machine Learning**, I specialize in **developing AI-driven applications** with **LLMs, Chatbots, and Data Science solutions**.

        With hands-on experience in **Generative AI, Python, LangChain, Hugging Face, and SQL**, I love solving real-world problems through technology.

        I'm open to **collaborations, consulting, and new opportunities in AI & Data Science**. Let's connect! 📩
    design:
      columns: '1'

  - block: collection
    id: projects
    content:
      title: AI & Data Science Projects
      text: "Explore some of my recent projects in NLP, Machine Learning, and AI-driven applications."
      filters:
        folders:
          - project
    design:
      view: card
      columns: 2

  - block: collection
    id: tutorials
    content:
      title: Learn AI & Data Science
      text: "I create educational content to help others understand AI, NLP, and Data Science. Explore my tutorials!"
      filters:
        folders:
          - tutorials
    design:
      view: article-grid
      columns: 2

  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      text: "I speak at AI & Data Science conferences, sharing insights on Generative AI, NLP, and automation."
      filters:
        folders:
          - event
    design:
      view: article-grid
      columns: 1

  - block: collection
    id: news
    content:
      title: Latest Blog Posts
      subtitle: ''
      text: 'Stay updated with my latest articles on AI, Data Science, and NLP.'
      page_type: post
      count: 5
      filters:
        exclude_featured: false
        exclude_future: false
        exclude_past: false
    design:
      view: date-title-summary
      spacing:
        padding: [0, 0, 0, 0]

  - block: cta-card
    content:
      title: "📬 Let's Connect!"
      text: |-
        I'm always excited to discuss AI, NLP, and Data Science! If you're interested in **collaborations, projects, or just a tech chat**, feel free to reach out.

        📩 **Email:** [m.asenhoury@hotmail.com](mailto:m.asenhoury@hotmail.com)  
        💼 **LinkedIn:** [linkedin.com/in/mohamed-senhoury](https://www.linkedin.com/in/mohamed-senhoury)  
        🧑‍💻 **GitHub:** [github.com/mohamed-senhoury](https://github.com/mohamed-senhoury)  

      button:
        text: Contact Me
        url: mailto:m.asenhoury@hotmail.com
    design:
      card:
        css_class: "bg-primary-700"
