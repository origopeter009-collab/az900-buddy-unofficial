# AZ-900 Buddy (Unofficial)

> **Unofficial study aid.** Not affiliated with or endorsed by Microsoft. All content is original and based on the public AZ-900 skills outline on Microsoft Learn. No real exam questions are used.

**Live demo:** https://claude.ai/artifact/9Etn4UH3jbVbe4CW4hQ6et

Built for the hackathon theme *"Building Smarter Exam Prep Tools from Our Own Learning Journey."*

## The problem
Cloud concepts feel abstract to beginners, practice questions rarely explain *why* an answer is right, and learners can't tell when they're ready to sit the exam. Most prep material also assumes English and examples from outside Africa.

## What it does

| Challenge | Feature |
|---|---|
| Smart Quiz Builder | Instant feedback and an explanation on every answer, grouped by the three skills-outline areas. An AI builder writes 3 fresh original questions on any topic. |
| Flashcard Coach | 14 key terms with a simple spaced-repetition rule: missed cards return first, mastered cards move up. |
| Personal Study Planner | Exam date + hours per day gives a day-by-day plan that weights weaker, higher-weighted areas. |
| AI Study Buddy | Explains concepts simply with African everyday examples (matatus, M-Pesa, markets, SACCOs) in English, Kiswahili, Hausa, Yoruba or Nigerian Pidgin. |
| Readiness Tracker | Score per area plus one weighted readiness percentage (last 3 attempts per area). A guide, not a prediction. |

## Skills areas covered
1. Cloud concepts
2. Azure architecture and services
3. Azure management and governance

Readiness weights use the midpoints of the published exam ranges, so check the current outline on Microsoft Learn.

## Prompt design
- **Study Buddy:** role (beginner-friendly Azure Fundamentals helper), method (simple explanation, then African example, then the Azure term), requested language with service names kept in English, a 150-word limit, stay within the public outline, admit uncertainty, never reproduce real exam questions.
- **Quiz builder:** asks for original questions on a chosen topic and area, technical accuracy, and a strict JSON format (question, correct answer, 3 wrong answers, explanation). The page validates the format and escapes the text before display.

## How it's built
- Single self-contained HTML/CSS/JavaScript page (`index.html`), no framework.
- AI features use Claude through the artifact runtime.
- Progress is stored in the browser's `localStorage`.
- Responsive and supports light and dark mode.

## Limitations
- Small built-in question bank (9 questions) and 14 flashcards; the AI builder extends it, but generated questions should be checked against Microsoft Learn.
- Progress is saved only on one device and browser.
- Readiness percentage is a rough guide.
- Translations are AI-assisted and may need native-speaker review.

## Roadmap
- Save progress across devices with a backend such as Supabase.
- Larger reviewed question bank and more local languages.
- Support other fundamentals exams, such as AI-900.
- Let training communities contribute their own examples.

## Run it locally
Open `index.html` in a browser. The learning cards, flashcards, planner and tracker work offline. The AI features need the Claude artifact runtime, so use the live demo link for those.

## Credits
Built during the hackathon with AI-assisted tools including Claude.
