# Introduction 
My idea for this project is a web app designed to support people who experience fear of flying. Since, until recently I used to be a very anxious flyer myself, I know first-hand how difficult this can be and how it can limit your life. For me it meant not being able to sleep the nights leading up to the flight, stomach aches, no appetite and and a lot of tension. And even though there are alternatives to flying, sometimes getting on a plane is unavoidable. Especially for long distances  or you need to be somewhere quickly, whether it's a meeting in another city or for personal reasons. 

# Introduction App
For this reason, I developed a concept for an app that is meant to support people in this situation. It's not desigend to be a therpeutic app, but rather a practical tool to help users prepare for their flight and stay as calm as possible during the experience. It also gives them the option to take notes after each flight, which can help them track their feelings and progress over time. 

## Functions 
### Exercises
Users can choose between recommended calming exercises that come with the app — each with a short description — or they can add their own relaxing techniques and exercises to their profile.


### Route 
It will be possible to enter both the departure and the destination airport for each flight.

### Airline (optional)
Furthermore, users can enter the airline they flew with. This field is  optional though.

### Scales
There will be different categories with scales from 1-10, which can be used to rate how strong you experienced turbulances, as well as a scale that lets you chose your average anxiety level throught your flight. 


## Technical Details 

### Database 
All user data — such as username, first name, last name, password, and so on — will be stored in a MySQL database.
The following tables will be used for this project: users, entries, flight_ratings, and user_exercises.
The last two tables are linked to the user through a foreign key, which makes it possible to clearly identify which account each entry belongs to.

### Signup and Login  
The signup process is validated on the server side using PHP.
The validation checks whether a username is already taken, whether the password meets certain requirements (such as minimum length and special characters), and whether all required fields have been filled out.
The data is only saved to the database once all conditions are met.

For the login process, PHP checks whether a user with matching credentials exists by comparing the input to the database.
If the information is incorrect, an appropriate error message is displayed.

### Server
The app runs locally on an Apache server using XAMPP.
The logic is implemented in PHP, while the data is stored in a MySQL database.
To protect against SQL injection, the database connection is handled through PDO.

### User Interface/User Experience(UI/UX)
The app is intentionally kept simple, since the main focus is on functionality rather than appearance.
It uses HTML and CSS, as well as JavaScript for interactive elements such as navigation and live feedback in forms.

For better usability, JavaScript is also used to immediately show whether certain password requirements are met while typing.
However, the actual validation and data processing is still handled on the server with PHP for security reasons.

### APIs
At the moment, the app does not use any external APIs.
However, I believe it has a lot of potential and could be expanded with additional features in the future.
Possible examples include a weather forecast for the day of the flight, automatic airline suggestions while typing, travel notices, and more.

# Conclusion
Fear of flying is something that affects many people.
While I cannot cure anyone with this project, I hope that it can make a  difference by helping users regain a sense of control — both technically and emotionally.

Thank you for your attention