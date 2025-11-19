# Project Idea: Fly Buddy

## Goal of the App
A web app designed to support individuals with fear of flying by providing helpful information, calming exercises, optional progress tracking and gentle guidance to increase comfort and confidence.

## Core Functions
- Sign up and log in for users
- Area for diary entries
- Calming exercises (e.g. A-Z)
- Scale 1-10 per flight (multiple Categories, e.g. Anxiety, Turbulence, etc)

## Tech Stack
- **Frontend**: HTML, CSS, Javascript 
- **Backend**: PHP (Login, Data handling)
- **Database**: MySQL (Users, Entries, Exercises)
- **Server**: Local Environment

## ERM 
# table: users
dot.node('users')
--------------
user_id (PK)
username (UNIQUE)
email (UNIQUE)
first_name
last_name
password
created_at

# table: entries
dot.node('entries')
--------------
entry_id (PK)
user_id (FK)
title
content
created_at
updated_at

# table: flight_ratings
dot.node('flight_ratings')
--------------
rating_id (PK)
user_id (FK)
flight_date
departure_airport
arrival_airport
airline (nullable)
anxiety_level
turbulence_level
comment
created_at

# table: exercises (global)
dot.node('exercises')
--------------
exercise_id (PK)
title
description
category
created_at

# table: user_exercises (custom)
dot.node('user_exercises')
--------------
user_exercise_id (PK)
user_id (FK)
title
description
created_at

# Relations
dot.edge('users', 'entries', label='1:n')
dot.edge('users', 'flight_ratings', label='1:n')
dot.edge('users', 'user_exercises', label='1:n')