[![license](https://img.shields.io/github/license/DAVFoundation/captain-n3m0.svg?style=flat-square)](https://github.com/DAVFoundation/captain-n3m0/blob/master/LICENSE)

# Google-Books-Search

Description

React-based Google Books Search app that displays books on user searches. Users can save them to review or purchase later.
Save button to save the book to the database, View button to view the book on Google Books.

This project was bootstrapped with Create React App.

Deployment

This App is deployed on Heroku: https://googlebooks256.herokuapp.com/

ScreenShots of the Deployed App:
![picture](https://github.com/Bremah-mvp/Google-Books-Search/blob/main/client/public/images/Screenshot%201.png)

![picture](https://github.com/Bremah-mvp/Google-Books-Search/blob/main/client/public/images/Screenshot%202.png)

Technologies used
MVC design pattern: Model, View, Controller.

mern

MongoDB

Express.js

React.js

Node.js

Search for books using the Google Books API

  getBook: function (query) {
    return axios.get(`https://www.googleapis.com/books/v1/volumes?q=${query}`);
  },

  // Delete book with the given id
  deleteBook: function (id) {
    return axios.delete("/api/books/" + id).then(result => result.data);
  },

  // Save book to the database
  saveBook: function (bookData) {
    return axios.post("/api/books", bookData).then(result => result.data);
  },
  
  // Get saved books from the database
  savedBooks: function () {
    return axios.get("/api/books").then(result => result.data);
  }

  Installation

To install dependencies, run the following:

npm i

To run it locally, make sure that the MongoDB server is running on your machine.

Usage

npm start

License

This repository is licensed under the MIT license.

Questions

Questions about this repository? Please contact me at mvpbremah@gmail.com. View more of my work in GitHub at Bremah-mvp