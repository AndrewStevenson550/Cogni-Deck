# CogniDeck: The AI-Powered Flashcard App

<p align="center">
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
<img src="https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Gemini" />
<a href="https://andrewstevenson550.github.io/Cogni-Deck/"><img src="https://img.shields.io/badge/Live%20Site-34A853?style=for-the-badge&logo=githubpages&logoColor=white" alt="Live Site" /></a>
</p>

**CogniDeck** is a free, AI-powered flashcard application inspired by Quizlet. It's built as a **single-file HTML/JavaScript application** that connects to a free backend on Firebase.

The app allows users to create, share, and study flashcard sets. Its standout feature is an AI import tool: a user can upload a `.txt` file, and the app will **call the Google Gemini AI directly from the browser** to create a complete, ready-to-study flashcard set.

## Features

* **No Frameworks, No Build Step:** Built with pure HTML, Tailwind CSS, and vanilla JavaScript (ESM).
* **Full Authentication:** Secure user sign-up, log-in, and session management via Firebase Authentication.
* **Full CRUD for Sets:** Create, read, update, and delete your personal study sets.
* **Public vs. Private:** Choose to make your sets private or share them publicly.
* **Search:** A real-time search page to find all public study sets.
* **AI-Powered Import (from .txt files):**
    * Upload a `.txt` file directly from the app.
    * The app reads the file in the browser and sends the text to the Google Gemini AI.
    * The AI generates terms and definitions and saves them as a new set in your account.
* **Multiple Study Modes:**
    * **3D Flashcards:** A clean study interface with 3D card-flip animations and progress tracking.
    * **Practice Quiz:** A multiple-choice quiz auto-generated from your card set.
* **Celebrations:** Fun confetti animation when you complete a study set or quiz!

## Tech Stack

* **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript
* **Backend:** Firebase
    * **Authentication:** User management (Email/Password).
    * **Database:** Firestore (for storing sets and cards).
* **AI:**
    * **Google Gemini AI (via Google AI Studio)**: Called directly from the browser to generate flashcards from text.

