
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Number Form</title>
    <style>
        .container {
            width: 300px;
            margin: 50px auto;
            text-align: center;
        }
        input {
            padding: 10px;
            margin-bottom: 10px;
            width: 100%;
            box-sizing: border-box;
        }
        button {
            padding: 10px 20px;
            cursor: pointer;
        }
        .display {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Enter Contact Number</h2>
        <form id="contactForm">
            <input type="tel" id="contactNumber" placeholder="Enter your contact number" required>
            <button type="submit">Submit</button>
        </form>
        <div id="displayNumber" class="display"></div>
    </div>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const contactNumber = document.getElementById('contactNumber').value;
            document.getElementById('displayNumber').textContent = `Saved Number: ${contactNumber}`;
            document.getElementById('contactNumber').value = '';
        });
    </script>
</body>
</html>
