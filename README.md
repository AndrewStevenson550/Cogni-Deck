# CogniDeck: The AI-Powered Flashcard App

<p align="center">
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
<img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
<img src="https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Google Gemini" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
</p>

**CogniDeck** is a free, AI-powered flashcard application inspired by Quizlet. It's built as a single-file HTML/JavaScript application that connects to a powerful and free backend on Firebase.

The app allows users to create, share, and study flashcard sets. Its standout feature is an AI import tool: a user can upload a PDF or text file, and a serverless function automatically parses the document, sends the content to the **Google Gemini AI**, and creates a complete, ready-to-study flashcard set.

## Features

* **No Frameworks:** Built with pure HTML, Tailwind CSS, and vanilla JavaScript (ESM).
* **Full Authentication:** Secure user sign-up, log-in, and session management via Firebase Authentication.
* **Full CRUD for Sets:** Create, read, update, and delete your personal study sets.
* **Public vs. Private:** Choose to make your sets private or share them publicly.
* **Search:** A real-time search page to find all public study sets.
* **AI-Powered Import:**
    * Upload `.pdf` or `.txt` files.
    * A Firebase Cloud Function automatically triggers on upload.
    * The function parses the file, sends the text to the Google Gemini AI, and generates a set of terms and definitions.
    * The new, AI-generated set is saved directly to your account.
* **3D Study Mode:** A clean study interface with 3D card-flip animations.

## Tech Stack

* **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript
* **Backend:** Firebase
    * **Authentication:** User management (Email/Password).
    * **Database:** Firestore (for storing sets and cards).
    * **Storage:** Firebase Storage (for file uploads).
* **Serverless AI:**
    * **Firebase Cloud Functions (Node.js)**: To host the backend AI logic.
    * **Google Gemini AI (via Google AI Studio)**: For parsing documents and generating flashcards.
    * **pdf-parse**: A Node.js library for extracting text from PDFs in the Cloud Function.

## Setup and Installation

This project is fully functional, but it requires you to set up your own free Firebase backend and link your Google AI key.

### Step 1: Frontend (Already Done!)

No build step is required. The `cognideck.html` file is self-contained. The only thing you must do is add your Firebase config.

### Step 2: Set Up Your Free Firebase Project

1.  **Create a Project:** Go to the [Firebase Console](https://firebase.google.com/) and create a new project.
2.  **Enable Services:** In the "Build" menu, enable:
    * **Authentication** (select the "Email/Password" provider).
    * **Firestore Database** (start in "Production mode").
    * **Storage**.
3.  **Get Your Config:**
    * Go to your Project Settings and create a new "Web App" (`</>`).
    * Firebase will give you a `firebaseConfig` object.
4.  **Add Config to HTML:**
    * Open `cognideck.html`.
    * Find the `const firebaseConfig = { ... };` object inside the `<script type="module">` tag (around line 125).
    * Paste your `firebaseConfig` object there.
5.  **Set Database Rules:**
    * Go to **Firestore Database** -> **Rules**.
    * Paste in the following rules to allow users to control their own sets and read public ones. Click **Publish**.
