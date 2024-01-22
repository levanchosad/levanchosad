<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        #firstButton, #secondButton {
            display: block;
        }

        #secondButton {
            display: none;
        }
    </style>
    <title>Date Invitation</title>
</head>
<body>

    <button id="firstButton" onclick="handleButtonClick('firstButton')">Ask for a Date</button>
    <button id="secondButton" onclick="handleButtonClick('secondButton')">Ask Again</button>

    <script>
        function handleButtonClick(buttonId) {
            var response = prompt("Hey there! I've really enjoyed our time together, and I was wondering if you'd like to go on a date with me. What do you say? (Type 'yes' or 'no')").toLowerCase();

            if (response === 'yes') {
                alert("That's great! I'm looking forward to it.");
                document.getElementById(buttonId).style.display = 'none';
            } else if (response === 'no') {
                alert("No worries! If you ever change your mind, feel free to let me know.");
                document.getElementById(buttonId).style.display = 'none';
                document.getElementById('secondButton').style.display = 'block';
            } else {
                alert("Sorry, I didn't understand your response. Please type 'yes' or 'no.'");
            }
        }
    </script>

</body>
</html>
