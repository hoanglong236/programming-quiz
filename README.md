# Programming Quiz

A mobile-friendly web quiz for practicing programming and computer science topics.  
Built with plain HTML, CSS, and JavaScript – no build tools or dependencies required.

## ✨ Features

- 7 topics: Java, C#, PHP, Database, Cloud, Web, C/C++
- 80+ questions per topic
- Instant feedback with explanations
- Jump to any question
- Progress bar and score tracking
- **Automatic progress saving** using `localStorage`
- Export / import progress as JSON (for backup or moving between devices)
- Responsive design that works on desktop and mobile

## 🚀 Live Demo

You can host this yourself using GitHub Pages:

1. Upload the `index.html` file to a GitHub repository.
2. Go to **Settings → Pages**.
3. Select the branch (usually `main`) and root folder.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`

## 📱 Running on your phone

Open the deployed URL in Chrome or Safari.  
Progress is saved automatically in the browser’s local storage.

To back up or transfer progress, use the **Export progress** button to download a JSON file, then use **Import progress** on another device.

## 🧠 How it works

- Select a topic from the dropdown.
- Answer questions and click **Check answer**.
- Your answers are saved instantly.
- Use the number buttons to jump between questions.
- When all questions are answered, your final score is shown.

## 📂 File Structure

```
.
├── index.html   # All HTML, CSS, and JavaScript in one file
├── LICENSE      # MIT License
└── README.md
```

## 🛠 Customization

You can add or modify questions directly inside the `<script>` section of `index.html`.  
Each question follows this format:

```javascript
{
  topic: "Java",
  question: "What is the default value of an int in Java?",
  options: ["0", "null", "undefined", "1"],
  correct: 0, // index of the correct option
  explanation: "The default value of int is 0."
}
```

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.