🌡️ Temperature Converter
A sleek, responsive web utility built with Vanilla JavaScript that allows users to seamlessly convert temperatures between Celsius and Fahrenheit. This project highlights the core principles of functional programming and real-time DOM updates.

🚀 How It Works: The Logic Flow

The application follows a simple but effective Input ➔ Process ➔ Output model.

1. Data Capture (The Input)
When the user clicks the Submit button, the convert() function is triggered. It first grabs the value from the numeric input field:
The Problem: Values from HTML inputs are always strings by default.
The Logic: We use Number(textbox.value) to explicitly convert that string into a numeric type so we can perform mathematical operations.

2. Decision Making (The Process)The app uses an If-Else conditional block to determine which mathematical formula to apply based on the user's radio button selection:
Celsius to Fahrenheit:$$temp = (Celsius \times \frac{9}{5}) + 32$$
Fahrenheit to Celsius:$$temp = (Fahrenheit - 32) \times \frac{5}{9}$$

3. Data Formatting & Rendering (The Output)
To ensure the UI looks professional, the result is processed before being displayed:
Precision: We use .toFixed(1) to round the result to one decimal place, preventing long, messy strings of numbers (e.g., 37.7777778 becomes 37.8).
DOM Injection: The script targets the <p id="result"> element and updates its textContent to show the final value with the appropriate unit symbol.

🛠️ Tech Stack & File Structure

HTML5: Structured the form using semantic elements like <label>, <input type="radio">, and <button>.
CSS3: Styled with a modern HSL color palette, using box-shadow for depth and a responsive max-width layout for the form container.
Vanilla JavaScript: Handles the core logic, calculations, and event listeners without any external libraries.

├── index.html   # The UI structure
├── style.css    # Modern styling and layout
└── server.js   # Logical engine and DOM manipulation

💡 Key Programming Concepts Used

Event Handling: Utilizing onclick to bridge the HTML button and JS logic.
Variable Scoping: Using let for the temp variable to allow value reassignment during calculation.
Type Conversion: Turning string input into usable numbers.
Conditional Statements: Handling multiple user choices and providing an error message if no unit is selected.
