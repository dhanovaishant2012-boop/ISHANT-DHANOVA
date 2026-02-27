
<html>
<head>
    <title>My Website</title>

    <meta name="description" content="Ishant Dhanova personal website. Learning coding and building websites.">
    <meta name="keywords" content="Ishant Dhanova, coding, HTML, Python, student developer">
    <meta name="author" content="Ishant Dhanova">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
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

    <h3>Online Python Compiler</h3>

<textarea id="code" rows="10" style="width:100%;">
print("Hello Ishant!")
</textarea>
<br><br>

<button onclick="runPython()">Run Code</button>

<pre id="output" style="background:black;color:lime;padding:10px;"></pre>

<script src="https://cdn.jsdelivr.net/pyodide/v0.25.1/full/pyodide.js"></script>

<script>
let pyodideReady = false;
let pyodide;

async function loadPyodideAndPackages() {
    pyodide = await loadPyodide();
    pyodideReady = true;
}

loadPyodideAndPackages();

async function runPython() {
    if (!pyodideReady) {
        alert("Python is loading... please wait.");
        return;
    }

    let code = document.getElementById("code").value;
    try {
        let result = await pyodide.runPythonAsync(code);
        document.getElementById("output").textContent = result ?? "Code executed.";
    } catch (err) {
        document.getElementById("output").textContent = err;
    }
}
</script>

<body>

<header>Welcome to My Website</header>

<div class="container">

<div class="card">
    <h2>About Me</h2>
    <p>Hi! My name is Ishant Dhanova.</p>
    <p>I am a student and I love learning coding.</p>
    <p>I enjoy building websites and learning Python.</p>
    <p>My goal is to become a software developer in the future 🚀</p>
</div>

<div class="card">
    <h2>My School</h2>
    <p>I study at <strong>Dewan Public School Hapur</strong>, a well‑known school in Hapur that focuses on excellent education and character development.</p>
    <p>At Dewan Public School Hapur, students are encouraged to learn new things, take part in activities, and grow into confident individuals.</p>
    <p>The school offers a balanced education with a strong emphasis on academics, sports, arts, and cultural activities.</p>
    <p>I enjoy studying here because of the friendly teachers, supportive classmates, and many opportunities to learn and improve myself every day.</p>
</div>

   <div class="card">
    <h2>My Hobbies</h2>
    <p>🎮 Gaming</p>
    <p>💻 Coding</p>
    <p>📚 Learning new technology</p>
</div> 

<div class="card">
    <h2>Contact Me</h2>
    <p>Click the Gmail icon to send me a message:</p>

    <a href="mailto:dhanovaishant2012@gmail.com?subject=Message from My Website">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Gmail_Icon.png" 
             width="80" 
             style="cursor:pointer;">
    </a>
</div>

    <div class="card">
        <h2>Contact</h2>
        <p>Email: dhanovaishant2012@email.com</p>
        <button onclick="alert('Thanks for visiting!')">Click Me</button>
    </div>

    <img src="photo.jpg" width="150" style="border-radius:50%;">

</div>

</body>
</html>
