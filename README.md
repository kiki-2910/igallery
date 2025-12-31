# Ex.07 Design of Interactive Image Gallery
## Date:25/12/2025

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
<html>
<head>
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css"> 
</head>
<body>

    <div class="top-banner">Interactive Image Gallery</div>

    <div class="main-content">
        <div class="gallery-container">
            <img id="galleryImage" class="gallery-image" src="image1.jpeg ">
            <div id="caption" class="caption">Built-in Best Friends</div>
            <div class="gallery-buttons">
                <button onclick="prevImage()">Previous</button>
                <button onclick="nextImage()">Next</button>
            </div>
        </div>
    </div>

    <div class="footer-banner">
       Desinged & Developed by MOHAMED ARSATH - 25000358 &copy;
    </div>

    <script src="index.js"></script>
</body>
</html>

body {
    font-family: sans-serif;
    display: flex;
    flex-direction: column;
    height: 100;
    background-color: white;
}

.top-banner {
    background-color:beige;
    text-align: center;
    padding: 15px;
    font-size: 22px;
    font-weight: bold;
}

.main-content {
    display: flex;
    justify-content: center;
    align-items: center;
}

.gallery-container {
    background: brown;
    padding: 20px;
    border-radius: 15px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    text-align: center;
    width: 480px;
}

.gallery-image {
      width: 200px;
      margin: 10px;
      cursor: pointer;
      transition: transform 0.3s;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
}
    .gallery img:hover {
      transform: scale(1.1);
}

.caption {
    margin: 15px 0;
    font-size: 18px;
    font-weight: 500;
}

.gallery-buttons {
    display: flex;
    justify-content: center;
    gap: 10px;
}

button {
    padding: 10px 25px;
    cursor: pointer;
    border: none;
    border-radius: 5px;
    background-color: black;
    color: ivory;
    font-size: 16px;
}

.footer-banner {
    background-color: beige;
    color: rgb(86, 49, 3);
    text-align: center;
    padding: 10px;
    font-size: 14px;
}

const gallery = [
    { src: "image1.jpeg", caption: "Built-in Best Friends!" },
    { src: "image2.jpeg", caption: "Disorder since birth!" },
    { src: "image3.jpeg", caption: "Random from drafts!" },
    { src: "image4.jpeg", caption: "Goofy Gooses!" },
     { src: "image5.jpeg", caption: "All my favs!" },
];

let index = 0;

function updateGallery() {
    document.getElementById("galleryImage").src = gallery[index].src;
    document.getElementById("caption").textContent = gallery[index].caption;
}

function nextImage() {
    index++;
    if (index >= gallery.length) {
        index = 0;
    }
    updateGallery();
}

function prevImage() {
    index--;
    if (index < 0) {
        index = gallery.length - 1;
    }
    updateGallery();
}
```
## OUTPUT:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e738223d-e55d-4aa2-bb16-fc10987010dc" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2db8fcf7-1a77-4a97-9bd1-23bef1090ff0" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/77b2cd44-c8c6-4197-bde8-6a76dda5d6bc" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/840bdc83-5273-43d7-ad1f-0b1dfa993f1e" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5923e1ee-265e-4f88-a55b-eec176ee9d63" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
