# Musterlösung Praktische Aufgabe HTML und CSS IV

## Webentwicklung mit HTML und CSS

### Aufgabe 1: Erstellen einer einfachen HTML-Seite

Erstellen Sie eine HTML-Seite mit dem Titel **"Meine erste Webseite"**. Die Seite soll folgende Elemente enthalten:

- Eine Überschrift der Stufe 1 mit dem Text **"Willkommen auf meiner Webseite"**.
- Einen Absatz mit einer kurzen Beschreibung über sich selbst.
- Ein Bild von sich selbst (verwenden Sie ein beliebiges Bild aus dem Internet).
- Eine ungeordnete Liste mit drei Ihrer Hobbys.

### Aufgabe 2: Einbinden und Anwenden von CSS

Erstellen Sie eine externe CSS-Datei mit dem Namen **"styles.css"** und binden Sie diese in Ihre HTML-Seite ein. Die CSS-Datei soll folgende Stile enthalten:

- Die Hintergrundfarbe der Seite soll hellgrau (#f0f0f0) sein.
- Die Textfarbe aller Überschriften (h1) soll dunkelblau (#003366) sein.
- Alle Absätze (p) sollen eine Schriftgröße von 16px und eine Schriftfarbe von dunkelgrau (#333333) haben.
- Die ungeordnete Liste soll keine Aufzählungszeichen anzeigen.

### Aufgabe 3: Erstellung eines Navigationsmenüs

Erstellen Sie in Ihrer HTML-Seite ein Navigationsmenü mit folgenden Links:

- **"Home"** (verlinkt auf die aktuelle Seite)
- **"Über mich"** (verlinkt auf eine neue Seite **"about.html"**, die Sie ebenfalls erstellen sollen)
- **"Kontakt"** (verlinkt auf eine neue Seite **"contact.html"**, die Sie ebenfalls erstellen sollen)

Das Navigationsmenü soll mit einer CSS-Klasse **"nav"** gestaltet werden. Die Links sollen horizontal nebeneinander angeordnet sein und einen Abstand von 20px zueinander haben.

### Aufgabe 4: Formulare und Benutzerinteraktionen

Erstellen Sie auf der **"contact.html"**-Seite ein einfaches Kontaktformular mit folgenden Feldern:

- Name (Textfeld)
- E-Mail (Textfeld)
- Nachricht (Textbereich)
- Absenden-Button

Stylen Sie das Formular mit CSS:

- Die Textfelder und der Textbereich sollen eine Breite von 100% und eine Höhe von 30px haben.
- Der Absenden-Button soll eine Hintergrundfarbe von grün (#28a745) und eine weiße Schriftfarbe haben.

### Aufgabe 5: Responsive Design

Machen Sie Ihre HTML-Seite responsive, indem Sie folgendes CSS hinzufügen:

- Die maximale Breite der Seite soll 800px betragen und zentriert auf dem Bildschirm angezeigt werden.
- Für Bildschirme, die kleiner als 600px sind, soll das Navigationsmenü vertikal angezeigt werden.

## Musterlösung

### HTML-Datei (index.html)

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine erste Webseite</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="nav">
        <a href="index.html">Home</a>
        <a href="about.html">Über mich</a>
        <a href="contact.html">Kontakt</a>
    </nav>
    <h1>Willkommen auf meiner Webseite</h1>
    <p>Hallo! Mein Name ist Max Mustermann und ich bin Webentwickler. Hier ist ein Bild von mir:</p>
    <img src="https://via.placeholder.com/150" alt="Bild von Max Mustermann">
    <h2>Meine Hobbys</h2>
    <ul>
        <li>Programmieren</li>
        <li>Lesen</li>
        <li>Reisen</li>
    </ul>
</body>
</html>

### aboutHTML
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Über mich</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="nav">
        <a href="index.html">Home</a>
        <a href="about.html">Über mich</a>
        <a href="contact.html">Kontakt</a>
    </nav>
    <h1>Über mich</h1>
    <p>Hier können Sie mehr über mich erfahren...</p>
</body>
</html>


### contactHTML
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontakt</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="nav">
        <a href="index.html">Home</a>
        <a href="about.html">Über mich</a>
        <a href="contact.html">Kontakt</a>
    </nav>
    <h1>Kontakt</h1>
    <form>
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required><br>
        <label for="email">E-Mail:</label>
        <input type="email" id="email" name="email" required><br>
        <label for="message">Nachricht:</label>
        <textarea id="message" name="message" rows="5" required></textarea><br>
        <button type="submit">Absenden</button>
    </form>
</body>
</html>

### stylesCSS
´´´css
body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

h1 {
    color: #003366;
}

p {
    font-size: 16px;
    color: #333333;
}

ul {
    list-style-type: none;
}

.nav {
    display: flex;
    justify-content: space-around;
    margin-bottom: 20px;
}

.nav a {
    text-decoration: none;
    color: #003366;
    margin: 0 20px;
}

@media (max-width: 600px) {
    .nav {
        flex-direction: column;
        align-items: center;
    }

    .nav a {
        margin: 10px 0;
    }
}

### zuätzliches-stylesCSS
´´´css
form {
    display: flex;
    flex-direction: column;
}

label {
    margin-top: 10px;
}

input[type="text"], input[type="email"], textarea {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
}

button {
    background-color: #28a745;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    margin-top: 10px;
}

button:hover {
    background-color: #218838;
}
