<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personalized Greeting</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .greeting {
            margin-top: 20px;
            font-size: 18px;
            color: green;
        }
        .error {
            margin-top: 20px;
            font-size: 18px;
            color: red;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Personalized Greeting</h1>
    <label for="name">Enter your name:</label>
    <input type="text" id="name" name="name">
    <button onclick="displayGreeting()">Submit</button>
    <div id="message"></div>
</div>

<script>
    function displayGreeting() {
        var name = document.getElementById("name").value;
        var message = document.getElementById("message");
        message.innerHTML = "";  // Clear previous messages

        if (name.trim() === "") {
            message.innerHTML = "<span class='error'>Please enter your name.</span>";
        } else {
            message.innerHTML = "<span class='greeting'>Hello, " + name + "!</span>";
        }
    }
</script>

</body>
</html>
