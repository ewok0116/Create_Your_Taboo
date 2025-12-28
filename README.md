# Create_Your_Taboo
A custom Taboo game application designed for creating personalized card decks.   Traditional Taboo games didn't fit our group's dynamics and inside jokes, so this project allows you to build your own decks with custom words, forbidden terms, and references that matter to your friend group.

#Notes
To keep the decks a db was a necessity so I created a db on firebase and added the necessary code block.
Example of that necessary code block:
//CHANGE HERE
export const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "your-project.firebaseapp.com",
    projectId: "your-project",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "123456789",
    appId: "1:12345:web:abcde",
    measurementId: "G-XXXXX"
};
This is the part that needs a change in index.json
