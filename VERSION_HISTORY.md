# CogniDeck - Version History

## [v4.0.0] - Advanced "Learn Mode"
*Date: 11/04/2025*

This is a major feature update that adds a powerful, customizable new study mode to make the app a true study tool.

### Added
- **New "Learn" Button:** Added a "Learn" button to all study sets on the dashboard.
- **Learn Setup Screen:** Created a new pre-session setup screen where users can customize their study session.
- **Customization Options:**
    - **Session Size:** Choose how many cards to study (10, 20, or All).
    - **Question Types:** Select "Multiple Choice," "Typed Answer," or a mix of both.
    - **Prompt Direction:** Choose to be prompted with the "Term" or the "Definition."
- **Learn Session Engine:**
    - The new session page tracks correct and incorrect answers.
    - Incorrectly answered cards are re-added to the queue to be asked again later.
    - The session ends when all cards in the session have been answered correctly at least once.
- **Confetti!:** Added a confetti celebration for successfully completing a Learn session.

## [v3.1.0] - The "About Me" Update
*Date: 11/01/2025*

This update adds a personal touch to the app, giving credit to the creator.

### Added
- Added a new **"About"** page to the main navigation bar.
- Created a new page featuring the "About the Creator" section for Andrew Stevenson.

## [v3.0.0] - Client-Side AI & Simplified Setup
*Date: 11/01/2025*

This was a major refactor to make the AI features *much* simpler to set up, removing the need for a separate backend deployment.

### Changed
- **Major AI Refactor:** Removed the need for Firebase Cloud Functions. The app now calls the Google Gemini AI **directly from the browser** using your API key.
- **Client-Side File Reading:** The "Import" page now reads PDF and text files entirely in the browser using `pdf.js` and `FileReader`.
- Updated the setup guide (`README.md`) to reflect the new, simpler 2-step process.

### Removed
- Removed the "How it works" section from the Import page.
- Removed all code related to Firebase Storage and Firebase Functions from the HTML file, as they are no longer needed.

## [v2.0.0] - New Study Modes & Polish
*Date: 11/01/2025*

Added new features to make studying more engaging and fun.

### Added
- **Practice Quiz Mode:** Added a new "Quiz" button to all study sets (with 4+ cards). This mode auto-generates a multiple-choice quiz from the set's terms and definitions.
- **Confetti Celebration:** Added a fun confetti animation that plays when a user finishes a study set (marks all cards as "known") or gets 100% on a quiz.

## [v1.0.0] - The Big Switch to HTML
*Date: 10/31/2025*

This was a foundational change, moving the entire project from React to a single, portable HTML file.

### Changed
- **Complete Rewrite:** The entire application was refactored from a React (`.jsx`) app into a **single `cognideck.html` file**.
- All components, styling (Tailwind), and logic (vanilla JavaScript) are now self-contained in one file.

### Added
- Created the first official `README.md` file for the project's GitHub repository, including setup instructions and technology badges.

### Fixed
- Resolved all previous JavaScript errors from the vanilla JS conversion, ensuring all pages (Auth, Dashboard, Editor) load and function correctly.

## [v0.1.0] - Initial Concept & Backend Setup
*Date: 10/30/2025*

The very first version of the project.

### Added
- Initial project concept as a "Quizlet clone" named **CogniDeck**.
- Set up the free Firebase backend for **Authentication** (Email/Password) and **Firestore** (Database).
- Implemented core features: User login/signup, creating, editing, and deleting flashcard sets.
- Implemented Public vs. Private sets and a "Search" page for all public sets.
