# Create_Your_Taboo

A custom Taboo game application designed for creating personalized card decks.

Traditional Taboo games didn't fit our group's dynamics and inside jokes, so this project allows you to build your own decks with custom words, forbidden terms, and references that matter to your friend group.

## Features
- Custom card deck creation
- Real-time database integration
- Mobile-friendly interface
- Motion controls for gameplay
- Multi-team tournament support

## Setup

### Firebase Configuration

To use this project, you need to set up your own Firebase project and add your credentials.

1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database in your project
3. Get your Firebase configuration from Project Settings
4. Replace the Firebase configuration in the HTML file (around line 140) with your own credentials:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "your-project.firebaseapp.com",
    projectId: "your-project-id",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID",
    measurementId: "YOUR_MEASUREMENT_ID"
};
```

### Firestore Security Rules

Don't forget to set up security rules in Firebase Console:
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /decks/{deckId} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}
```

## Deployment

The project is deployed on Netlify and accessible at:  
https://transcendent-mandazi-39ac0c.netlify.app

### Deploy Your Own

1. Fork this repository
2. Add your Firebase configuration
3. Deploy to Netlify or any static hosting service

## How to Play

1. Select or create a custom deck
2. Enter team names
3. Start the game
4. Tilt your phone down for ✓ (correct)
5. Tilt your phone up for ✗ (pass)

## Notes

Firebase was chosen as the database solution to persist custom decks across sessions, enabling real-time synchronization and easy access from any device.

## Technologies Used

- HTML5
- JavaScript (ES6 Modules)
- Firebase Firestore
- CSS3
