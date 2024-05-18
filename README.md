# Quotesx
Webapp development for quotes x channel
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quote Sharing App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }
        textarea {
            width: 100%;
            height: 100px;
            resize: none;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .quote {
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            background-color: #f9f9f9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Quote Sharing App</h1>
        <textarea id="quoteInput" placeholder="Enter your quote here..."></textarea>
        <button onclick="postQuote()">Post Quote</button>
        <div id="quoteList"></div>
    </div>

    <script>
        function postQuote() {
            var quote = document.getElementById("quoteInput").value;
            if (quote.trim() !== "") {
                var quoteElement = document.createElement("div");
                quoteElement.classList.add("quote");
                quoteElement.textContent = quote;
                document.getElementById("quoteList").appendChild(quoteElement);
                document.getElementById("quoteInput").value = "";
            } else {
                alert("Please enter a quote!");
            }
        }
    </script>
</body>
</html>
