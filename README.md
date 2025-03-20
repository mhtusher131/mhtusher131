## Hi there 👋

<!--
**mhtusher131/mhtusher131** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
**import os

def generate_readme(name, title, location, linkedin, github, skills, projects, publications, achievements):
    readme_content = f"""
# Hi there, I'm {name} 👋

## 💻 Junior Software Engineer | {location}

[![LinkedIn](https://img.shields.io/badge/LinkedIn-{linkedin.split('/')[-1]}-blue)]({linkedin})
[![GitHub](https://img.shields.io/badge/GitHub-{github.split('/')[-1]}-black)]({github})

---

## 🚀 Skills & Technologies

- **Programming Languages:** {', '.join(skills['languages'])}
- **Libraries & Tools:** {', '.join(skills['tools'])}
- **Architecture & Methodologies:** {', '.join(skills['architecture'])}
- **Problem Solving:** {', '.join(skills['problem_solving'])}

---

## 📌 Projects

"""
    for project in projects:
        readme_content += f"- **{project['name']}**\n  - {project['description']}\n"
    
    readme_content += """
---

## 📚 Publications

"""
    for pub in publications:
        readme_content += f"- [{pub['title']}]({pub['link']})\n"
    
    readme_content += """
---

## 🏅 Achievements & Extracurricular Activities

"""
    for achievement in achievements:
        readme_content += f"- {achievement}\n"

    with open("README.md", "w") as file:
        file.write(readme_content)

    print("✅ README.md generated successfully!")

# User details from the resume
name = "Md Mahamudul Hasan"
title = "Junior Software Engineer"
location = "Dhaka, Bangladesh"
linkedin = "https://www.linkedin.com/in/mhtusher131"
github = "https://github.com/mhtusher131"

skills = {
    "languages": ["Python", "JavaScript", "SQL", "HTML", "CSS"],
    "tools": ["Django", "Ajax", "Tailwind", "Git", "MySQL", "REST APIs"],
    "architecture": ["Agile", "DevOps", "ITSM", "ITIL4"],
    "problem_solving": ["DSA", "LeetCode", "Competitive Programming"]
}

projects = [
    {"name": "Bangla License Plate Recognition", "description": "Developed CNN model for Bengali character recognition with 85% accuracy using GFPGAN and morphological processing."},
    {"name": "Bangla Text Summarization", "description": "Built a deep learning Seq2seq and T5 transformer model for abstractive Bangla text summarization."},
    {"name": "To-Do Application", "description": "Developed a Django-based task management app with user authentication, CRUD, filtering, and due date tracking."}
]

publications = [
    {"title": "Bengali License Plate Recognition: Unveiling Clarity with CNN and GFPGAN", "link": "https://ieeexplore.ieee.org/document/10441040"},
    {"title": "Advancing Abstractive Bangla Text Summarization: A Deep Learning Approach Using Seq2seq Encoder-Decoder Model and T5 Transformer", "link": "https://ieeexplore.ieee.org/document/10464712"}
]

achievements = [
    "Solved 200+ problems on LeetCode and Codeforces.",
    "Active member of AUST Innovation & Design Club, contributing to hackathons and team projects.",
    "Published 2 IEEE papers on Bengali NLP & OCR technologies."
]

# Generate the README file
generate_readme(name, title, location, linkedin, github, skills, projects, publications, achievements)
**
