**📝 To-Do List Web App (Vanilla JavaScript)
**📌 Description:**
This is a simple and responsive To-Do List Web Application built using HTML, CSS, and Vanilla JavaScript (no frameworks). The app allows users to add tasks, mark them as complete, and remove them from the list. It's designed for ease of use, instant feedback, and a clean UI — perfect for practicing DOM manipulation and event handling in JavaScript.

**🎯 Features:**
✅ Add Tasks — Type a task and click Add to insert it into the list.
📝 Mark as Complete — Click on a task’s text to toggle it as completed (with strikethrough).
❌ Remove Tasks — Click the Remove button to delete a task instantly.
⚡ Instant Updates — UI updates in real-time without any page reloads.
💻 Responsive Design — Works well on desktops, tablets, and mobiles.

**🛠️ Tools Used:**
HTML5 – For structure
CSS3 – For styling and responsiveness
JavaScript (ES6) – For interactivity and DOM manipulation

**InterView Questions:**
**1. How do you select elements in the DOM?**
You can select elements in the DOM using various methods:
document.getElementById('id') – Selects an element by its ID.
document.getElementsByClassName('class') – Selects elements by class name (returns a collection).
document.getElementsByTagName('tag') – Selects elements by tag name.
document.querySelector('selector') – Selects the first element matching the CSS selector.
document.querySelectorAll('selector') – Selects all elements matching the CSS selector (returns a NodeList).

**2. What are event listeners?**
Event listeners are functions that run when a specific event occurs on an element (like click, hover, keypress, etc.).
element.addEventListener('click', function() {
  alert('Element clicked!');
});

**3. Explain event delegation.**
Event delegation is a technique where you add a single event listener to a parent element instead of adding it to each child. It works by using event bubbling.
document.getElementById('parent').addEventListener('click', function(e) {
  if (e.target.matches('.child')) {
    console.log('Child element clicked!');
  }
});

**4. How do you prevent default behavior in JS?**
Use event.preventDefault() to stop the default behavior of an element (like submitting a form or following a link).
document.querySelector('form').addEventListener('submit', function(e) {
  e.preventDefault();
  console.log('Form submission prevented!');
});

**5. What is the difference between var, let, and const?**
var: Function-scoped, can be re-declared and updated.
let: Block-scoped, cannot be re-declared but can be updated.
const: Block-scoped, cannot be re-declared or updated.
var x = 5;
let y = 10;
const z = 15;

**6. How does bubbling and capturing work in events?**
When an event occurs:
Capturing Phase: The event travels from the root to the target.
Bubbling Phase: The event bubbles back from the target to the root.
You can specify the phase using the third parameter in addEventListener.
element.addEventListener('click', handler, true); // Capturing
element.addEventListener('click', handler, false); // Bubbling (default)

**7. How do you add and remove classes in JS?**
Use the classList API:
element.classList.add('new-class');
element.classList.remove('old-class');
element.classList.toggle('active'); // Adds if not present, removes if present

**8. What is closure in JavaScript?**
A closure is a function that "remembers" the variables from its outer scope, even after the outer function has finished executing.
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2

**9. Explain arrow functions.**
Arrow functions are a shorter syntax for writing functions. They do not bind their own this.
// Regular function
function add(a, b) {
  return a + b;
}

// Arrow function
const add = (a, b) => a + b;

10. What is the difference between == and ===?
== (loose equality): Compares values after type conversion.
=== (strict equality): Compares values without type conversion (types must match).
'5' == 5   // true
'5' === 5  // false
