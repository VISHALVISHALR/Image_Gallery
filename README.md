# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic Photo Showcase</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: url("m4.jpeg") no-repeat center center fixed;
            background-size: cover;
            position: relative;
            color: #fff;
        }

        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: -1;
        }

        h1 {
            background-color: rgba(76, 175, 80, 0.8);
            color: white;
            padding: 1rem;
            margin: 0;
            text-align: center;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
            border-radius: 10px;
            max-width: 600px;
            margin: 20px auto;
        }

        .gallery-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
            margin: 20px;
            background-color: rgba(255, 255, 255, 0.2);
            border-radius: 15px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        }

        .gallery-item {
            position: relative;
            width: 250px;
            height: 250px;
            border: 3px solid rgba(255, 255, 255, 0.8);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background-color: rgba(255, 255, 255, 0.2);
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .gallery-item:hover {
            transform: scale(1.05) rotate(3deg);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        #lightboxContent {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
        }

        #lightboxContent img {
            max-width: 90%;
            max-height: 70vh;
            border-radius: 8px;
            border: 2px solid #4CAF50;
        }

        .close-button {
            background-color: #ff4d4d;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 20px;
            transition: background-color 0.3s ease;
        }

        .close-button:hover {
            background-color: #e63939;
        }

        footer {
            background-color: rgba(30, 144, 255, 0.8);
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
            font-size: 14px;
            box-shadow: 0 -2px 6px rgba(0, 0, 0, 0.3);
        }
    </style>
    <script>
        function displayLightbox(imageSrc, imageAlt) {
            const lightbox = document.getElementById("lightbox");
            const lightboxImage = document.getElementById("lightboxImage");

            lightboxImage.src = imageSrc;
            lightboxImage.alt = imageAlt;
            lightbox.style.display = "flex";
        }

        function hideLightbox() {
            const lightbox = document.getElementById("lightbox");
            lightbox.style.display = "none";
        }
    </script>
</head>

<body>
    <h1>FOOTBALL PLAYERS SHOWCASE</h1>

    <div class="gallery-container">
        <div class="gallery-item">
            <img src="m1.jpg" alt="PLAYER 1" onclick="displayLightbox('m1.jpg', 'PLAYER 1')">
        </div>
        <div class="gallery-item">
            <img src="m2.jpg" alt="PLAYER 2" onclick="displayLightbox('m2.jpg', 'PLAYER 2')">
        </div>
        <div class="gallery-item">
            <img src="m3.jpg" alt="PLAYER 3" onclick="displayLightbox('m3.jpg', 'PLAYER 3')">
        </div>
    </div>

    <div id="lightbox">
        <div id="lightboxContent">
            <img id="lightboxImage" src="" alt="">
            <button class="close-button" onclick="hideLightbox()">Close</button>
        </div>
    </div>

    <footer>
        Design and Developed by vishal R(24900248)
    </footer>
</body>

</html>
```

## OUTPUT
![Screenshot 2025-05-15 214311](https://github.com/user-attachments/assets/f4a49a35-2605-4acc-bfe0-69305dc452e1)
![Screenshot 2025-05-15 214349](https://github.com/user-attachments/assets/c3c92797-5085-445d-99e4-9102ae923410)
![Screenshot 2025-05-15 214405](https://github.com/user-attachments/assets/07361808-66b0-46d6-805b-686958b33330)
![Screenshot 2025-05-15 214421](https://github.com/user-attachments/assets/873de9e4-9dfd-440a-adca-368dd8820717)




## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
