# Ex.07 Design of Interactive Image Gallery
## Date:17/03/2026

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

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

## PROGRAM:
```

<!DOCTYPE html>
<html>
<head>
<title>Image Gallery</title>

<style>
body{
    text-align:center;
    font-family:Arial;
    background-color:#f2f2f2;
}

h2{
    margin-top:30px;
    color:#c12c2c;
}

.gallery-box{
    margin-top:50px;
}

img{
    width:420px;
    height:320px;
    border-radius:18px;
    margin:0 40px;
}

button{
    padding:12px 20px;
    font-size:18px;
    border:none;
    background-color:#2fe058;
    color:rgb(249, 226, 226);
    border-radius:7px;
    cursor:pointer;
}

button:hover{
    background-color:#0d3216;
}

/* Footer text */
.credit{
    margin-top:60px;
    font-size:16px;
    color:#555;
}
</style>

</head>

<body>

<h2>Interactive Image Gallery</h2>

<div class="gallery-box">
    <button onclick="prevImage()">Previous</button>

    <img id="galleryImage">

    <button onclick="nextImage()">Next</button>
</div>

<script>
let images = [
    "pic4.jpeg",
    "pic1.jpeg",
    "pic2.jpeg",
    "pic3.jpeg",
    "pic5.jpeg"
];

let index = 0;

function showImage(){
    document.getElementById("galleryImage").src = images[index];
}

function nextImage(){
    index++;
    if(index >= images.length){
        index = 0;
    }
    showImage();
}

function prevImage(){
    index--;
    if(index < 0){
        index = images.length - 1;
    }
    showImage();
}

// Load first image on page start
showImage();
</script>

<p class="credit">Created by Iraiyarul.D.R</p>

</body>
</html>
```
## OUTPUT:
<img width="1880" height="1074" alt="image" src="https://github.com/user-attachments/assets/1c8fe58a-5b7a-4fbc-95c6-a9b77386ce55" />

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
