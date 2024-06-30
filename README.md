#  Interactive Web-Based Quiz Platform

This repository contains the source code for a web-based quiz platform. The platform is equipped with an integrated quiz creation tool, quiz taker, question bank and a gamification feature for interactive quizzes. This platform was developed as part of the final year project for my Electrical and Electronic Engineering degree.

Currently there are already existing quiz platforms available. However, there is a lack for a singular product that incorporates both regular and gamified quizzes to cater for either professional or entertainment applications. Hence, this project aims to provides a versatile one-stop solution that addresses this problem. Its main objective is to enhance student participation and improve learning outcomes in classrooms. 

## Database and Website Hosting
The platform utilizes a **Microsoft Azure SQL Database** to store all quiz data. In order to attain the lowest latency and fastest load times, the server's geological location was set to East Asia, which is the best option for Malaysia.

The website is hosted using **Microsoft Azure Static Web Apps**. These web apps have an integrated feature that allows them to connect seamlessly to an **Azure SQL Database** without needing any backend coding. The quiz platform is deployed online as a web application, and the source files are stored in a GitHub repository.

The website can be accessed through the following link:<br />
https://green-mud-023b7ab00.4.azurestaticapps.net/login.html
> *Username:*&nbsp;&nbsp;teacher<br />*Password:*&nbsp;&nbsp;&nbsp;teacher

> ### Note
> The Azure SQL Database was set up using a free student package, which only has a one year trial period. Hence, the online quiz platform will only be operational till 13/11/2024, after which the database will then be offline indefinitely.

## JavaScript Libraries/Framework
- Bootstrap 5
- MathJax
- MathJS
- FileReader
- jQuery

## Features
1. Quiz Creator and Editor
   - An integrated quiz creation tool with 6 different question types.
2. Quiz Taker
   - A tool to attempt the created quizzes. Equipped with a point allocation system, feedback system and timer.
3. Question Bank
   - A structured repository to store questions for future quizzes. Equipped with import/export and search/filter functionalities.
4. Interactive Quiz
   - An integrated tool to host interactive quizzes. Gamifies existing quizzes by adding video game elements.

## Code Structure
- [login.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/login.html): Login page for quiz platform.
- [dashboard.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/dashboard.html): Home page to access to all the various features.
- [index.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/index.html): Integrated quiz creation tool.
- [editor.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/editor.html): Page to select an already uploaded quiz to be edited.
- [quiz_edit.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/quiz_edit.html): Integrated quiz editing tool.
- [tester.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/tester.html): Page to select an already uploaded quiz to be attempted.
- [quiz_test.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/quiz_test.html): Integrated quiz taking tool.
- [qbank.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/qbank.html): Page to add, remove and edit questions from the question bank.
- [interactive.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/interactive.html): Page to convert exisiting quizzes into interactive quizzes and host them.
- [lobby.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/lobby.html): Game lobby for all participants to join the interactive quiz.
- [waiting.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/waiting.html): Waiting room for all participants before the interactive quiz starts.
- [int_quiz_question.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/int_quiz_question.html): Main interactive quiz screen where the questions and answer choices are displayed, along with a leaderboard and other video game elements.
- [int_quiz_answer.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/int_quiz_answer.html): Main interactive quiz screen where each participant selects their desired answer choice. Displays the points earned for each question.
- [assets](https://github.com/julianganjs/interactive-quiz-platform/tree/main/assets): Contains all the styles, libraries, fonts, images and frameworks needed for the website to operate.
- [swa-db-connections](https://github.com/julianganjs/interactive-quiz-platform/tree/main/swa-db-connections): Configuration file for Microsoft Azure SQL Database.
