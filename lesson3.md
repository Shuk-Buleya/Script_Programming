### Arrays Fundamentals  
**What are Arrays?**  
- Lists of values that can hold multiple data types (even mixed)  
- Used to store grouped data (e.g., students, test scores)  
- Created with square brackets `[]` (best practice):  
  ```javascript
  // Recommended
  let colors = ["red", "green", "blue"];
  
  // Avoid (unexpected behavior)
  let numbers = new Array(10); // Creates 10 empty slots
  ```  

**Key Properties**  
1. `length`: Returns number of elements  
   ```javascript
   let fruits = ["🍎", "🍌"];
   console.log(fruits.length); // 2
   ```  
2. Zero-indexed: First element at position `0`  
   ```javascript
   console.log(fruits[0]); // "🍎"
   ```  

**Modifying Arrays**  
- Overwrite elements:  
  ```javascript
  fruits[1] = "🥭"; // ["🍎", "🥭"]
  ```  
- Add elements:  
  ```javascript
  fruits[5] = "🍇"; // Creates empty slots
  console.log(fruits); // ["🍎", "🥭", empty × 3, "🍇"]
  ```  

**`const` with Arrays**  
- Can modify elements, but can't reassign the array:  
  ```javascript
  const arr = [1, 2];
  arr[0] = 99; // ✅ Works
  arr = [3, 4]; // ❌ Error
  ```  

---

### Array Methods & Multidimensional Arrays  
**Essential Methods**  
| Method       | Action                           | Example                          |
|--------------|----------------------------------|----------------------------------|
| `push()`     | Add item to end                  | `fruits.push("🍊");`            |
| `pop()`      | Remove last item                 | `fruits.pop();`                 |
| `unshift()`  | Add item to start                | `fruits.unshift("🍍");`         |
| `shift()`    | Remove first item                | `fruits.shift();`               |
| `splice()`   | Insert/remove items              | `fruits.splice(1, 0, "🥝");`    |
| `concat()`   | Merge arrays                     | `let food = fruits.concat(veggies);` |
| `sort()`     | Alphabetical/numeric sort        | `fruits.sort();`                |
| `reverse()`  | Reverse order                    | `fruits.reverse();`             |

**Finding Elements**  
```javascript
let prices = [5, 7, 3];
console.log(prices.indexOf(7));    // 1
console.log(prices.find(x => x>5)); // 7
```

**Multidimensional Arrays**  
- Arrays containing other arrays:  
  ```javascript
  let matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
  ];
  console.log(matrix[1][2]); // 6
  ```  

---

### Objects & Practical Patterns  
**Objects Basics**  
- Collections of key-value pairs:  
  ```javascript
  let car = {
    make: "Toyota",
    model: "Camry",
    year: 2020,
    isElectric: false
  };
  ```  

**Accessing Properties**  
- Dot notation: `car.make` // "Toyota"  
- Bracket notation (for dynamic keys):  
  ```javascript
  let key = "model";
  console.log(car[key]); // "Camry"
  ```  

**Combining Objects & Arrays**  
1. **Arrays in Objects**:  
   ```javascript
   let classroom = {
     teacher: "Ms. Smith",
     students: ["John", "Emma", "Liam"]
   };
   ```  
2. **Objects in Arrays**:  
   ```javascript
   let inventory = [
     { item: "Keyboard", price: 25 },
     { item: "Mouse", price: 15 }
   ];
   ```  
3. **Nested Objects**:  
   ```javascript
   let company = {
     name: "TechCorp",
     offices: [
       { city: "New York", employees: 50 },
       { city: "London", employees: 30 }
     ]
   };
   console.log(company.offices[0].city); // "New York"
   ```  

**Practical Exercise**  
```javascript
// 1. Create friends list
let people = { friends: [] };

// 2. Add friends
people.friends.push(
  { firstName: "Alex", id: 1 },
  { firstName: "Sam", id: 2 }
);

// 3. Access data
console.log(people.friends[0].firstName); // "Alex"
```

**Key Takeaways**  
- Use `[]` for arrays, `{}` for objects  
- Prefer array methods over manual index manipulation  
- Combine arrays/objects to model complex data  
