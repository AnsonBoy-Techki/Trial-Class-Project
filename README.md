Below are the steps to build the website
Copy Paste step by step to understand how HTML & CSS works


//STEP 1
//Write HTML Structure
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Title</title>
</head>
<body>
</body>
</html>

//Step 2
//Change the Title
 <title>Favourite Cartoon</title>

 //Step 3
 // Write a Header
 <h1>My Favourite Cartoon</h1>

 //Step 4
 //Add CSS for body, h1, p
 <style>
     body {
            background: #11223c;
            font-family: 'zilla slab', sans-serif;

        }

        h1 {
            text-align: center;
            color: yellow;
            padding-top: 50px;
        }

        p {
            color: white;
            text-align: center;
        }
 </style>

//Step 5
//Add Image
<img src="https://my.kumonglobal.com/wp-content/uploads/2022/03/Learn-from-Rowan-Atkinson_Kumon-Malaysia_530x530_NewsThumbnail.jpg" alt="Mr Bean" />

//Step 6
// Write the cartoon name and main character name
<h1>Mr Bean</h1>
<p>by Rowan Atkinson</p>

//Step 7
//Make 2 Div groups and name the first one as "thefront" and second as "theback"
//put image into "thefront" and names into "theback"
<div class="thefront">
    <img src="https://my.kumonglobal.com/wp-content/uploads/2022/03/Learn-from-Rowan-Atkinson_Kumon-Malaysia_530x530_NewsThumbnail.jpg"
        alt="Mr Bean" />
</div>

<div class="theback">
    <h1>Mr Bean</h1>
    <p>by Rowan Atkinson</p>
</div>

//Step 8
//Add Container and card 
//put "thefront" and "theback" inside them
<div class="maincontainer"> //name the container as "maincontainer"
<div class="thecard"> //name the card as "thecard"

<div class="thefront">
    <img src="https://my.kumonglobal.com/wp-content/uploads/2022/03/Learn-from-Rowan-Atkinson_Kumon-Malaysia_530x530_NewsThumbnail.jpg"
        alt="Mr Bean" />
</div>

<div class="theback">
    <h1>Mr Bean</h1>
    <p>by Rowan Atkinson</p>
</div>

</div>
</div>


Step 9
//Add the balance CSS inside style tag for containers, card and images

/* THE MAINCONTAINER HOLDS CARD */
    .maincontainer {
        position: absolute;
        width: 250px;
        height: 320px;
        background: none;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    /* THE CARD HOLDS THE FRONT AND BACK FACES */
    .thecard {
        width: 100%;
        height: 100%;
        border-radius: 10px;
        transform-style: preserve-3d;
        transition: all 0.8s ease;
        margin-top: 50px;
        margin-bottom: 50px;
    }

    /* THE PSUEDO CLASS CONTROLS THE FLIP ON MOUSEOVER AND MOUSEOUT */
    .thecard:hover {
        transform: rotateY(180deg);
        cursor: pointer;
    }

    /* THE FRONT FACE OF THE CARD, WHICH SHOWS BY DEFAULT */
    .thefront {
        position: absolute;
        width: 100%;
        height: 100%;
        border-radius: 10px;
        backface-visibility: hidden;
        overflow: hidden;
        background: #ffc728;
        color: #000;
    }

    /* THE BACK FACE OF THE CARD, WHICH SHOWS ON MOUSEOVER */
    .theback {
        width: 100%;
        height: 100%;
        border-radius: 10px;
        backface-visibility: hidden;
        overflow: hidden;
        background: black;
        color: yellow;
        text-align: center;
        transform: rotateY(180deg);
        box-shadow: 5px 5px 30px 5px lightgray;
    }

    /*This block (starts here) is merely styling for the flip card, and is NOT an essential part of the flip code */
    .theback h1 {
        font-weight: bold;
        font-size: 24px;
        text-align: center;
    }

    .thefront img {
        width: 100%;
        height: 100%;
        object-fit: fill;

    }







