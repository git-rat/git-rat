# Hi there 👋 I'm Rathika

I'm an engineering student passionate about problem-solving and software development. I'm currently learning Java and Dart while working on projects that enhance my understanding of algorithms and system design.

## 🚀 Skills & Interests
- Programming Languages: Java, Dart, Python, C
- Interests: LeetCode problem-solving, Flutter app development, system design
- Currently Learning: Dart & Flutter

## 📫 Connect with Me
- **GitHub**: [yolorat](https://github.com/yolorat)
- **LeetCode**: [rat_for_code](https://leetcode.com/rat_for_code/)
- **LinkedIn**: [Rathika C](https://www.linkedin.com/in/rathika-c-34461a244/)

## 🔭 Projects
- **Crop Health Management**: A computer vision project leveraging Keras for plant disease detection.

- # GitHub Snake Animation Workflow
# This will generate and update a snake animation in your profile README

name: GitHub Snake Game

on:
  schedule:
    - cron: "0 0 * * *"  # Runs daily at midnight UTC
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Generate GitHub Contributions Snake Animations
        uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
            dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

      - name: Deploy to Output Branch
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
          publish_branch: output
          commit_message: "Update snake animation [skip ci]"
![GitHub Snake Animation](https://github.com/your-username/your-username/raw/output/github-snake.svg)

![GitHub Snake Animation](https://github.com/your-username/your-username/raw/output/github-snake-dark.svg)


Let's connect and collaborate!
