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
>  - <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Example</title>
    <style>
        /* Default style for the heading */
        #dynamic-heading {
            color: teal;
            font-size: 24px;
        }

        .highlight {
            color: crimson;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <header>
        <h1 id="dynamic-heading">Welcome to JavaScript DOM Manipulation</h1>
    </header>

    <main>
        <p id="paragraph">This paragraph will change dynamically when you click the button below.</p>

        <button onclick="changeText()">Change Text</button>
        <button onclick="toggleStyle()">Toggle Style</button>
        <button onclick="addElement()">Add Element</button>
        <button onclick="removeElement()">Remove Element</button>

        <div id="container"></div>
    </main>

    <footer>
        <p>© 2025 DOM Project</p>
    </footer>

    <!-- Link external JavaScript -->
    <script src="script.js"></script>
</body>
</html>
// Function to change text content
function changeText() {
    const heading = document.getElementById("dynamic-heading");
    heading.textContent = "Text Changed! DOM is powerful!";
}

// Function to toggle a CSS class
function toggleStyle() {
    const heading = document.getElementById("dynamic-heading");
    heading.classList.toggle("highlight");
}

// Function to add a new paragraph
function addElement() {
    const newPara = document.createElement("p");
    newPara.textContent = "🟢 New paragraph added dynamically!";
    newPara.id = "new-paragraph";
    document.getElementById("container").appendChild(newPara);
}

// Function to remove the dynamically added paragraph
function removeElement() {
    const existingPara = document.getElementById("new-paragraph");
    if (existingPara) {
        existingPara.remove();
    } else {
        alert("No element to remove!");
    }
}



# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
