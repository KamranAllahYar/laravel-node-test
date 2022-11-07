# laravel-node-test

Tech requirements
==========================

1) Use an SQL Database with an ORM
2) Store data in related tables with foreign keys, don't use json columns
3) Use a high level Javascript or PHP framework (Nest.JS, AdonisJs, Laravel

User stories  
============
1) As a user I would like to book an appointment
2) As a user I would like to select the date and see all available slots for this day As a user I want to open the scheduling page and schedule for multiple people at once (think of booking a haircut for yourself and your two kids)
3) As a business, I want to create different schedulings that have separate configuration for all user stories below
4) As a business I want to have a configurable break break between appointments
5) As a business owner I want to offer timeslots for a configurable amount of days (for example starting from today always 7 days)
6) As a business owner I want to configure breaks 
7) As a business owner I want that a configurable amount (1 or more) clients can book one time slot
8) As a business owner I want to not get invalid bookings: for booked out slots, out of range, disabled time validation should fail
9) As a business owner I want to set opening hours which can differ from day to day (for example I want to have different opening hours on weekends and monday)
10) As a business owner I want create one or multiple breaks (lunch, cleaning, ...), for example a lunch break from 12:00-13:00 and a cleaning break from 15:00-16:00
11) As a business owner I would like to specify times when I dont work, for example on public holidays
12) As a business owner I want to create multiple different scheduling events with totally different parameters (hair cut, hair coloring, whatever)
13) As a business owner I want those different events to be totally separate
14) As another developer I want peace of mind and just run the automated test suite and know that I did not break anything

Acceptance criteria
===================
1) A time scheduling JSON based Rest API should be created
2) 1 GET api which provides all data an SPA might need to display a calendar and a time selection
3) 1 POST api which creates a booking for 1 or more people
4) Implement automated testing that ensures the functionality of your code
5) For the tests purpose, A booking is done with only an E-Mail, first name and last name
6) Important: dont trust the frontend, validate the data so that the API returns an exception in case something does not fit into the schema or is already booked out - For a men haircut - booking should not be possible at 7am because its before the shop opens - booking at 8:02 should not be possible because its not fitting in any slot - booking at 12:15 should not be possible as its lunch break
7) Seed your database with the following scheduling - Men Haircut - slots for the next 7 days, sunday off - from 08:00-20:00 monday to friday - from 10:00-22:00 saturday - lunch break at 12:00-13:00 - cleaning break at 15:00-16:00 - max 3 clients per slot - slots every 10 minutes - 5 minutes cleanup break between slots - the third day starting from now is a public holiday - Woman Haircut - slots for the next 7 days, sunday off - lunch break at 12:00-13:00 - from 08:00-20:00 monday to friday - from 10:00-22:00 saturday - cleaning break at 15:00-16:00 - slots every 1 hour - 10 minutes cleanup break  - max 3 clients per slot - the third day starting from now is a public holiday

Grading
========
Your project will be graded by 3 attributes, each on a scale of 1-10. If an attribute dips below 7 it disqualifies your solution. You need an average score of at least 8 to pass this round.

1) Feature completeness 1-10
2) No edge cases & bug free 1-10
3) Code style & architecture 1-10

Hints
=====

1) 4/10 people fail on feature completeness because they did not read the project description carefully. Our tip: Read carefully, check if your project fullfills every user story and ask if you dont understand something 100 %.
2) 5/10 people fail because their code is buggy and they have not tested it properly for edge cases. If you test < 2 hours the chance is high, you belong to this category. Our tip: test your stuff!
