education-quiz
=============

**F# Javascript HTML5 education client application with minimal PHP server interaction**



**Software Requirements Specification (http://en.wikipedia.org/wiki/Software_requirements_specification)**

Introduction Purpose
===================

This software is to run tutorials and quizzes in an internet browser using HTML5 and javascript. The original idea is to write the code in F# using Visual Studio 2012 with Websharper under a GNU AGPL v3 licence(http://www.websharper.com/licensing) this would also allow the use of Sencha extentions (http://www.websharper.com/downloads , http://www.sencha.com/products/touch/license/) and then convert it to HTML5/javascript using Websharper (other tools could also be used). 

Tutorials should be able to include SVG and animations such as Adobe Edge.
 
Quizzes should be able to create random numbers in the questions and there should be the ability to have working as part of the answer and multimedia elements. Most of the content should be on the client side with the option of uploading results to a PHP server (e.g. Linux) and downloading updates and content. Content should be available as either free or commercial. Content should be classified with teachers having the option to limit the use of classified content. 

Results should be able to be displayed, sent to the server, emailed and printed. A group of questions (test) should also be able to be printed. On the server side results from a school's students should be collated and sent back to the teachers. 

Usernames and passwords should be used rather than personal information. 

The client software should run on touch devices (e.g. phones and tablets) as well as computers (e.g. Linux, MACs and Windows), this should enable BYOD education. 

Open data standards should be used to allow a variety of authoring software to create the content. 

Comprehensive documentation/videos should be developed with each function. 

The UI should be easy to use, uncluttered, with a submenu to an options list. 

A rewards system should be set up to give pretend money to spend at a shop. The goods purchased should depreciate in some way, such as a car requiring regular servicing with cost based on car value and usage. This would ensure a more realistic purchasing-depreciation/investment-growth 3D world. 

There should be a recall section where the same question is asked after an hour then a day then a week then a month then each year (variable steps) to aid recall (forgotten items to go back to the 'just learnt' category. 

A group of questions (curriculum) should be able to be set up by the teacher.

A group of questions (revision material) should be able to be set up by the teacher/student.

Multimedia with sound be accessible to the deaf.

Pages should load the essentials first then the background code and graphics (e.g. button with 'Exit' text before the exit graphics)

 ---------

Definitions
----------


 System overview
 --------------
F# programming to be converted to HTML5/javascript for client internet browser.
PHP programming for server

 References
 ---------
GNU AGPL v3 licence: http://www.gnu.org/licenses/agpl-3.0.html
Websharper: www.websharper.com
www.sencha.com

 
Overall description Product perspective System Interfaces
========================================================

 User Interfaces
 --------------
Main screen, sub-menu with scroll down containing buttons to other menues.

 Hardware interfaces
 ------------------
Any browser enabled device (phone, touchpad, PC, etc)

 Software interfaces
 ------------------
HTML5 enabled Internet browser

 Communication Interfaces
 -----------------------
web links or email between client and server for updates, results and content

 Memory Constraints
 -----------------
Most content on client HDD, phone RAM (variation in features depending on client)

 Operations
 ---------
Open index page on client, this links to sub-menues:
Recall learnt material
Theory material
Quiz material
Results
Shop
Other

 Site Adaptation Requirements
 ---------------------------
Need to change client HTML5 based on device (phone, touch, PC, etc.)
 
Product functions
================

 User characteristics
 -------------------
Teachers
Students

 Constraints, assumptions and dependencies
 ----------------------------------------
Load text based content before graphics
 
Specific requirements External interface requirements
====================================================

 Functional requirements
 ----------------------
Only send new data
update client to receipt successful results upload
store data in database in such a fashion to minimise cost (e.g 1KB blocks for Amaxon's DynamoDB)


 Performance requirements
 -----------------------
Client page opens in 1 second.
Server page opens in 1 second.

 Design constraints Standards Compliance
 --------------------------------------
Must satisfy HTML5
 
Logical database requirement
===========================

 Software System attributes Reliability
 -------------------------------------
Create code for multiple types of Databases (e.g. SQL, DynamoDB, mySQL)

 Availability
 -----------
24/7/365

 Security
 -------
store multiple copies of data in geographic separate locations to ensure redundancy

 Maintainability
 --------------
automatic

 Portability
 ----------
communication with open data types (e.g. CSV)
 
Other requirements
=================
due to limitations in DynamoDB and other databases students need to be limited to a particular school.
a data table with summary data to be created at the same time as individual results (e.g. update averages)
Content must have a voting system with each question to determine which questions need replacing.


