# **Short Notes on Variables and Operators in JavaScript**  

## **Variables**  

### **What are Variables?**  
Variables store data that can change while the code runs. They make code dynamic.  

**Example:**  
```javascript
let firstName = "Shukran";  
let age = 25;  
```  
- `firstName` can later be updated to `"Husna"`.  
- Without variables, code would do the same thing every time.  

### **Declaring Variables**  
- Use `let`, `var`, or `const` to declare.  
- `let` and `var` can be reassigned.  
- `const` cannot be reassigned (constant).  

**Example:**  
```javascript
let city = "Paris";  
city = "Berlin";  // Valid  
const PI = 3.14;  
PI = 3.15;       // Error!  
```  

### **Naming Variables**  
- Start with lowercase (`age`, `userName`).  
- Use **camelCase** (`ageOfUser`).  
- No spaces or special characters (except `_`).  

### **Primitive Data Types**  
JavaScript has 7 primitive types:  
1. **String** – Text (`"Hello"`, `'Hi'`, `` `Hi ${name}` ``).  
2. **Number** – Integers (`5`), decimals (`3.14`), etc.  
3. **BigInt** – Large integers (`12345678901234567890n`).  
4. **Boolean** – `true` or `false`.  
5. **Symbol** – Unique identifiers (`Symbol("id")`).  
6. **Undefined** – Not assigned (`let x;` → `x` is `undefined`).  
7. **Null** – Explicitly empty (`let y = null;`).  

**String Examples:**  
```javascript
let name = "Alice";  
let msg = `Hello, ${name}`;  // Template string  
```  

**Escape Characters:**  
- `\n` → New line  
- `\"` → Double quote in a string  
- `\\` → Backslash  

---

## **Operators**  

### **Arithmetic Operators**  
| Operator | Example | Result |  
|----------|---------|--------|  
| `+` (Addition) | `5 + 3` | `8` |  
| `-` (Subtraction) | `5 - 3` | `2` |  
| `*` (Multiplication) | `5 * 3` | `15` |  
| `/` (Division) | `6 / 3` | `2` |  
| `**` (Exponent) | `2 ** 3` | `8` |  
| `%` (Modulus) | `10 % 3` | `1` (remainder) |  

**Increment/Decrement:**  
- `x++` → Postfix (use then increment)  
- `++x` → Prefix (increment then use)  

**Example:**  
```javascript
let a = 5;  
console.log(a++); // 5 (logs first, then increments)  
console.log(++a); // 7 (increments first, then logs)  
```  

### **Assignment Operators**  
Shortcut for updating variables:  
| Operator | Example | Equivalent |  
|----------|---------|------------|  
| `+=` | `x += 2` | `x = x + 2` |  
| `-=` | `x -= 2` | `x = x - 2` |  
| `*=` | `x *= 2` | `x = x * 2` |  
| `/=` | `x /= 2` | `x = x / 2` |  
| `**=` | `x **= 2` | `x = x ** 2` |  

**Example:**  
```javascript
let num = 10;  
num += 5;  // num = 15  
```  

---

## **Comparison & Logical Operators**  

### **Comparison Operators**  
Return `true` or `false`.  

| Operator | Meaning | Example |  
|----------|---------|---------|  
| `==` | Loose equality (value only) | `5 == "5"` → `true` |  
| `===` | Strict equality (value + type) | `5 === "5"` → `false` |  
| `!=` | Not equal (loose) | `5 != "5"` → `false` |  
| `!==` | Not equal (strict) | `5 !== "5"` → `true` |  
| `>` | Greater than | `5 > 3` → `true` |  
| `<` | Less than | `5 < 3` → `false` |  
| `>=` | Greater than or equal | `5 >= 5` → `true` |  
| `<=` | Less than or equal | `5 <= 3` → `false` |  

### **Logical Operators**  
Combine conditions:  

| Operator | Meaning | Example |  
|----------|---------|---------|  
| `&&` | AND (both must be true) | `(5 > 3) && (2 < 4)` → `true` |  
| `||` | OR (at least one true) | `(5 < 3) || (2 < 4)` → `true` |  
| `!` | NOT (inverts boolean) | `!(5 > 3)` → `false` |  

**Example:**  
```javascript
let age = 20;  
let hasLicense = true;  
if (age >= 18 && hasLicense) {  
  console.log("Can drive!");  
}  
```  

### **Type Conversion**  
- `String(x)` → Converts to string.  
- `Number(x)` → Converts to number (`"5"` → `5`).  
- `Boolean(x)` → Converts to boolean (`0` → `false`).  

**Example:**  
```javascript
let numStr = "123";  
let num = Number(numStr);  // 123 (number)  
```  

### **Key Takeaways**  
1. **Variables** store changeable data (`let`, `const`).  
2. **Primitive Types** include strings, numbers, booleans, etc.  
3. **Operators** perform math, comparisons, and logic.  
4. **Type Conversion** helps change data types when needed.  

**Practice:**  
- Try declaring variables and testing operators.  
- Use `prompt()` to get user input and perform calculations.  

