# Projektidee: Fluganst Buddy

## Ziel der Anwendung
Eine Web-App, die Menschen mit Hilfe von Informationen, Entspannungsübungen und Fortschrittsverfolgung dabei unterstützt mit ihrer Flugangst umzugehen. 

## Kernfunktionen
- Registrierung und Login für User
- Bereich für "Tagebucheinträge"
- Beruhigungsübungen (z.B. A-Z)
- Skala 1-10 pro Flug (mehrere Kategorien, z.B. Angst, Turbulenzen)

## Technischer Aufbau 
- **Frontend**: HTML, CSS, Javascript 
- **Backend**: PHP (Login, Datenverarbeitung)
- **Datenbank**: MySQL (Nutzer, Einträge, Übungen)
- **Server**: Lokale Umgebung 

## ERM 
# Tabelle: users
dot.node('users')
--------------
user_id (PK)
username (UNIQUE)
email (UNIQUE)
first_name
last_name
password
created_at

# Tabelle: entries
dot.node('entries')
--------------
entry_id (PK)
user_id (FK)
title
content
created_at
updated_at

# Tabelle: flight_ratings
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

# Tabelle: exercises (global)
dot.node('exercises')
--------------
exercise_id (PK)
title
description
category
created_at

# Tabelle: user_exercises (benutzerdefiniert)
dot.node('user_exercises')
--------------
user_exercise_id (PK)
user_id (FK)
title
description
created_at

# Beziehungen
dot.edge('users', 'entries', label='1:n')
dot.edge('users', 'flight_ratings', label='1:n')
dot.edge('users', 'user_exercises', label='1:n')