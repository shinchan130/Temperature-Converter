# Temperature-Converter
Easily convert between Celsius, Fahrenheit, and Kelvin with our user-friendly temperature converter. Whether you're checking the weather, cooking, or working on a science project, get accurate and instant results every time.
🌐 HTML (Structure of the Page)
<!DOCTYPE html>
This tells the browser that the document is using HTML5.

<html lang="en">
This starts the HTML document and sets the language to English.

<head>...</head>
This section contains meta information like:

charset="UTF-8": allows a wide range of characters (including symbols and letters from different languages).

viewport: makes the layout responsive on mobile.

<title>: gives the page a title (shown in the browser tab).

<style>: contains internal CSS for page styling.

<body>...</body>
Everything visible on the page is placed inside this section.

<h1>Temperature Converter</h1>
This is a large heading at the top of your page.

<div id="contenar">
This is a container box for the input fields (spelled “contenar” — it should ideally be “container”).

Inside it:

You have two div blocks (class: input-div). Each one holds:

An input field for numbers (temperature).

A text input that shows the unit (Celsius or Fahrenheit) but is read-only.

🎨 CSS (Page Styling)
body
Adds padding around the whole page to give breathing room.

h1
Centers the main heading on the page.

#contenar
Applies background color, padding, and centers the content inside the container.

.input-div
Displays each temperature input box side-by-side (inline-block).

.inp
Styles the main input boxes:

Border and border radius (rounded top corners).

Text is black, large size (180%).

Fixed height and width.

Centered text.

No outline (removes blue border when clicked).

.inp2
Styles the read-only labels below the main input:

Same width.

Lighter background.

Smaller height and font.

No outline.

🧠 JavaScript (Interactive Functionality)
This part makes the converter actually work.

let cel = document.getElementById("cel");
Grabs the Celsius input box from the page.

let fah = document.getElementById("fah");
Grabs the Fahrenheit input box from the page.

cel.addEventListener("input", function () {...})
Listens for any input in the Celsius box:

Converts the number to Fahrenheit using the formula:
F = (C × 9/5) + 32

If it's a decimal, rounds to 4 digits.

Updates the Fahrenheit input with the result.

fah.addEventListener("input", function () {...})
Listens for any input in the Fahrenheit box:

Converts the number to Celsius using the formula:
C = (F − 32) × 5/9

If it's a decimal, rounds to 4 digits.

Updates the Celsius input with the result.

