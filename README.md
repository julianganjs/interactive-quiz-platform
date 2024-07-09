#  Interactive Web-Based Quiz Platform

This repository contains the source code for a web-based quiz platform. The platform is equipped with an integrated quiz creation tool, quiz taker, question bank and a gamification feature for interactive quizzes. This was developed as part of the final year project for my Electrical and Electronic Engineering degree.

Currently there are already existing quiz platforms available. However, there is a lack for a singular product that incorporates both regular and gamified quizzes to cater for either professional or entertainment applications. Hence, this project aims to provides a versatile one-stop solution that addresses this problem. Its main objective is to enhance student participation and improve learning outcomes in classrooms. 

## Database and Website Hosting
The platform utilizes a **Microsoft Azure SQL Database** to store all quiz data. The website itself is hosted using **Microsoft Azure Static Web Apps**. These web apps have an integrated feature that allows them to connect seamlessly to an **Azure SQL Database** without needing any backend coding, and retrieves data using **REST API**. The quiz platform is deployed online as a web application, and the source files are stored in a GitHub repository.

The website can be accessed through the following link:<br />
https://green-mud-023b7ab00.4.azurestaticapps.net/login.html
> *Username:*&nbsp;&nbsp;teacher<br />*Password:*&nbsp;&nbsp;&nbsp;teacher

> ### Note
> As the database is currently offline, please wait for 1-2 minutes after the first login attempt, then refresh the login page and try again. The database will be awakened after the first login attempt, and the username and password can then be authenticated.<br /><br />The Azure SQL Database was set up using a free student package, which only has a one year trial period. Hence, the online quiz platform will only be operational till 13/11/2024, after which the database will then be offline indefinitely.

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
   - A tool to attempt the created quizzes. It's equipped with a point allocation system, feedback system and timer.
3. Question Bank
   - A structured repository to store questions for future quizzes. It's equipped with import/export and search/filter functionalities.
4. Interactive Quiz
   - An integrated tool to host interactive quizzes. It gamifies existing quizzes by adding video game and interactive elements.

## Code Structure
- [login.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/login.html): Login page for quiz platform.
- [dashboard.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/dashboard.html): Home page to access to all the various features.
- [index.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/index.html): Integrated quiz creation tool.
- [editor.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/editor.html): Selection page to choose an existing quiz to be edited.
- [quiz_edit.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/quiz_edit.html): Integrated quiz editing tool.
- [tester.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/tester.html): Selection page to choose an existing quiz to be attempted.
- [quiz_test.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/quiz_test.html): Integrated quiz taking tool.
- [qbank.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/qbank.html): Integrated question bank.
- [interactive.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/interactive.html): Selection page to convert exisiting quizzes into interactive quizzes and host them.
- [lobby.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/lobby.html): Game lobby for all participants to join the interactive quiz.
- [waiting.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/waiting.html): Waiting room for all participants before the interactive quiz starts.
- [int_quiz_question.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/int_quiz_question.html): Main interactive quiz screen where the game is carried out. Questions and answer choices are displayed along with a leaderboard and other video game elements.
- [int_quiz_answer.html](https://github.com/julianganjs/interactive-quiz-platform/blob/main/int_quiz_answer.html): Main interactive quiz screen where each participant selects their desired answer choice, and the points earned for each question is calculated and displayed.
- [assets](https://github.com/julianganjs/interactive-quiz-platform/tree/main/assets): Contains all the styles, libraries, fonts, images and frameworks needed for the website to operate.
- [swa-db-connections](https://github.com/julianganjs/interactive-quiz-platform/tree/main/swa-db-connections): Configuration file for Static Web Apps to Microsoft Azure SQL Database connection.

## Usage
1. Clone this repository.
2. Download all HTML files and the 'assets' folder into the same directory.
3. Inspect all HTML files, and remove all occurences of the following code snippet:
   ```ruby
   const endpoint = '/data-api/rest/#';
   const response = await fetch(endpoint);
   const data = await response.json();
   ```
   where '#' can be any value. This code snippet utilizes REST API to query data from the database in JSON format.
5. Replace all `data` variables with a dummy JSON object. For example:
   ```ruby
   data = {"value":[{"id":24,"course_id":"ENG1","quiz_id":"QZENG4","q_id":"2","q_type":"calc_multi"},{"id":25,"course_id":"ENG1","quiz_id":"QZENG4","q_id":"1","q_type":"calc"},{"id":26,"course_id":"ENG1","quiz_id":"QZENG1","q_id":"3","q_type":"sa"},{"id":27,"course_id":"ENG1","quiz_id":"QZENG1","q_id":"4","q_type":"essay"}]};
   ```
6. Refer to the subsequent code below each `data` variable to identify the key/value pairs needed.
7. Open dashboard.html using your default browser.
8. Access the desired feature by selecting any one of the cards in the home page.
9. If you do not wish to download the files onto your local machine, you may proceed to test the platform using the link: https://green-mud-023b7ab00.4.azurestaticapps.net/login.html

## Examples
### Login Page
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/f767f175-be58-460a-b6e9-08a69f752a6d" width="600vw">

### Home Page (Dashboard)
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/eb7e3e56-f42a-4b4f-9fe2-3b3f9d05e2c3" width="600vw">

### Quiz Creator
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/1e91daae-2b4e-4947-b4db-4fd78f3e4940" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/07784a0f-b32b-491f-9698-7cb719d8b41e" width="600vw"><br />
Up to 6 different question types are made available to the educator.

#### Question Types
- #### Multiple Choice
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/3db944cd-46f5-4b18-b823-d58a735d088e" width="650vw">
- #### True/False
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/7bb5ceab-f0ef-43e6-86b1-17b85c2977c4" width="650vw">
- #### Short Answer
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/893f8516-c274-43ed-8972-b2e61f3f2df2" width="650vw">
- #### Essay
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/4cabd2b2-05ad-45c9-bbe4-7f7b0b1e7e81" width="650vw"><br />
  The correct answer is in the form of keywords. The total mark for the question is divided by the number of keywords the educator has set. Thus, the quiz taker will be awarded a portion of the total marks for each correct keyword he/she has included in his/her essay answer.
- #### Calculated
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/9c2d558d-224f-4ef2-8d80-1a0ca9fa923c" width="650vw"><br />
  Calculated questions are able to generate random numeric values which populate the questions, using a mathematical formula keyed in by the educator. This prevents academic misconduct among students as they cannot copy each other's answer, due to all values will be different. The answer only accepts numerical values. The range of numbers which the random values are generated from is also set by the educator.
- #### Calculated Multichoice
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/10a80c94-9e26-43b4-9a4f-719093e65853" width="650vw"><br />
  Same concept as calculated questions, except the quiz takers are provided with 4 answer choices to choose from. The educator can set the format of which the answer choices are displayed in.

- ##### Get From Question Bank
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/c160851c-e021-4f48-a786-9941f032d1d6" width="650vw"><br />
  The quiz creator can access, retrieve and duplicate questions directly from the question bank.

### Quiz Editor
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/17990153-d927-45a0-a1b6-68f6a07419db" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/fdfe1ae4-9b84-47a6-b04f-d337b1ebbf0a" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/0efe6cb8-8d3f-43b4-bf20-be349eb36243" width="600vw"><br />
The quiz editor has the exact same layout as the quiz creator, except that it is only used to make changes to existing quizzes or delete them.

### Quiz Tester
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/98aad201-7c13-44e8-be23-9b558f021851" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/6bcf21a7-ed0f-4337-9c7f-e3a586795757" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/f7760f85-a815-41c1-b2a2-ea0f6f115195" width="600vw">
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/0bfa66e9-afae-4a2e-b3ab-cbb6d8e097ef" width="600vw"><br />
The quiz tester screen is equipped with a quiz navigation box to navigate between each question, a timer, and an automated feedback card system to display the correct answers when the quiz has ended.

### Question Bank
<img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/8b70bffe-4ba5-41b8-95aa-0c122c4cdb5c" width="600vw"><br />
The interface of the question bank is similar to the quiz creator tool, except that the existing questions in the bank are loaded beforehand. It is also equipped with a search and filter functionality.

### Interactive Quiz
- #### Starting Page
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/57e3b41c-778a-4b72-a432-6dcc01dc5775" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/f33cb17d-c54f-4cb6-9083-17fe412e3c90" width="650vw"><br/>
  This page is where the educator can host an interactive quiz session using existing quizzes, or where participants can join ongoing interactive quizzes using the provided unique quiz PIN.

- #### Lobby
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/2fbe67af-2265-474f-ad60-3d0dfbd31647" width="650vw"><br />
  The lobby screen displays the unique quiz PIN to join the session, along with each participant's name. This allows the educator to wait for all students to join the quiz before starting the session.

- #### Waiting Room
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/4e0f1df0-adfb-425a-9e95-59087f02387d" width="650vw"><br />
  This screen acts as a waiting room for all participants before the game session starts.

- #### Game Session (Educator's Screen)
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/38425617-27da-4a3d-931e-d39d89e08f9e" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/4f3cbf67-4740-4b71-8cfd-1f1775912637" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/f4b20301-0b03-4f8c-b5ce-b3c7d53a096f" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/05df1185-81cf-42d3-a299-b6757fd2bc77" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/892f3ca7-3f23-400a-a44f-be557a18496d" width="650vw">

- #### Game Session (Student's Screen)
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/ee404bca-392e-4b08-8a88-dbd509c9c11b" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/165fc0c3-4ec3-4ce1-8bee-942ff9aa6056" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/c7974125-7b8f-4eb2-a850-7c5de62fe9f9" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/5f0171a9-6163-418f-a090-fc4ffa0c3ffc" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/ed949c1f-a19a-4cd8-b26e-bb8d562e0346" width="650vw">
  <img src="https://github.com/julianganjs/interactive-quiz-platform/assets/127673790/4f71a0cd-0e7a-4c73-bad2-b094a5c212c4" width="650vw"><br/>
  The points earned for each question is calculated using a custom algorithm. For each question, a maximum amount of 1000 points is available. The student is awarded an amount of points based on the time remaining to answer the question (a quick answer = more points). This amount is then multiplied by a multiplier, which is determined based on the student's correct answer streak (if the student has answered 3 questions correctly in a row, then the points for the next question will be multiplied by x1.3). No points will be awarded for wrong answers and the student's answer streak will end.

## License
This project is licensed under the MIT License.
