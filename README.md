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
   - An integrated tool to attempt the quizzes created.
3. Question Bank
   - A structured repository to store questions for future quizzes. Equipped with import/export and search/filter functionalities.
4. Interactive Quiz
   - An integrated tool to convert created quizzes into gamified quizzes which can be hosted.
