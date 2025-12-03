# Lumina - AI-Generated SaaS Landing Page

### Front-End Development Intern Assignment
**Submitted by:** [Your Name]
**Live Demo:** [INSERT YOUR HOSTED GITHUB PAGES/NETLIFY LINK HERE]
**Walkthrough Video:** [INSERT YOUR VIDYARD LINK HERE]

---

## 📋 Project Overview
This repository contains a high-fidelity, responsive landing page for "Lumina," a fictional AI analytics company. The entire codebase (HTML, Tailwind classes, and JavaScript logic) was generated using **[Insert AI Tool Name, e.g., Claude 3.5 Sonnet]** via a structured prompt engineering workflow.

## 🛠️ Tech Stack & Tools
* **Core:** HTML5, Vanilla JavaScript
* **Styling:** Tailwind CSS (via CDN for portability)
* **Fonts:** Google Fonts (Inter & Outfit)
* **Assets:** Unsplash (Images), Inline SVGs (Icons)
* **AI Model:** [e.g., Claude 3.5 Sonnet / GPT-4o]
* **Hosting:** [GitHub Pages / Netlify]

---

## 🧠 Prompt Engineering Strategy
To meet the requirement for "reusable and high-quality prompts," I moved away from simple zero-shot commands and adopted a **Modular Meta-Prompt Architecture**.

### 1. The "Meta-Prompt" (Governance Layer)
Before generating any UI, I initialized the AI with a strict "System Instruction." This defined:
* **Global Design Tokens:** Fixed colors (`indigo-600`, `slate-900`) to prevent visual inconsistency.
* **Mobile-First Constraint:** Forced the AI to write `base` classes for mobile and `md:` prefixes for desktop.
* **Tech Constraints:** Strictly prohibited external CSS files to ensure the final output was a single, portable HTML file.

### 2. Component-Based Generation
I broke the generation process into 5 sequential steps (Navbar → Hero → Features → Form → Footer). This prevented the AI from hitting token limits and allowed for "Context Isolation," ensuring each section received full attention to detail.

---

## 🔄 Challenges & Iteration (Refinement Process)
*Evaluation Criteria: How I handled errors and refined prompts.*

### Challenge 1: The Mobile Menu State
* **Issue:** Initially, the AI generated a mobile menu that was visible by default, cluttering the mobile view.
* **Fix:** I refined the Navbar prompt to explicitly request a `hidden` class by default and a specific Vanilla JS script to toggle the state. I enforced the use of `id` attributes to ensure the JavaScript could target the correct DOM elements.

### Challenge 2: Image Consistency
* **Issue:** The AI initially suggested using `<img>` tags with random sources that might break.
* **Fix:** I updated the Meta-Prompt to enforce `images.unsplash.com` with specific search keywords (e.g., "dashboard", "analytics") and the `object-cover` class to prevent aspect ratio distortion.

### Challenge 3: Visual Rhythm
* **Issue:** The sections felt "flat" when strictly using white backgrounds.
* **Fix:** I introduced a constraint in the "Features" prompt to use `bg-gray-50`. This created a visual distinction between the Hero (White) and Features (Gray), improving the user journey.

---

## 📂 Project Structure
Since the assignment required a simple hosted page, I utilized a "Zero-Build" approach:

```text
/
├── index.html      # Contains all structure, styles (Tailwind), and scripts
└── README.md       # Documentation and Strategy
