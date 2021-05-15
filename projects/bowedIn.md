---
layout: project
type: project
image: images/project1.jpg
title: Creating a job finding app with BowedIn
permalink: projects/bowedin
# All dates must be YYYY-MM-DD format!
date: 2021-05-14
labels:
  - Meteor
  - SemanticUI
  - JavaScript
  - JSX
  - Agile Project Management
  - Team work
summary: This is my final rpoject for ICS 314 Software Engineering using the Meteor framework. This involved extensive work in HTML, CSS, and JavaScript (an JSX). I also wrote tests using the testcafe suite and learned to deploy an application on Digital Ocean.
---
My final project for ICS 314 Software Engineering was an online application, Bowedin.com, aimed at helping students connect to employees and employees to students. Bowedin.com allows two categories of users: students and companies. Each type of user has access to different types of data in the database. Students are able to view positions that are offered by companies. Companies are able to view student profiles. Furthermore, each company has the ability to create and publish positions for students to view. Each position can either be a permanent job or an internship. All users have access to their respective homepage that lists their information that was collected when they signed up. Each user also has the ability to edit their profile information. Finally, Bowedin.com has an admin role that is able to review all information published by the database to monitor the app for inappropriate content.

My contribution to Bowedin was to create and design the Landing page. Pictured below.

<img class="ui centered large image" src="/images/BowedIn.png">

My main goal for the Landing page was to create an aesthetically pleasing and modern front for the application. It was very important for me to present a modern webpage that would evoke a sense of reliability yet appeal to the millennial and generation-z demographic. The process for creating this webpage involved first deciding on a color scheme. I chose to go with gray, orange, and Manoa green. I have also included several SemanticUI with React components including animated buttons and cards. As I designed the webpage I made certain to check with my group and take in any input and constructive criticism.

<img class="ui medium right floated rounded image" src="/images/messageBowedIn.png">

Another of my contributions was to implement a messaging service within the app. On the Recruit Students page (company user view) student profiles are presented as SemanticUI React cards and on the search page (student user view) positions are also listed as SemanticUI React Cards. An example of his emssage field is pictured to the right. On each card there is an option to send the owner of the Card a message. The message is then presented to the respective owner’s home page. I also implemented email functionality within BowedIn. Meaning that each message was then sent as an email automatically from a gmail account that I made: bowedinconnect@gmail.com. Each user will receive an email from this address with the contents of the message from BowedIn. This required me to work with the backend of the Meteor application. I wrote Meteor methods that retrieve data from the user and pass the information to the backend for processing. I also created a meteor method to allow the Meteor application to automatically send emails.

In addition to these tasks, I wrote numerous tests using the testcafe suite that helped make certain that features of the app worked properly. I additionally did minor UI updates throughout the app. Lastly, I worked with Digital Ocean to ascertain a secure connection (http -> https) that makes sure users have a secure connection while submitting and retrieving data. I was also in charge of deploying the app onto the Digital Ocean cloud.

Overall, this was an excellent and insightful learning experience. This was not just a demanding programming experience that involved learning and utilizing three programming languages: HTML, CSS, and JavaScript (and JSX). I was initially very intimidated and doubtful about my own ability to achieve this task. I was however, guided by my TA: Branden Ogata and encouraged and supported by my teammates: Justin Loi, Sara Cheng, and Jackie Wu. Without such people, I do not think I would have had such an amazing experience developing BowedIn.

Aside from the technical skill that I learned from this experience working with HTML, CSS, JavaScript, DigitalOcean, GitHub, and testcafe, I learned much about group work and team cooperation. I have thoroughly enjoyed my time working with other people and am encouraged to pursue interdynamic work in the future. I believe that I have learned about effectively communicating with others and offering support when needed.
