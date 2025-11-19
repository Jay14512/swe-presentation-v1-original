# Einleitung 
Meine Projektidee ist eine Web-Applikation für Menschen mit Flugangst. Da ich bis vor kurzem selbst unter massiver Flugangst litt, weiß ich aus Erfahrung, wie problematisch das sein kann. Begonnen damit, dass man einige Nächte davor schon nicht mehr schlafen kann, einen Knoten im Bauch hat, kein Appetit und so weiter. Natürlich gibt es Alternativen zum Fliegen, jedoch lässt es sich nicht immer vermeiden. Gerade bei längeren Strecken oder wenn man mal schnell wo sein muss, zum Beispiel bei einem Meeting in einer anderen Stadt oder aus sonstigen geschäflichen beziehungsweise privaten Gründen. 

# Vorstellung App
Genau für dieses Problem bzw. für diese Situation habe ich ein Konzept für eine App entwickelt, die Menschen dabei Helfen soll mit ihrer Flugangst besser umzugehen. Es handelt sich hierbei nicht um eine App, mit der man sich therapieren kann, sondern vielmehr um ein Werkzeug um die Vorbereitungen auf den Flug beziehungsweise den Flug selbst so stressfrei wie möglich zu gestalten und hinterher die Möglichkeit bieten sich Notizen zum jeweiligen Flug zu machen. 

## Funktionen 
### Übungen
Die User:innen haben die Möglichkeit entweder empfohlene Beruhigungsübungen durchzuführen, welche mit Beschreibung direkt in der App mitgeliefert werden, oder eigene Entspannungstechniken und Übungen mit Beschreibung dieser in ihrem Profil einzutragen. 

### Strecke 
Für jeden Flug gibt es die Möglichkeit sowohl den Start als auch den Zielflughafen anzugeben. 

### Fluglinie (optional)
Weiters gibt es die Möglichkeit einzutragen mit welcher Gesellschaft jemand geflogen ist. Dieses Feld ist jedoch optional. 

### Skalas
Es wird verschiedene Kategorien mit Skalas von 1-10 geben. Zum Beispiel eine Skala in der man bewerten kann wie stark man die Turbulenzen empfunden hat. Eine weitere Skala auf der man das durchschnittliche Angstlevel während des Flugs auswählen kann. 

## Technische Details 

### Datenbank 
Alle Daten der User:innen, sprich Username, Vorname, Nachname, Passwort und so weiter werden in MySQL gespeichert. Die Datenbank enthält neben der User-Tabelle weitere Tabellen wie entries, flight_ratings und user_exercises, die über Foreign Keys mit dem jeweiligen User beziehungsweise der jeweiligen Userin verknüpft sind. Dadurch lässt sich jederzeit nachvollziehen, welchem Konto der Eintrag zuzuordnen ist. 

### Signup und Login  
Die Registrierung wird serverseitig mit PHP validiert. Dabei wird zum Beispiel geprüft, ob der Benutzername bereits vergeben ist, ob das Passwort bestimmte Anforderungen erfüllt (zum Beispiel Mindestlänge und Sonderzeichen), und ob alle Pflichtfelder ausgefüllt wurden. Erst wenn alle Bedingungen erfüllt sind, werden die Daten in der Datenbank gespeichert.

Beim Login wird mit PHP überprüft, ob ein:e passende:r User:in mit den angegebenen Zugangsdaten existiert. Dazu wird ein Datenbankabgleich durchgeführt. Wenn die Angaben nicht stimmen, wird eine entsprechende Fehlermeldung angezeigt.

### Server
Die App läuft lokal mit einem Apache-Server über XAMPP. Die Logik wird mit PHP umgesetzt, während die Daten mit MySQL verwaltet werden. Um SQL-Injections zu verhindern erfolgt die Verbindung zur Datenbank über PDO. 

### User Interface/User Experience(UI/UX)
Die App ist bewusst schlicht gehalten, da der Hauptfokus auf der Funktionalität und nicht auf dem Aussehen liegt. Es wird HTML und CSS sowie JavaScript für die Interaktivität von Navigationselementen und Live-Feedback bei Formularen verwendet. 

Für bessere Benutzerfreundlichkeit wird JavaScript verwendet, um beim Passwortfeld direkt zu zeigen, ob bestimmte Anforderungen erfüllt sind. Die eigentliche Validierung und Datenverarbeitung erfolgt aus Sicherheitsgründen trotzdem auf dem Server mit PHP.

### APIs
Im Moment werden noch keine APIs verwendet. Jedoch hat die App meiner Meinung nach sehr viel Potenzial und könnte in Zukunft mit weiteren Funktionen ausgebaut werden. Beispiele hierfür sind eine Wettervorhersage für den Tag des Flugs, automatische Vorschläge der Fluggesellschaft während man tippt, Reisehinweise und so weiter.

# Abschluss
Flugangst ist ein Thema von dem sehr sehr viele Menschen betroffen sind. Mit meinem Projekt kann ich zwar niemanden einfach so von Flugangst befreien, jeodch hoffe ich, dass einen kleinen Beitrag damit leisten kann, um Betroffenen ein bisschen Kontrolle über die Situation zu geben, sowohl technisch, als auch emotional. 

Vielen Dank 