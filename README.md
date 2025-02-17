<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript Assignment</title>
    <style>
        
        #circle {
            position: relative;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: red;
        }

        
        .image {
            width: 200px;
            height: 150px;
            margin: 10px;
            border: none;
        }

        .enlarged {
            width: 240px;
            height: 180px;
            border: 5px solid red;
        }
    </style>
</head>
<body>
    <h1 id="heading">Welcome to my Page</h1>
    <p id="paragraph" style="background-color: rgb(11, 244, 38);">What comes first, chicken or the egg?</p>
    <p><button id="change-content-button">Change Content</button></p>

    <img class="image" src="https://media.istockphoto.com/id/689936364/photo/funny-runnigh-chicken-in-bio-farm.jpg?s=612x612&w=0&k=20&c=Lv0IW_ZlvIT2cU-DylL7rKjlZTxTdp7EC8aTd4cNSt8=" alt="Image 1">
    <img class="image" src="data:image/jpeg;base64,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" alt="Image 2">
    <img class="image" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSmSw-eiZMO8oy3wiplbklM7EwO2V7Wz0JX8A&s" alt="Image 3">

    <div id="circle"></div>

    <form>
        <label for="name">What is your Name?:</label>
        <input type="text" id="name" name="name"><br><br>
        <label for="age">Do I dare ask how old you are?:</label>
        <input type="number" id="age" name="age">
        <p id="feedback"></p>
    </form>

    <script>
               document.getElementById("change-content-button").addEventListener("click", function() {
            document.getElementById("heading").innerHTML = "Content Updated!";
            document.getElementById("paragraph").innerHTML = "Yep...Nobody knows";
            document.getElementById("paragraph").style.backgroundColor = "lightblue";
        });

               let images = document.getElementsByClassName("image");
        for (let i = 0; i < images.length; i++) {
            images[i].addEventListener("click", function() {
                if (this.classList.contains("enlarged")) {
                    this.classList.remove("enlarged");
                } else {
                    this.classList.add("enlarged");
                }
            });
        }

       
        let circle = document.getElementById("circle");
        document.addEventListener("mousemove", function(event) {
            circle.style.top = event.clientY + "px";
            circle.style.left = event.clientX + "px";
            circle.style.backgroundColor = getRandomColor();
        });

        function getRandomColor() {
            let letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }

        
        document.getElementById("age").addEventListener("input", function() {
            let age = parseInt(this.value);
            if (isNaN(age)) {
                document.getElementById("feedback").innerHTML = "You're how old?";
            } else if (age < 18) {
                document.getElementById("feedback").innerHTML = "You are a minor.";
            } else {
                document.getElementById("feedback").innerHTML = "You are an adult.";
            }
        });
    </script>
</body>
</html>
