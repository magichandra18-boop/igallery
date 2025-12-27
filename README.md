# Ex.08 Design of Interactive Image Gallery
## Date:27/12/25

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
    <title>Interactive Image Gallery</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background: #f4f4f4;
        margin: 0;
        padding: 20px;
      }

      h1 {
        text-align: center;
      }

      .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 15px;
        max-width: 1000px;
        margin: auto;
      }

      .gallery img {
        width: 100%;
        height: 200px;
        object-fit: cover;
        cursor: pointer;
        border-radius: 10px;
        transition: transform 0.3s, box-shadow 0.3s;
      }

      .gallery img:hover {
        transform: scale(1.05);
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
      }

      /* Popup */
      .popup {
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.8);
        justify-content: center;
        align-items: center;
      }

      .popup img {
        max-width: 90%;
        max-height: 90%;
        border-radius: 10px;
      }

      .popup span {
        position: absolute;
        top: 20px;
        right: 30px;
        font-size: 30px;
        color: white;
        cursor: pointer;
      }
    </style>
  </head>
  <body>
    <h1>My Image Gallery</h1>

    <div class="gallery">
      <img src="a.png" onclick="openPopup(this.src)" />
      <img src="b.png" onclick="openPopup(this.src)" />
      <img src="c.png" onclick="openPopup(this.src)" />
    </div>

    <div class="popup" id="popup">
      <span onclick="closePopup()">✖</span>
      <img id="popupImg" />
    </div>

    <script>
      function openPopup(src) {
        document.getElementById("popup").style.display = "flex";
        document.getElementById("popupImg").src = src;
      }

      function closePopup() {
        document.getElementById("popup").style.display = "none";
      }
    </script>
  </body>
</html>
```

## OUTPUT:
<img width="1682" height="726" alt="Screenshot 2025-12-27 124020" src="https://github.com/user-attachments/assets/9598168d-aa20-44a7-b5b5-a8277076e2be" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
