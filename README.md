# Ex.07 Design of Interactive Image Gallery
## Date:27.12.25

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
igallery.html:
<html>
    <head>
        <title>Image Gallery</title>
        <link href="style.css" rel="stylesheet">
        <script src="script.js" defer></script>
    </head>
    <body>
        <div class="head">
            <h1>Cartoon Image Gallery</h1>
        </div>
        <div class="box1">
            <div class="img">
                <img src="samosa.jpeg" id="image">
                <p id="caption" style="text-align: center;"><b>Samosa Motu</b></p>
            </div>
            <div class="dong">
                <input type="button" value="previous" id="button1">
                <input type="button" value="Next" id="button2">
            </div>
            
        </div>
        <h2>&copy; Rithik M (25014301)</h2>
    </body>
</html>

style.css:
*
{
    margin: 0%;
    padding: 0%;
}
.head
{
    border: 2px solid cyan;
    width: 100%;
    height: 45px;
    text-align: center;
    background-color: blue;
}
.head h1
{
    margin-bottom: 10px;
    color: whitesmoke;
}
.box1
{
    border: 2px solid black;
    border-radius: 7px;
    height: 390px;
    width: 450px;
    margin-top: 10%;
    margin-left: 550px;
    background: linear-gradient(cyan,black);
}
.img
{
    
    width: 250px;
    height: 200px;
    padding-bottom: 30px;
    padding-right: 50px;
    border-radius: 15px;
    margin-top: 35px;
    margin-left: 75px;
}
.box1 h3{
    margin-top: 30px;
    text-align: center;
}
#button1
{
    margin-left: 140px;
    margin-top: 20px;
    height: 30px;
    width: 70px;
    border: 1px solid blue;
    border-radius: 5px;
    background-color: blue;
    color: white;
}
#button2
{
    height: 30px;
    width: 70px;
    border: 1px solid blue;
    border-radius: 5px;
    background-color: blue;
    color: white;
    margin-left: 15px;
}
body
{
    background-image: url(bg.jpg);
    background-size: 100%;
}
#button2:hover
{
    cursor: pointer;
    background-color: black;
}
#button1:hover
{

    cursor: pointer;
    background-color: black;
}
h2{
    background-color: black;
    color: white;
    text-align: center;
    margin-top: 95px;
}
#image
{
    height: 230px;
    width: 300px;
    border: 2px solid black;
    margin-top: 15px;
    border-radius: 15px;
}
.dong
{
    margin-top: 30;
    margin-left: 7;
}
#caption{
    margin-top: 5;
    margin-left: 50px;
    color: aliceblue;

}

script.js:
var gallery = [
    { src: "gadget.jpeg", caption: "Paglu" },
    { src: "motu.jpeg", caption: "Motu" },
    { src: "patlu.jpeg", caption: "Patlu" },
    { src: "samosa.jpeg", caption: "Samosa Motu" },
];

var index = 0;
var imgElement = document.getElementById("image");
var captionElement = document.getElementById("caption");
var prevBtn = document.getElementById("button1");
var nextBtn = document.getElementById("button2");

function updateGallery() {
    imgElement.src = gallery[index].src;
    captionElement.textContent = gallery[index].caption;
}

button2.onclick = function() {
    index = (index + 1) % gallery.length;
    updateGallery();
}

button1.onclick = function() {
    index = (index - 1 + gallery.length) % gallery.length;
    updateGallery();
}

updateGallery();

```
## OUTPUT:
![alt text](<Screenshot 2025-12-27 083812.png>)
![alt text](<Screenshot 2025-12-27 083828.png>)
![alt text](<Screenshot 2025-12-27 083840.png>)
![alt text](<Screenshot 2025-12-27 083854.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
