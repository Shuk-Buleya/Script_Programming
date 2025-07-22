### Step-by-Step Practice Exercise: JavaScript Basics  

**Objective**: Create an HTML file linked to a JavaScript file that logs messages, uses comments, prompts for user input, and generates random numbers.  

---

#### **Step 1: Set Up Files**  
1. **Create `index.html`**:  
   ```html
   <!DOCTYPE html>
   <html>
   <head>
     <title>JavaScript Practice</title>
   </head>
   <body>
     <h1>Open the console to see results!</h1>
     <!-- Link to external JS file -->
     <script src="script.js"></script>
   </body>
   </html>
   ```

2. **Create `script.js`**:  
   (This file will hold your JavaScript code.)

---

#### **Step 2: Write JavaScript Code**  
In `script.js`:  
1. **Log your name** and add a **multi-line comment**:  
   ```javascript
   /* 
   * script.js
   * Purpose: Practice JavaScript basics: logging, comments, user input, random numbers.
   */
   console.log("Alice"); // Replace "Alice" with your name
   ```

2. **Prompt for user input** and log the response:  
   ```javascript
   let userFeeling = prompt("How are you feeling today?");
   console.log("User is feeling: " + userFeeling);
   ```

3. **Generate a random number** between 1–100 and log it:  
   ```javascript
   let randomNum = Math.floor(Math.random() * 100) + 1;
   console.log("Random number: " + randomNum);
   ```

---

#### **Step 3: Test & Debug**  
1. Open `index.html` in your browser.  
2. **Check the console** (Right-click → *Inspect* → *Console*):  
   - You should see:  
     ```
     Alice
     User is feeling: [user's input]
     Random number: [e.g., 42]
     ```  
3. **Comment out code**:  
   - Temporarily disable the `console.log("Alice")` line by adding `//` at the start:  
     ```javascript
     // console.log("Alice"); 
     ```  
   - Refresh the page → Your name disappears from the console.  

---

#### **Step 4: Experiment**  
1. **Add a new variable**:  
   ```javascript
   let score = 0; // Initial score
   console.log("Score: " + score);
   ```  
2. **Update the score** with the random number:  
   ```javascript
   score = randomNum; 
   console.log("New score: " + score);
   ```  

---

#### **Final Code**  
`script.js`:  
```javascript
/* 
* script.js
* Practice: Logging, comments, user input, random numbers.
*/
// console.log("Alice"); // Commented out for debugging
let userFeeling = prompt("How are you feeling today?");
console.log("User is feeling: " + userFeeling);

let randomNum = Math.floor(Math.random() * 100) + 1;
console.log("Random number: " + randomNum);

let score = 0;
console.log("Initial score: " + score);

score = randomNum; // Update score with the random number
console.log("New score: " + score);
```

**Outcome**:  
- Browser shows a prompt asking for your mood.  
- Console logs:  
  ```
  User is feeling: [your input]
  Random number: 57
  Initial score: 0
  New score: 57
  ```  
