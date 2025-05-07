## Ex.08 Design of Interactive Image Gallery
## NAME= SYED HUZAIF
## REG-NO= 212224240166
## Date:7.5.25

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>chennai-Vadapalani</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-04-16 105442.png" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-04-16 105931.png"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-04-16 105931.png" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="Screenshot 2025-04-16 111003.png" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>

```

## OUTPUT:
![alt text](image-1.png)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
