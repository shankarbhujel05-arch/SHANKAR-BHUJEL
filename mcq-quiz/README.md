# MCQ Quiz — BY Er. Shankar Bhujel

A fully static MCQ quiz website. Works on GitHub Pages with no backend or database.

## 📁 File Structure

```
/
├── index.html            ← Main quiz app (single file)
├── quizzes.json          ← Manifest listing all available quizzes
└── questions/
    ├── general_knowledge.json
    ├── grammar.json
    ├── vocabulary.json
    └── your_quiz.json    ← Add your own!
```

## ➕ How to Add a New Quiz

### Step 1 — Create a JSON file in `/questions/`

```json
{
  "title": "My Quiz Title",
  "questions": [
    {
      "question": "What is 2 + 2?",
      "options": ["3", "4", "5", "6"],
      "answer": 1,
      "explanation": "2 + 2 equals 4. This is basic arithmetic."
    }
  ]
}
```

- `answer` is the **index** of the correct option (0 = first, 1 = second, etc.)

### Step 2 — Register it in `quizzes.json`

```json
{
  "quizzes": [
    {
      "id": "my_quiz",
      "file": "questions/my_quiz.json",
      "title": "My Quiz Title",
      "description": "A short description",
      "icon": "🧮"
    }
  ]
}
```

## ♻️ Re-practicing Mistakes

After completing a quiz, click **Export Mistakes** to download a `_mistakes.json` file.
You can load that file back into the quiz for targeted revision.

## 🌐 Deploying to GitHub Pages

1. Push all files to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root `/`
4. Your quiz will be live at `https://yourusername.github.io/repo-name/`

## ✅ Features

- Dynamic quiz loading from JSON files
- Color-coded answer feedback (green/red)
- Explanation reveal after each answer
- Live score counter + timer
- Previous/Next navigation
- Progress indicator
- Quiz completion summary with accuracy %
- Mistake tracking & export
- Responsive — works on mobile, tablet, desktop
- 100% static — no server needed
