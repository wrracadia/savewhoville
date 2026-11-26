<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Christmas Secret</title>
<style>
    body {
        font-family: Georgia, serif;
        text-align: center;
        background: #f5f8f5;
        color: #333;
        padding: 50px 20px;
    }
 
    .container {
        max-width: 500px;
        margin: auto;
    }
 
    input {
        padding: 10px;
        width: 220px;
        font-size: 1rem;
        margin: 10px 0;
    }
 
    button {
        padding: 10px 20px;
        font-size: 1rem;
        cursor: pointer;
    }
 
    .error {
        color: darkred;
        margin-top: 10px;
    }
 
    #poemPage {
        display: none;
    }
</style>
</head>
<body>
 
<div id="loginPage" class="container">
    <h1>  Christmas Challenge  </h1>
    <p><strong>What is the magic of Christmas?</strong></p>
 
    <input
        type="text"
        id="password"
        placeholder="Enter your answer..."
        autocomplete="off">
 
    <br>
 
    <button onclick="checkPassword()">Unlock</button>
 
    <div id="error" class="error"></div>
</div>
 
<div id="poemPage" class="container">
    <h1>  Access Granted  </h1>
 
    <p>
        At Christmas time we laugh and share,<br>
        With those we love and know are there.<br>
        Through every season, near or far,<br>
        Family is the brightest star.
    </p>
</div>
 
<script>
function checkPassword() {
    const answer = document
        .getElementById("password")
        .value
        .trim()
        .toLowerCase();
 
    if (answer === "family") {
        document.getElementById("loginPage").style.display = "none";
        document.getElementById("poemPage").style.display = "block";
    } else {
        document.getElementById("error").textContent =
            "  That's not the magic of Christmas. Try again.";
    }
}
</script>
 
</body>
</html>
 


