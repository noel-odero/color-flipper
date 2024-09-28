
# Color Flipper

A simple web application that allows users to change the background color of the page to a random hexadecimal color code with the click of a button. This project demonstrates the use of Javascript for DOM manipulation and event handling.

## Table of Contents
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Code Explanation](#code-explanation)




## Technologies Used
- **HTML5**: Markup language for structuring the web page.
- **CSS3**: Styling language to improve the visual layout.
- **JavaScript**: Programming language to add interactivity.

## Features
- Click a button to change the background color to a random hexadecimal color.
- Displays the current color code on the webpage.
- Simple and intuitive user interface.

## Getting Started
To get a local copy up and running follow these simple steps:

1. **Clone the repository:**

   git clone https://github.com/noel-odero/color-flipper.git


2. **Navigate into the project directory:**

   cd color-flipper


3. **Open the `index.html` file in your web browser.**

## Usage
1. Click the "Click Me" button.
2. The background color of the page will change to a random color, and the color code will be displayed.

## Code Explanation
### HTML Structure
The HTML file sets up the basic structure of the application, including a navigation bar, a container for displaying the current color, and a button for generating the new color.

### JavaScript Functionality
- **Array of Hexadecimal Values**:

  const hex = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, "A", "B", "C", "D", "E", "F"];

  An array containing all possible characters for generating a hex color code.

- **Event Listener**


  btn.addEventListener('click', function() {
      // Code to generate and display a new color
  });

  Adds a click event listener to the button, triggering color generation when clicked.

- **Random Color Generation**:


  for (let i = 0; i < 6; i++) {
      hexColor += hex[getRandomNumber()];
  }

  A loop that constructs a new hexadecimal color by selecting random characters from the `hex` array.

- **Changing the Background Color**:

  document.body.style.backgroundColor = hexColor;

  Updates the background color of the document body to the newly generated color.

### Difference Between `getElementById` and `querySelector`
- **`getElementById`**: A method that selects an element by its unique ID. It returns a single element.


  const btn = document.getElementById('btn');


- **`querySelector`**: A more versatile method that selects the first element matching a specified CSS selector (can be a class, ID, or tag). It returns a single element.


  const color = document.querySelector(".color");
