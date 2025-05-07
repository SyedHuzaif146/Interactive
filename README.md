# Ex.08 Design of Interactive Image Gallery
## Date:03.05.2025

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
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>THE UNIVERSE</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      background: #f2f2f2;
    }
    h1 {
      text-align: center;
      margin-bottom: 30px;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
    }
    .gallery img {
      width: 100%;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.3s;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }

    /* Modal styling */
    .modal {
      display: none;
      position: fixed;
      z-index: 999;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
    }
    .close, .prev, .next {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      font-size: 30px;
      color: white;
      background: rgba(0,0,0,0.5);
      border: none;
      padding: 10px;
      cursor: pointer;
    }
    .close {
      top: 10px;
      right: 20px;
      font-size: 35px;
      transform: none;
    }
    .prev { left: 20px; }
    .next { right: 20px; }
  </style>
</head>
<body>

  <h1>THE UNIVERSE</h1>

  <div class="gallery" id="gallery">
    <img src="image1.jpeg" alt="Image 1">
    <img src="image2.jpeg" alt="Image 2">
    <img src="image3.jpeg" alt="Image 3">
    <img src="image4.jpeg" alt="Image 4">
  </div>

  <!-- Modal -->
  <div class="modal" id="modal">
    <span class="close" id="closeBtn">&times;</span>
    <button class="prev" id="prevBtn">&#10094;</button>
    <img class="modal-content" id="modalImg" src="">
    <button class="next" id="nextBtn">&#10095;</button>
  </div>

  <script>
    const galleryImages = document.querySelectorAll("#gallery img");
    const modal = document.getElementById("modal");
    const modalImg = document.getElementById("modalImg");
    const closeBtn = document.getElementById("closeBtn");
    const prevBtn = document.getElementById("prevBtn");
    const nextBtn = document.getElementById("nextBtn");

    let currentIndex = 0;

    function showModal(index) {
      currentIndex = index;
      modal.style.display = "flex";
      modalImg.src = galleryImages[currentIndex].src;
    }

    galleryImages.forEach((img, i) => {
      img.addEventListener("click", () => showModal(i));
    });

    closeBtn.onclick = () => modal.style.display = "none";
    prevBtn.onclick = () => {
      currentIndex = (currentIndex - 1 + galleryImages.length) % galleryImages.length;
      modalImg.src = galleryImages[currentIndex].src;
    };
    nextBtn.onclick = () => {
      currentIndex = (currentIndex + 1) % galleryImages.length;
      modalImg.src = galleryImages[currentIndex].src;
    };

    window.onclick = (e) => {
      if (e.target === modal) modal.style.display = "none";
    };
  </script>

</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot (43).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
