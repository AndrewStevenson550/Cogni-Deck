# Cogni-Deck
CogniDeck: The AI-Powered Flashcard App

<p align="center">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/HTML5-E34F26%3Fstyle%3Dfor-the-badge%26logo%3Dhtml5%26logoColor%3Dwhite" alt="HTML5" />
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Tailwind_CSS-06B6D4%3Fstyle%3Dfor-the-badge%26logo%3Dtailwindcss%26logoColor%3Dwhite" alt="Tailwind CSS" />
<img src="https://www.google.com/search?q=https://img.shields.io/badge/JavaScript-F7DF1E%3Fstyle%3Dfor-the-badge%26logo%3Djavascript%26logoColor%3Dblack" alt="JavaScript" />
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Firebase-FFCA28%3Fstyle%3Dfor-the-badge%26logo%3Dfirebase%26logoColor%3Dblack" alt="Firebase" />
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Google_Gemini-4285F4%3Fstyle%3Dfor-the-badge%26logo%3Dgoogle%26logoColor%3Dwhite" alt="Google Gemini" />
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Node.js-339933%3Fstyle%3Dfor-the-badge%26logo%3Dnodedotjs%26logoColor%3Dwhite" alt="Node.js" />
</p>

CogniDeck is a free, AI-powered flashcard application inspired by Quizlet. It's built as a single-file HTML/JavaScript application that connects to a powerful and free backend on Firebase.

The app allows users to create, share, and study flashcard sets. Its standout feature is an AI import tool: a user can upload a PDF or text file, and a serverless function automatically parses the document, sends the content to the Google Gemini AI, and creates a complete, ready-to-study flashcard set.

Features

No Frameworks: Built with pure HTML, Tailwind CSS, and vanilla JavaScript (ESM).

Full Authentication: Secure user sign-up, log-in, and session management via Firebase Authentication.

Full CRUD for Sets: Create, read, update, and delete your personal study sets.

Public vs. Private: Choose to make your sets private or share them publicly.

Search: A real-time search page to find all public study sets.

AI-Powered Import:

Upload .pdf or .txt files.

A Firebase Cloud Function automatically triggers on upload.

The function parses the file, sends the text to the Google Gemini AI, and generates a set of terms and definitions.

The new, AI-generated set is saved directly to your account.

3D Study Mode: A clean study interface with 3D card-flip animations.

Tech Stack

Frontend: HTML5, Tailwind CSS, Vanilla JavaScript

Backend: Firebase

Authentication: User management (Email/Password).

Database: Firestore (for storing sets and cards).

Storage: Firebase Storage (for file uploads).

Serverless AI:

Firebase Cloud Functions (Node.js): To host the backend AI logic.

Google Gemini AI (via Google AI Studio): For parsing documents and generating flashcards.

pdf-parse: A Node.js library for extracting text from PDFs in the Cloud Function.
