# Programming Quiz

A mobile-friendly web quiz for practicing programming and computer science topics.  
Built with plain HTML, CSS, and JavaScript – no build tools or dependencies required.

## ✨ Features

- 7 topics: Java, C#, PHP, Database, Cloud, Web, C/C++
- 80+ questions per topic
- Instant feedback with explanations
- **Code snippet formatting** in questions and explanations, with a language label and copy button
- Jump to any question
- Progress bar and score tracking
- **Automatic progress saving** using `localStorage`
- **Copy question** button to quickly grab the current question and options
- Flag questions for later review
- Export / import progress as JSON (for backup or moving between devices)
- Responsive design that works on desktop and mobile

## 🚀 Live Demo

You can host this yourself using GitHub Pages:

1. Upload the files to a GitHub repository.
2. Go to **Settings → Pages**.
3. Select the branch (usually `main`) and root folder.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`

## 📱 Running on your phone

Open the deployed URL in Chrome or Safari.  
Progress is saved automatically in the browser's local storage.

To back up or transfer progress, use the **Export progress** button to download a JSON file, then use **Import progress** on another device.

## 🧠 How it works

- Select a topic from the dropdown.
- Answer questions and click **Check answer**.
- Your answers are saved instantly.
- Use the number buttons to jump between questions.
- Flag questions you want to revisit.
- When all questions are answered, your final score is shown.

## 📂 File Structure

```
.
├── index.html      # Quiz UI, styles, and logic
├── questions.js    # All quiz questions grouped by topic
├── LICENSE         # MIT License
└── README.md
```

## 🛠 Customization

### Adding or editing questions

All questions live in `questions.js`, grouped by topic. Each topic is exposed as a global array (e.g. `javaQuestions`, `csharpQuestions`, …) that `index.html` reads through the `topics` mapping.

Each question follows this format:

```javascript
{
  topic: "Java",
  question: "What is the default value of an int in Java?",
  options: ["0", "null", "undefined", "1"],
  correct: 0, // index of the correct option
  explanation: "The default value of `int` is `0`."
}
```

To add a new topic, create a new array in `questions.js`, register it in the `topics` object inside `index.html`, and add a matching `<option>` to the topic dropdown in the HTML.

### Code formatting

The `question` and `explanation` fields support Markdown-style code formatting:

- Inline code using single backticks: `` `readonly` ``
- Fenced code blocks using triple backticks, optionally with a language identifier:

  ````markdown
  ```csharp
  readonly int instanceValue;
  ```
  ````

Code blocks are rendered with a language label and a copy button.

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.