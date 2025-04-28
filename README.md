# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨



HTML (index.html)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Interactive Web Page</h1>
    </header>
    <main>
        <section>
            <p id="text">This text will change dynamically when you click the button.</p>
            <button onclick="changeText()">Change Text</button>
        </section>
        <section>
            <button onclick="toggleStyle()">Toggle Style</button>
            <button onclick="addElement()">Add New Element</button>
            <div id="dynamic-content"></div>
        </section>
    </main>
    <footer>
        <p>Created with ❤️ by [Your Name]</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>



CSS (styles.css)

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header, footer {
    text-align: center;
    background-color: #333;
    color: #fff;
    padding: 10px 0;
}

button {
    padding: 10px 20px;
    margin: 10px;
    cursor: pointer;
}

#dynamic-content {
    margin-top: 20px;
}

.styled {
    color: white;
    background-color: #007bff;
    font-weight: bold;
}
JavaScript (script.js)

// Change the text content dynamically
function changeText() {
    document.getElementById("text").textContent = "The text has been changed! 📝";
}

// Modify CSS styles dynamically
function toggleStyle() {
    const textElement = document.getElementById("text");
    textElement.classList.toggle("styled");
}

// Add a new element to the page dynamically
function addElement() {
    const newElement = document.createElement("p");
    newElement.textContent = "This is a new paragraph added to the page.";
    const dynamicContentDiv = document.getElementById("dynamic-content");
    dynamicContentDiv.appendChild(newElement);
}
