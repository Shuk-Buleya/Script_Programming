### **Logic Statements in JavaScript**

#### **Page 1 of 3**

### **1. Introduction: Making Code Make Decisions**
Until now, your code has run the same way every time. **Logic statements** change that. They let your code choose different paths based on conditions, making your programs dynamic and interactive.

**Key Concepts Covered:**
- `if` and `if else` statements
- `else if` statements
- Conditional ternary operator (`? :`)
- `switch` statements

---

### **2. `if` and `if else` Statements**
The most basic way to make a decision in code.

**Syntax:**
```javascript
if (condition) {
    // Code to run if the condition is TRUE
} else {
    // Code to run if the condition is FALSE (optional)
}
```

**How it Works:**
1. The `condition` inside the parentheses `()` is evaluated and converted to a Boolean (`true` or `false`).
2. If `true`, the code inside the `if` block `{}` runs.
3. If `false` and an `else` block exists, the code inside the `else` block runs.
4. Only one block will ever be executed.

**Practical Example:**
```javascript
let isRaining = true;

if (isRaining) {
    console.log("Take your umbrella! ☔");
} else {
    console.log("Enjoy the sunshine! ☀️");
}
// Output: "Take your umbrella! ☔"
```

**🚨 Common Pitfall: Assignment (=) vs. Comparison (==/===)**
A single equals sign `=` **assigns** a value, it doesn't **compare**.
```javascript
let hobby = "dancing";
if (hobby = "coding") { // WRONG! This assigns "coding" to hobby.
    console.log("I love coding too!");
}
// This will always run because the assignment succeeds, making the condition truthy.
```
**Always use `===` (strict equality) for comparisons in your conditions.**

---

### **3. `else if` Statements**
Use `else if` to check multiple conditions in sequence. The code will execute the block for the *first* true condition it finds and then skip the rest.

**Syntax:**
```javascript
if (condition1) {
    // Code if condition1 is true
} else if (condition2) {
    // Code if condition2 is true
} else if (condition3) {
    // Code if condition3 is true
} else {
    // Code if none of the above are true
}
```

**Practical Example: Ticket Price Calculator**
```javascript
let age = 25;
let cost;
let message;

if (age < 3) {
    cost = 0;
    message = "Free entry!";
} else if (age < 12) { // No need for (age >= 3 && age < 12) because the first 'if' already caught younger ages.
    cost = 5;
    message = "Child discount applied.";
} else if (age < 65) {
    cost = 10;
    message = "Standard adult price.";
} else {
    cost = 7;
    message = "Senior discount applied.";
}

console.log(message); // "Standard adult price."
console.log("Cost: $" + cost); // "Cost: $10"
```

**Why it's efficient:** The moment a true condition is found, the rest are ignored. This is cleaner and faster than writing multiple separate `if` statements.

---

### **4. The Ternary Operator (`? :`)**
A shortcut for a simple `if-else` statement. It's an operator that takes **three operands**, hence the name "ternary".

**Syntax:**
```javascript
condition ? expressionIfTrue : expressionIfFalse;
```
- Read the `?` as **"then"**.
- Read the `:` as **"else"**.

**Practical Example 1: Assigning a Value**
```javascript
let age = 20;
let canVote = (age >= 18) ? "Yes, you can vote!" : "No, too young.";
console.log(canVote); // "Yes, you can vote!"
```

**Practical Example 2: Executing an Action**
```javascript
let isMember = true;
isMember ? console.log("Welcome back!") : console.log("Please sign up!");
// Output: "Welcome back!"
```

**Use it for:** Quick, one-line decisions. For more complex logic with multiple steps, stick with `if-else`.

---

### **5. `switch` Statements**
Best used when you need to check one variable or expression against a long list of **specific values**. Much cleaner than a long chain of `else if` statements.

**Syntax:**
```javascript
switch (expression) {
    case value1:
        // Code to run if expression === value1
        break; // Crucial! Exits the switch block.
    case value2:
        // Code to run if expression === value2
        break;
    default:
        // Code to run if no cases match (like an 'else' clause)
        break;
}
```

**Practical Example: Daily Schedule**
```javascript
let activity = "Lunch";

switch (activity) {
    case "Get up":
        console.log("It's 6:30 AM");
        break;
    case "Breakfast":
        console.log("It's 7:00 AM");
        break;
    case "Lunch":
        console.log("It's 12:00 PM"); // This will run.
        break;
    case "Dinner":
        console.log("It's 6:30 PM");
        break;
    default:
        console.log("I don't know that activity.");
        break;
}
// Output: "It's 12:00 PM"
```

**⚡ The `break` keyword is critical!** It tells JavaScript to exit the `switch` block. If you forget it, code execution will **"fall through"** and run the code in the next case(s) until it hits a `break` or the end of the block.

**Combining Cases:** You can stack cases to run the same code for multiple values.
```javascript
let grade = "B";

switch (grade) {
    case "F":
    case "D":
        console.log("You failed. Try again.");
        break;
    case "C":
    case "B":
        console.log("You passed! Well done."); // This will run.
        break;
    case "A":
        console.log("Excellent! You aced it.");
        break;
    default:
        console.log("Unknown grade.");
}
// Output: "You passed! Well done."
```

---

### **6. Key Takeaways & Summary**

| Statement | Best Used For... | Example |
| :--- | :--- | :--- |
| **`if/else`** | Making one decision or a simple either/or choice. | `if (isLoggedIn) { welcome() } else { login() }` |
| **`else if`** | Choosing one option from several possible conditions. | Calculating ticket prices based on age ranges. |
| **Ternary `? :`** | Quick, one-line assignments or actions. | `let message = isError ? "Fail" : "Pass";` |
| **`switch`** | Comparing one expression against many specific values. | Handling a menu of commands (`"play"`, `"pause"`, `"stop"`). |

**Remember:**
- **Always use `===`** (strict comparison) in your conditions to avoid bugs.
- **Always include `break`** in each `case` of a `switch` statement unless you specifically want fall-through.
- Use **`default`** in a `switch` as a catch-all, similar to `else`.
- **Keep it readable.** A long `else if` chain is often better as a `switch`. A simple `if-else` is often clearer than a ternary.

### **Next Steps: Practice!**
Checkput the following mini project:
**Rock Paper Scissors:** Use `if` statements to compare player and computer choices from an array.
