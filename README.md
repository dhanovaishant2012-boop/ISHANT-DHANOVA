<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f1f3f4;
            margin: 0;
            text-align: center;
        }

        header {
            background-color: #4285F4;
            color: white;
            padding: 20px;
            font-size: 28px;
        }

        .container {
            padding: 20px;
        }

        .card {
            background: white;
            max-width: 500px;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }

        h2 {
            color: #4285F4;
        }

        button {
            padding: 10px 15px;
            background-color: #4285F4;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #3367D6;
        }
    </style>
</head>
<body>

<header>Welcome to My Website</header>

<div class="container">

    <div class="card">
        <h2>About Me</h2>
        <p>Hello! My name is Ishant.</p>
        <p>I am learning coding and building websites.</p>
        <p>This website is hosted using GitHub Pages 🚀</p>
    </div>

    <div class="card">
        <h2>My Skills</h2>
        <p>✔ HTML</p>
        <p>✔ Python</p>
        <p>✔ GitHub</p>
    </div>

    <div class="card">
        <h2>Contact</h2>
        <p>Email: your@email.com</p>
        <button onclick="alert('Thanks for visiting!')">Click Me</button>
    </div>

</div>

</body>
</html>
