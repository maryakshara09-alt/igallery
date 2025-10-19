# Ex.08 Design of Interactive Image Gallery
## Date:15.10.2025

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
  <title>Photo Gallery</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>MARY AKSHARA (25009401) Gallery</h1>
  </header>

  <div class="gallery">
    
    <div class="photo"><img src="img.jpg1.png"  onclick="openModal(this)"></div>
    <div class="photo"><img src="img.jpg2.png"  onclick="openModal(this)"></div>
    <div class="photo"><img src="img.jpg3.png"  onclick="openModal(this)"></div>
    <div class="photo"><img src="img.jpg4.png"  onclick="openModal(this)"></div>
    <div class="photo"><img src="img.jpg5.png"  onclick="openModal(this)"></div>
    
    
  </div>

  <footer>
    <p>My Gallery App 
         Designed by MARY AKSHARA(25009401)</p>
  </footer>
  <div id="myModal" class="modal">
    <span class="close" onclick="closeModal()">&times;</span>
    <img id="modalImage" src="">
  </div>

  <script>
    function openModal(img) {
      const modal = document.getElementById("myModal");
      const modalImg = document.getElementById("modalImage");
      modal.style.display = "flex";
      modalImg.src = img.src;
    }

    function closeModal() {
      const modal = document.getElementById("myModal");
      modal.style.display = "none";
    }
     
    </script>
</body>
</html>
style.css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  background: #f3f4f6;
  color: #333;
}

 
header {
  text-align: center;
  padding: 30px 10px;
  background: linear-gradient(135deg, #4f46e5, #3b82f6);
  color: white;
  box-shadow: 0 2px 8px rgba(0,0,0,0.2);
}

header h1 {
  font-size: 2rem;
  letter-spacing: 1px;
}

 
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  padding: 30px;
}

.photo {
  overflow: hidden;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.photo:hover {
  transform: scale(1.03);
  box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.photo:hover img {
  transform: scale(1.1);
}

 
footer {
  text-align: center;
  padding: 15px 0;
  background: #111827;
  color: #f9fafb;
  font-size: 0.9rem;
}
 
.modal {
  display: none; 
  position: fixed; 
  z-index: 1000; 
  left: 0;
  top: 0;
  width: 100%; 
  height: 100%; 
  overflow: auto; 
  background-color: rgba(0,0,0,0.8); 
  justify-content: center;
  align-items: center;
}

.modal img {
  max-width: 90vw;
  max-height: 90vh;
  border-radius: 10px;
  box-shadow: 0 0 20px #000;
}

.close {
  position: absolute;
  top: 30px;
  right: 50px;
  color: #fff;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
  z-index: 1001;
}

```
## OUTPUT:
![alt text](<Screenshot (88)-1.png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
