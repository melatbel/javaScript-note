# JavaScript note

// Declaring different variables of different data types

```jsx

let firstName = 'Asabeneh'
let age = 100 
let isMarried = true
```

// Declaring variables with number values

```jsx

const gravity = 9.81 
const boilingPoint = 100 
const PI = 3.14 
```

// Variables can also be declaring in one line separated by comma

```jsx

let name = 'Asabeneh',
job = 'teacher',
live = 'Finland'
```

In JavaScript, there are two main categories of data types: primitive and non-primitive.

# 1. Primitive Data Types:

Primitive data types are the most basic data types in JavaScript. They are immutable, meaning that their values cannot be changed once they are created. There are six primitive data types in JavaScript**:**

- **Number**: represents numeric values, including integers and floating-point numbers.
- **String**: represents textual data, enclosed in single or double quotes.
- **Boolean**: represents a logical value, either true or false.
- **Null**: represents a deliberate non-value or absence of any object value.
- **Undefined**: represents an uninitialized value or absence of a defined value.
- **Symbol**: represents a unique identifier that is not equal to any other value.
- Here is an example of how to declare and use primitive data types in JavaScript:
    
    ```jsx
    let num = 42; // number
    let bool = true; // boolean
    let n = null; // null
    let u; // undefined
    let sym = Symbol("foo"); // symbol
    console.log(typeof num); // "number"
    console.log(typeof str); // "string"
    console.log(typeof bool); // "boolean"
    console.log(typeof n); // "object" (known bug in JavaScript)
    console.log(typeof u); // "undefined"
    console.log(typeof sym); // "symbol"
    
    let numOne = 3
    let numTwo = 3
    
    console.log(numOne == numTwo)      // true
    
    //Math Object
    const PI = Math.PI
    
    console.log(PI)                            // 3.141592653589793
    
    // Rounding to the closest number
    // if above .5 up if less 0.5 down rounding
    
    console.log(Math.round(9.81))              // 10
    console.log(Math.min(-5, 3, 20, 4, 5, 10)) // -5, returns the minimum value
    
    console.log(Math.max(-5, 3, 20, 4, 5, 10)) // 20, returns the maximum value
    const randNum = Math.random() // creates random number between 0 to 0.999999
    console.log(randNum)
    
    // Let us  create random number between 0 to 10
    
    const num = Math.floor(Math.random () * 11) // creates random number between 0 and 10
    console.log(num)
    let randomNum = Math.random() // generates 0 to 0.999... //Random Number Generator
    //Absolute value
    console.log(Math.abs(-10))      // 10
    
    //Square root
    console.log(Math.sqrt(100))     // 10
    
    console.log(Math.sqrt(2))       // 1.4142135623730951
    
    // Power
    console.log(Math.pow(3, 2))     // 9
    
    console.log(Math.E)             // 2.718
    
    // Logarithm
    // Returns the natural logarithm with base E of x, Math.log(x)
    console.log(Math.log(2))        // 0.6931471805599453
    console.log(Math.log(10))       // 2.302585092994046
    
    // Returns the natural logarithm of 2 and 10 respectively
    console.log(Math.LN2)           // 0.6931471805599453
    console.log(Math.LN10)          // 2.302585092994046
    ```
    
- **Strings**
    
    Strings are texts, which are under ***single*** , ***double***, ***back-tick*** quote.
    
    ```jsx
    let str = "Hello, world!"; 
    let quote = "The saying,'Seeing is Believing' is not correct in 2020."
    let space = ' '           // an empty space string
    let firstName = 'Asabeneh'
    ```
    
    - **String Concatenation:** Connecting two or more strings together.
    
    ```jsx
    let firstName = 'Asabeneh'
    let space = ' ' 
    let lastName = 'Yetayeh'
    let fullName = firstName + space + lastName; // concatenation, merging two string together.
    console.log(fullName); //Asabeneh Yetayeh
    ```
    
    ### Escape Sequences in Strings
    
    In JavaScript and other programming languages \ followed by some characters is an escape sequence. Common escape characters:
    
    - \n: new line
    - \t: Tab, means 8 spaces
    - \\: Back slash
    - \': Single quote (')
    - \": Double quote ("
    
    ```jsx
    console.log('I hope everyone is enjoying the 30 Days Of JavaScript challenge.\nDo you ?') // line break //output I hope everyone is enjoying the 30 Days Of JavaScript challenge.
    Do you ?
    
    console.log('Day 1\t3\t5')//Day 1 3 5
    console.log('This is a backslash  symbol (\\)') // To write a backslash
    console.log('In every programming language it starts with \"Hello, World!\"')
    console.log("In every programming language it starts with \'Hello, World!\'")
    console.log('The saying \'Seeing is Believing\' isn\'t correct in 2020')
    ```
    
    ### Template Literals (Template Strings)
    
    We can inject data as expressions inside a template string. To inject data, we enclose the expression with a curly bracket({}) preceded by a $ sign. 
    
    ```jsx
    //Syntax
    `String literal text`
    `String literal text ${expression}`
    // example 1
    console.log(`The sum of 2 and 3 is 5`)              // statically writing the data
    let a = 2
    let b = 3
    console.log(`The sum of ${a} and ${b} is ${a + b}`) // injecting the data dynamically
    // example 2
    let firstName = 'Asabeneh'
    let lastName = 'Yetayeh'
    let country = 'Finland'
    let city = 'Helsinki'
    let language = 'JavaScript'
    let job = 'teacher'
    let age = 250
    let fullName = firstName + ' ' + lastName
    
    let personInfoTwo = `I am ${fullName}. I am ${age}. I live in ${country}.` //ES6 - String interpolation method
    let personInfoThree = `I am ${fullName}. I live in ${city}, ${country}. I am a ${job}. I teach ${language}.`
    console.log(personInfoTwo)
    console.log(personInfoThree) // output I am Asabeneh Yetayeh. I am 250. I live in Finland.
    I am Asabeneh Yetayeh. I live in Helsinki, Finland. I am a teacher. I teach JavaScript.
    // example 3
    let a = 2
    let b = 3
    console.log(`${a} is greater than ${b}: ${a > b}`) // output  2 is greater than 3: false
    ```
    
    - **String Methods**
        
        In JavaScript, there are several methods that can be used to manipulate strings. Here are some of the most commonly used methods:
        
        1. charAt(): This method returns the character at a specified index in a string. It takes one parameter, which is the index of the character to be returned. If the index is out of range, an empty string is returned.
        
         Example:
        
        ```jsx
        let str = "hello";
        console.log(str.charAt(1)); // Output: "e"
        ```
        
        1. indexOf(): This method returns the index of the first occurrence of a specified substring in a string. It takes one parameter, which is the substring to search for. If the substring is not found, -1 is returned.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.indexOf("world")); // Output: 6
        ```
        
        1. replace(): This method replaces a specified substring with another string and returns the modified string. It takes two parameters, the first one is the substring to be replaced and the second one is the string to replace it with.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.replace("world", "universe")); // Output: "hello universe"
        ```
        
        1. slice(): This method extracts a portion of a string and returns it as a new string. It takes two parameters, which are the starting and ending indexes of the portion to be extracted. If the ending index is not specified, the method will extract the rest of the string.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.slice(0, 5)); // Output: "hello"
        ```
        
        1. split(): This method splits a string into an array of substrings based on a specified separator. It takes one parameter, which is the separator to use. If no separator is specified, the method will split the string at every character.
        
        Example:
        
        ```jsx
        let str = "hello,world";
        console.log(str.split(",")); // Output: ["hello", "world"]
        ```
        
        1. toLowerCase(): This method converts a string to lowercase and returns the modified string.
        
        Example:
        
        ```jsx
        let str = "Hello World";
        console.log(str.toLowerCase()); // Output: "hello world"
        ```
        
        1. toUpperCase(): This method converts a string to uppercase and returns the modified string.
        
        Example:
        
        ```jsx
        let str = "Hello World";
        console.log(str.toUpperCase()); // Output: "HELLO WORLD"
        ```
        
        1. startsWith(): This method checks whether a string starts with a specified substring and returns a boolean value. It takes one parameter, which is the substring to check for.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.startsWith("hello")); // Output: true
        ```
        
        1. endsWith(): This method checks whether a string ends with a specified substring and returns a boolean value. It takes one parameter, which is the substring to check for.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.endsWith("world")); // Output: true
        ```
        
        1. repeat(): This method returns a new string consisting of a specified number of copies of the original string. It takes one parameter, which is the number of times to repeat the string.
        
        Example:
        
        ```jsx
        let str = "hello";
        console.log(str.repeat(3)); // Output: "hellohellohello"
        ```
        
        1. substr(): This method extracts a portion of a string and returns it as a new string. It takes two parameters, the first one is the starting index of the portion to be extracted and the second one is the length of the portion to be extracted.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.substr(0, 5)); // Output: "hello"
        ```
        
        1. toLocaleLowerCase(): This method converts a string to lowercase based on the current locale and returns the modified string.
        
        Example:
        
        ```jsx
        let str = "HÉLLÖ WÖRLD";
        console.log(str.toLocaleLowerCase()); // Output: "héllö wörld" (depending on the locale)
        ```
        
        1. toLocaleUpperCase(): This method converts a string to uppercase based on the current locale and returns the modified string.
        
        Example:
        
        ```jsx
        let str = "héllö wörld";
        console.log(str.toLocaleUpperCase()); // Output: "HÉLLÖ WÖRLD" (depending on the locale)
        ```
        
        1. toString(): This method returns a string representing the specified object. It is usually called on non-string objects to convert them to strings.
        
        Example:
        
        ```jsx
        let num = 123;
        console.log(num.toString()); // Output: "123"
        ```
        
        1. valueOf(): This method returns the primitive value of a string object. It is usually called on string objects to convert them to primitive values.
        
        Example:
        
        ```jsx
        let str = new String("hello");
        console.log(str.valueOf()); // Output: "hello"
        ```
        
        1. trim(): This method removes whitespace from both ends of a string and returns the modified string.
        
        Example:
        
        ```jsx
        let str = "   hello world   ";
        console.log(str.trim()); // Output: "hello world"
        ```
        
        1. trimStart() or trimLeft(): These methods remove whitespace from the beginning of a string and return the modified string.
        
        Example:
        
        ```jsx
        let str = "   hello world";
        console.log(str.trimStart()); // Output: "hello world"
        ```
        
        1. trimEnd() or trimRight(): These methods remove whitespace from the end of a string and return the modified string.
        
        Example:
        
        ```jsx
        let str = "hello world   ";
        console.log(str.trimEnd()); // Output: "hello world"
        ```
        
        1. padStart(): This method pads a string with another string until it reaches a specified length. It takes two parameters, the first one is the target length and the second one is the padding string.
        
        Example:
        
        ```jsx
        let str = "hello";
        console.log(str.padStart(10, "*")); // Output: "*****hello"
        ```
        
        1. padEnd(): This method pads a string with another string until it reaches a specified length. It takes two parameters, the first one is the target length and the second one is the padding string.
        
        Example:
        
        ```jsx
        let str = "hello";
        console.log(str.padEnd(10, "*")); // Output: "hello*****"
        ```
        
        1. charCodeAt(): This method returns the Unicode value of the character at a specified index in a string. It takes one parameter, which is the index of the character.
        
        Example:
        
        ```jsx
        let str = "hello";
        console.log(str.charCodeAt(1)); // Output: 101
        ```
        
        1. concat(): This method concatenates two or more strings and returns the result.
        
        Example:
        
        ```jsx
        let str1 = "hello";
        let str2 = "world";
        console.log(str1.concat(" ", str2)); // Output: "hello world"
        ```
        
        1. includes(): This method checks if a string contains another string and returns a boolean value. It takes one parameter, which is the substring to search for.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.includes("world")); // Output: true
        ```
        
        1. startsWith(): This method checks if a string starts with another string and returns a boolean value. It takes one parameter, which is the substring to search for.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.startsWith("hello")); // Output: true
        ```
        
        1. endsWith(): This method checks if a string ends with another string and returns a boolean value. It takes one parameter, which is the substring to search for.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.endsWith("world")); // Output: true
        ```
        
        1. repeat(): This method repeats a string a specified number of times and returns the result. It takes one parameter, which is the number of times to repeat the string.
        
        Example:
        
        ```jsx
        let str = "hello";
        console.log(str.repeat(3)); // Output: "hellohellohello"
        ```
        
        1. replaceAll(): This method replaces all occurrences of a specified substring with another substring and returns the modified string. It takes two parameters, the first one is the substring to be replaced and the second one is the replacement substring.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.replaceAll("o", "*")); // Output: "hell* w*rld"
        ```
        
        1. match(): This method searches a string for a specified pattern and returns an array of all matches found. It takes one parameter, which is the pattern to search for.
        
        Example:
        
        ```jsx
        let str = "The quick brown fox jumps over the lazy dog";
        console.log(str.match(/the/gi)); // Output: ["The", "the"]
        ```
        
        1. search(): This method searches a string for a specified pattern and returns the index of the first match found. It takes one parameter, which is the pattern to search for.
        
        Example:
        
        ```jsx
        let str = "The quick brown fox jumps over the lazy dog";
        console.log(str.search(/brown/gi)); // Output: 10
        ```
        
        1. slice(): This method extracts a section of a string and returns the extracted part as a new string. It takes two parameters, the first one is the starting index and the second one is the ending index (optional).
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.slice(0, 5)); // Output: "hello"
        ```
        
        1. substring(): This method extracts a section of a string and returns the extracted part as a new string. It takes two parameters, the first one is the starting index and the second one is the ending index (optional).
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.substring(0, 5)); // Output: "hello"
        ```
        
        1. substr(): This method extracts a section of a string and returns the extracted part as a new string. It takes two parameters, the first one is the starting index and the second one is the length of the substring.
        
        Example:
        
        ```jsx
        let str = "hello world";
        console.log(str.substr(0, 5)); // Output: "hello"
        ```
        
    
- **Booleans, Operators, Date**
    
    A boolean data type represents one of the two values:*true* or *false*.
    
    ### Truthy values
    
    - All numbers(positive and negative) are truthy except zero
    - All strings are truthy except an empty string ('')
    - The boolean true
    
    ### Falsy values
    
    - 0
    - 0n
    - null
    - undefined
    - NaN
    - the boolean false
    - '', "", ``, empty string
    
    ## Undefined
    
    If we declare a variable and if we do not assign a value, the value will be undefined. In addition to this, if a function is not returning the value, it will be undefined.
    
    ```jsx
    let firstName
    console.log(firstName) //not defined, because it is not assigned to a value yet
    ```
    
    ## Null
    
    ```jsx
    let empty = null
    console.log(empty) // -> null , means no value
    ```
    
    - Operators
        
        ### Assignment operators
        
        An equal sign in JavaScript is an assignment operator. It uses to assign a variable.
        
        ```
        let firstName = 'Asabeneh'
        let country = 'Finland'
        ```
        
        ![Untitled](JavaScript%20note%20b7861e8ae9434cf98fa24e4c2f48f29b/Untitled.png)
        
        ```jsx
        let numOne = 4
        let numTwo = 3
        let sum = numOne + numTwo
        let diff = numOne - numTwo
        let mult = numOne * numTwo
        let div = numOne / numTwo
        let remainder = numOne % numTwo
        let powerOf = numOne ** numTwo
        
        console.log(sum, diff, mult, div, remainder, powerOf) // 7,1,12,1.33
        ```
        
        ### Logical Operators
        
        ```jsx
        // && ampersand operator gets true only if the two operands are true.
        //example
        
        const check = 4 > 3 && 10 > 5         // true && true -> true
        const check = 4 > 3 && 10 < 5         // true && false -> false
        const check = 4 < 3 && 10 < 5         // false && false -> false
        
        // || pipe or operator: operator gets true either of the operand is true.
        
        // example
        
        const check = 4 > 3 || 10 > 5         // true  || true -> true
        const check = 4 > 3 || 10 < 5         // true  || false -> true
        const check = 4 < 3 || 10 < 5         // false || false -> false
        
        //! Negation:operator negates true to false and false to true.
        
        // examples
        
        let check = 4 > 3                     // true
        let check = !(4 > 3)                  //  false
        let isLightOn = true
        let isLightOff = !isLightOn           // false
        let isMarried = !false                // true
        ```
        
        ### Increment Operator
        
        1. Pre-increment
        
        ```jsx
        let count = 0
        console.log(++count)        // 1
        console.log(count)          // 1
        ```
        
        1. Post-increment
        
        ```jsx
        let count = 0
        console.log(count++)        // 0
        console.log(count)          // 1
        ```
        
        **Decrement Operator**
        
        1. Pre-decrement
        
        ```jsx
        let count = 0
        console.log(--count) // -1
        console.log(count)  // -1
        ```
        
        1. Post-decrement
        
        ```jsx
        let count = 0
        console.log(count--) // 0
        console.log(count)   // -1
        ```
        
        ### Ternary Operators
        
        Ternary operator allows to write a condition. 
        
        ```jsx
        let isRaining = true
        isRaining
          ? console.log('You need a rain coat.')
          : console.log('No need for a rain coat.')
        isRaining = false
        
        isRaining
          ? console.log('You need a rain coat.')
          : console.log('No need for a rain coat.')
        // output You need a rain coat.
        // No need for a rain coat.
        
        let number = 5
        number > 0
          ? console.log(`${number} is a positive number`)
          : console.log(`${number} is a negative number`)
        number = -5
        
        number > 0
          ? console.log(`${number} is a positive number`)
          : console.log(`${number} is a negative number`)
        //5 is a positive number
        //-5 is a negative number
        ```
        
    - Window Methods
        
        ### Window alert() method
        
        Alert() method displays an alert box with a specified message and an OK button. It is a builtin method and it takes on argument.
        
        ```jsx
        alert(message)
        alert('Welcome to 30DaysOfJavaScript')
        ```
        
        **Window prompt() method**
        
        The window prompt methods display a prompt box with an input on your browser to take input values and the input data can be stored in a variable. The prompt() method takes two arguments. The second argument is optional.
        
        ```jsx
        prompt('required text', 'optional text')
        let number = prompt('Enter number', 'number goes here')
        console.log(number)
        ```
        
        ### Window confirm() method
        
        The confirm() method displays a dialog box with a specified message, along with an OK and a Cancel button. A confirm box is often used to ask permission from a user to execute something. Window confirm() takes a string as an argument. Clicking the OK yields true value, whereas clicking the Cancel button yields false value.
        
        ```jsx
        const agree = confirm('Are you sure you like to delete? ')
        console.log(agree) // result will be true or false based on what you click on the dialog box
        ```
        
    - **Date Object**
        
        ```jsx
        // Getting full year
        const now = new Date()
        console.log(now.getFullYear()) // 2020 
        // Getting month
        const now = new Date()
        console.log(now.getMonth()) // 0, because the month is January,  month(0-11)
        
        // Getting date
        
        const now = new Date()
        console.log(now.getDate()) // 4, because the day of the month is 4th,  day(1-31)
        
        // Getting day
        
        const now = new Date()
        console.log(now.getDay()) // 6, because the day is Saturday which is the 7th day
        //  Sunday is 0, Monday is 1 and Saturday is 6
        // Getting the weekday as a number (0-6)
        
        // Getting hours
        
        const now = new Date()
        console.log(now.getHours()) // 0, because the time is 00:56:41
        
        // Getting minutes
        
        const now = new Date()
        console.log(now.getMinutes()) // 56, because the time is 00:56:41
        
        // Getting seconds
        
        const now = new Date()
        console.log(now.getSeconds()) // 41, because the time is 00:56:41
        
        // Getting time
        //Using getTime()
        const now = new Date() //
        console.log(now.getTime()) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41
        //Using Date.now()
        const allSeconds = Date.now() //
        console.log(allSeconds) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41
        
        const timeInSeconds = new Date().getTime()
        console.log(allSeconds == timeInSeconds) // true
        ```
        
- **Conditionals**
    
    Conditional statements are used for make decisions based on different conditions. By default , statements in JavaScript script executed sequentially from top to bottom.
    
    1. **If**
    
    ```jsx
    let num = 3
    if (num > 0) {
      console.log(`${num} is a positive number`)
    }
    //  3 is a positive number
    ```
    
    1. **If Else**
    
    ```jsx
    let isRaining = true
    if (isRaining) {
      console.log('You need a rain coat.')
    } else {
      console.log('No need for a rain coat.')
    }
    // You need a rain coat.
    
    isRaining = false
    if (isRaining) {
      console.log('You need a rain coat.')
    } else {
      console.log('No need for a rain coat.')
    }
    // No need for a rain coat.
    
    num = -3
    if (num > 0) {
      console.log(`${num} is a positive number`)
    } else {
      console.log(`${num} is a negative number`)
    }
    //  -3 is a negative number
    ```
    
    1. **If Else if Else**
    
    ```jsx
    // if else if else
    let weather = 'sunny'
    if (weather === 'rainy') {
      console.log('You need a rain coat.')
    } else if (weather === 'cloudy') {
      console.log('It might be cold, you need a jacket.')
    } else if (weather === 'sunny') {
      console.log('Go out freely.')
    } else {
      console.log('No need for rain coat.')
    }
    ```
    
    1. **Switch**
    
    ```jsx
    let num = prompt('Enter number');
    switch (true) {
      case num > 0:
        console.log('Number is positive');
        break;
      case num == 0:
        console.log('Numbers is zero');
        break;
      case num < 0:
        console.log('Number is negative');
        break;
      default:
        console.log('Entered value was not a number');
    }
    
    let weather = 'cloudy'
    switch (weather) {
      case 'rainy':
        console.log('You need a rain coat.')
        break
      case 'cloudy':
        console.log('It might be cold, you need a jacket.')
        break
      case 'sunny':
        console.log('Go out freely.')
        break
      default:
        console.log(' No need for rain coat.')
    }
    
    // Switch More Examples
    let dayUserInput = prompt('What day is today ?')
    let day = dayUserInput.toLowerCase()
    
    switch (day) {
      case 'monday':
        console.log('Today is Monday')
        break
      case 'tuesday':
        console.log('Today is Tuesday')
        break
      case 'wednesday':
        console.log('Today is Wednesday')
        break
      case 'thursday':
        console.log('Today is Thursday')
        break
      case 'friday':
        console.log('Today is Friday')
        break
      case 'saturday':
        console.log('Today is Saturday')
        break
      case 'sunday':
        console.log('Today is Sunday')
        break
      default:
        console.log('It is not a week day.')
    }
    ```
    

# 2. **Non-Primitive Data Types**

Non-primitive data types are more complex data types that can hold multiple values and are mutable. They are also known as reference types because they are stored as references to memory locations rather than as actual values. There are three non-primitive data types in JavaScript:

- Object: represents a collection of key-value pairs, where the keys are strings and the values can be any data type.
- Array: represents a collection of ordered values, where each value can be any data type.
- Function: represents a reusable block of code that can be called with arguments.

- **Arrays**
    
    Represents a collection of ordered values, where each value can be any data type.
    
    It is very common to use *const* instead of *let* to declare an array variable. If you are using const it means you do not use that variable name again.
    
    ```jsx
    // Using Array constructor
    const arr = Array()
    // or
    //let arr = new Array()
    console.log(arr) // []
    
    Using square brackets([])
    // syntax
    // This the most recommended way to create an empty list
    const arr = []
    console.log(arr)
    
    // Array with initial values
    const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // array of numbers
    const fruits = ['banana', 'orange', 'mango', 'lemon'] // array of strings, fruits
    
    // Print the array and its length
    
    console.log('Numbers:', numbers)
    console.log('Number of numbers:', numbers.length)
    // output  Numbers: [0, 3.14, 9.81, 37, 98.6, 100]
    // Number of numbers: 6
    
    const arr = [
        'Asabeneh',
        250,
        true,
        { country: 'Finland', city: 'Helsinki' },
        { skills: ['HTML', 'CSS', 'JS', 'React', 'Python'] }
    ] // arr containing different data types
    console.log(arr)
    ```
    
    ### Creating an array using split
    
    ```jsx
    let js = 'JavaScript'
    const charsInJavaScript = js.split('')
    
    console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]
    
    let txt =
      'I love teaching and empowering people. I teach HTML, CSS, JS, React, Python.'
    const words = txt.split(' ')
    
    console.log(words)
    // the text has special characters think how you can just get only the words
    // ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]
    ```
    
    ### Accessing array items using index
    
    ```jsx
    const fruits = ['banana', 'orange', 'mango', 'lemon']
    let firstFruit = fruits[0] 
    console.log(firstFruit) // banana
    
    ```
    
    ```jsx
    const webTechs = [
      'HTML',
      'CSS',
      'JavaScript',
      'React',
      'Redux',
      'Node',
      'MongoDB'
    ] // List of web technologies
    
    console.log(webTechs)        // all the array items
    console.log(webTechs.length) // => to know the size of the array, which is 7
    console.log(webTechs[0])     //  -> HTML
    console.log(webTechs[6])     //  -> MongoDB
    
    let lastIndex = webTechs.length - 1
    console.log(webTechs[lastIndex]) // -> MongoDB
    ```
    
    ```jsx
    const countries = [
      'Albania',
      'Bolivia',
      'Canada',
      'Denmark',
      'Ethiopia',
      'Finland',
      'Germany',
      'Hungary',
      'Ireland',
      'Japan',
      'Kenya'
    ] // List of countries
    
    console.log(countries)      // -> all countries in array
    console.log(countries[0])   //  -> Albania
    console.log(countries[10])  //  -> Kenya
    
    let lastIndex = countries.length - 1;
    console.log(countries[lastIndex]) //  -> Kenya
    ```
    
    ### Modifying array element
    
    An array is mutable(modifiable). Once an array is created, we can modify the contents of the array elements.
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    numbers[0] = 10      // changing 1 at index 0 to 10
    numbers[1] = 20      // changing  2 at index 1 to 20
    
    console.log(numbers) // [10, 20, 3, 4, 5]
    
    const countries = [
      'Albania',
      'Bolivia',
      'Canada',
      'Kenya'
    ]
    
    countries[0] = 'Afghanistan'  // Replacing Albania by Afghanistan
    let lastIndex = countries.length - 1
    countries[lastIndex] = 'Korea' // Replacing Kenya by Korea
    
    console.log(countries)
    ```
    
    - **Methods to manipulate array**
        
        ### Array Constructor
        
        Array: To create an array.
        
        ```jsx
        const arr = Array() // creates an an empty array
        console.log(arr)
        
        const eightEmptyValues = Array(8) // it creates eight empty values
        console.log(eightEmptyValues) // [empty x 8]
        ```
        
        ### Creating static values with fill
        
        fill: Fill all the array elements with a static value
        
        ```jsx
        const arr = Array() // creates an an empty array
        console.log(arr)
        
        const eightXvalues = Array(8).fill('X') // it creates eight element values filled with 'X'
        console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']
        
        const eight0values = Array(8).fill(0) // it creates eight element values filled with '0'
        console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]
        
        const four4values = Array(4).fill(4) // it creates 4 element values filled with '4'
        console.log(four4values) // [4, 4, 4, 4]
        ```
        
        ### Concatenating array using concat
        
        concat: To concatenate two arrays.
        
        ```jsx
        const firstList = [1, 2, 3]
        const secondList = [4, 5, 6]
        const thirdList = firstList.concat(secondList)
        
        console.log(thirdList) // [1, 2, 3, 4, 5, 6]
        ```
        
        ```jsx
        const fruits = ['banana', 'orange', 'mango', 'lemon']                 // array of fruits
        const vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // array of vegetables
        const fruitsAndVegetables = fruits.concat(vegetables)                 // concatenate the two arrays
        
        console.log(fruitsAndVegetables)
        // ooutput ["banana", "orange", "mango", "lemon", "Tomato", "Potato", "Cabbage", "Onion", "Carrot"]
        ```
        
        ### Getting array length
        
        Length:To know the size of the array
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        console.log(numbers.length) // -> 5 is the size of the array
        ```
        
        ### Getting index an element in arr array
        
        indexOf:To check if an item exist in an array. If it exists it returns the index else it returns -1.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        
        console.log(numbers.indexOf(5)) // -> 4
        console.log(numbers.indexOf(0)) // -> -1
        console.log(numbers.indexOf(1)) // -> 0
        console.log(numbers.indexOf(6)) // -> -1
        ```
        
        Check an element if it exist in an array.
        
        - Check items in a list
        
        ```jsx
        // let us check if a banana exist in the array
        
        const fruits = ['banana', 'orange', 'mango', 'lemon']
        let index = fruits.indexOf('banana')  // 0
        
        if(index === -1){
           console.log('This fruit does not exist in the array')
        } else {
            console.log('This fruit does exist in the array')
        }
        // This fruit does exist in the array
        
        // we can use also ternary here
        index === -1 ? console.log('This fruit does not exist in the array'): console.log('This fruit does exist in the array')
        
        // let us check if an avocado exist in the array
        let indexOfAvocado = fruits.indexOf('avocado')  // -1, if the element not found index is -1
        if(indexOfAvocado === -1){
           console.log('This fruit does not exist in the array')
        } else {
            console.log('This fruit does exist in the array')
        }
        // This fruit does not exist in the array
        ```
        
        ### Getting last index of an element in array
        
        lastIndexOf: It gives the position of the last item in the array. If it exist, it returns the index else it returns -1.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5, 3, 1, 2]
        
        console.log(numbers.lastIndexOf(2)) // 7
        console.log(numbers.lastIndexOf(0)) // -1
        console.log(numbers.lastIndexOf(1)) //  6
        console.log(numbers.lastIndexOf(4)) //  3
        console.log(numbers.lastIndexOf(6)) // -1
        ```
        
        includes:To check if an item exist in an array. If it exist it returns the true else it returns false.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        
        console.log(numbers.includes(5)) // true
        console.log(numbers.includes(0)) // false
        console.log(numbers.includes(1)) // true
        console.log(numbers.includes(6)) // false
        
        const webTechs = [
          'HTML',
          'CSS',
          'JavaScript',
          'React',
          'Redux',
          'Node',
          'MongoDB'
        ] // List of web technologies
        
        console.log(webTechs.includes('Node'))  // true
        console.log(webTechs.includes('C'))     // false
        ```
        
        ### Checking array
        
        Array.isArray:To check if the data type is an array
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        console.log(Array.isArray(numbers)) // true
        
        const number = 100
        console.log(Array.isArray(number)) // false
        ```
        
        ### Converting array to string
        
        toString:Converts array to string
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        console.log(numbers.toString()) // 1,2,3,4,5
        
        const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
        console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook
        ```
        
        ### Joining array elements
        
        join: It is used to join the elements of the array. By default, it joins with a comma, but we can pass different string parameter which can be joined between the items.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        console.log(numbers.join()) // 1,2,3,4,5
        
        const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
        
        console.log(names.join()) // Asabeneh,Mathias,Elias,Brook
        console.log(names.join('')) //AsabenehMathiasEliasBrook
        console.log(names.join(' ')) //Asabeneh Mathias Elias Brook
        console.log(names.join(', ')) //Asabeneh, Mathias, Elias, Brook
        console.log(names.join(' # ')) //Asabeneh # Mathias # Elias # Brook
        
        const webTechs = [
          'HTML',
          'CSS',
          'JavaScript',
          'React',
          'Redux',
          'Node',
          'MongoDB'
        ] // List of web technologies
        
        console.log(webTechs.join())       // "HTML,CSS,JavaScript,React,Redux,Node,MongoDB"
        console.log(webTechs.join(' # '))  // "HTML # CSS # JavaScript # React # Redux # Node # MongoDB"
        ```
        
        ### Slice array elements
        
        Slice: To cut out a multiple items in range. It takes two parameters:starting and ending position. It doesn't include the ending position.
        
        ```jsx
          const numbers = [1,2,3,4,5]
        
          console.log(numbers.slice()) // -> it copies all  item
          console.log(numbers.slice(0)) // -> it copies all  item
          console.log(numbers.slice(0, numbers.length)) // it copies all  item
          console.log(numbers.slice(1,4)) // -> [2,3,4] // it doesn't include the ending position
        ```
        
        ### Splice method in array
        
        Splice: It takes three parameters:Starting position, number of times to be removed and number of items to be added.
        
        ```jsx
          const numbers = [1, 2, 3, 4, 5]
          numbers.splice()
          console.log(numbers)                // -> remove all items
        ```
        
        ```jsx
          const numbers = [1, 2, 3, 4, 5]
        	numbers.splice(0,1)
          console.log(numbers)            // remove the first item
        ```
        
        ```jsx
          const numbers = [1, 2, 3, 4, 5, 6]
        	numbers.splice(3, 3, 7, 8, 9)
          console.log(numbers.splice(3, 3, 7, 8, 9))  // -> [1, 2, 3, 7, 8, 9] //it removes three item and replace three items
        ```
        
        ### Adding item to an array using push
        
        Push: adding item in the end. To add item to the end of an existing array we use the push method.
        
        ```jsx
        // syntax
        const arr  = ['item1', 'item2','item3']
        arr.push('new item')
        console.log(arr)
        // ['item1', 'item2','item3','new item']
        ```
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        numbers.push(6)
        console.log(numbers) // -> [1,2,3,4,5,6]
        
        numbers.pop() // -> remove one item from the end
        console.log(numbers) // -> [1,2,3,4,5]
        ```
        
        ```jsx
        let fruits = ['banana', 'orange', 'mango', 'lemon']
        fruits.push('apple')
        console.log(fruits)    // ['banana', 'orange', 'mango', 'lemon', 'apple']
        
        fruits.push('lime')
        console.log(fruits)   // ['banana', 'orange', 'mango', 'lemon', 'apple', 'lime']
        ```
        
        ### Removing the end element using pop
        
        pop: Removing item in the end.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        numbers.pop() // -> remove one item from the end
        console.log(numbers) // -> [1,2,3,4]
        ```
        
        ### Removing an element from the beginning
        
        shift: Removing one array element in the beginning of the array.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        numbers.shift() // -> remove one item from the beginning
        console.log(numbers) // -> [2,3,4,5]
        ```
        
        ### Add an element from the beginning
        
        unshift: Adding array element in the beginning of the array.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        numbers.unshift(0) // -> add one item from the beginning
        console.log(numbers) // -> [0,1,2,3,4,5]
        ```
        
        ### Reversing array order
        
        reverse: reverse the order of an array.
        
        ```jsx
        const numbers = [1, 2, 3, 4, 5]
        numbers.reverse() // -> reverse array order
        console.log(numbers) // [5, 4, 3, 2, 1]
        
        numbers.reverse()
        console.log(numbers) // [1, 2, 3, 4, 5]
        ```
        
        ### Sorting elements in array
        
        sort: arrange array elements in ascending order. Sort takes a call back function, we will see how we use sort with a call back function in the coming sections.
        
        ```jsx
        const webTechs = [
          'HTML',
          'CSS',
          'JavaScript',
          'React',
          'Redux',
          'Node',
          'MongoDB'
        ]
        
        webTechs.sort()
        console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]
        
        webTechs.reverse() // after sorting we can reverse it
        console.log(webTechs) // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HTML", "CSS"]
        ```
        
        ### Array of arrays
        
        Array can store different data types including an array itself. Let us create an array of arrays
        
        ```jsx
        const firstNums = [1, 2, 3]
        const secondNums = [1, 4, 9]
        
        const arrayOfArray =  [[1, 2, 3], [1, 2, 3]]
        console.log(arrayOfArray[0]) // [1, 2, 3]
        
         const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
         const backEnd = ['Node','Express', 'MongoDB']
         const fullStack = [frontEnd, backEnd]
         console.log(fullStack)   // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]
         console.log(fullStack.length)  // 2
         console.log(fullStack[0])  // ["HTML", "CSS", "JS", "React", "Redux"]
         console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]
        ```
        
    
- **Scope**
    
    Variables scopes can be:
    
    - Global
    - Local
    
    **Window Global Object**
    
    Without using console.log() open your browser and check, you will see the value of a and b if you write a or b on the browser. That means a and b are already available in the window.
    
    ```jsx
    //scope.js
    a = 'JavaScript' // declaring a variable without let or const make it available in window object and this found anywhere
    b = 10 // this is a global scope variable and found in the window object
    function letsLearnScope() {
      console.log(a, b)
      if (true) {
        console.log(a, b)
      }
    }
    console.log(a, b) // accessible
    ```
    
    ### Global scope
    
    A globally declared variable can be accessed every where in the same file. But the term global is relative. It can be global to the file or it can be global relative to some block of codes.
    
    ```jsx
    //scope.js
    let a = 'JavaScript' // is a global scope it will be found anywhere in this file
    let b = 10 // is a global scope it will be found anywhere in this file
    function letsLearnScope() {
      console.log(a, b) // JavaScript 10, accessible
      if (true) {
        let a = 'Python'
        let b = 100
        console.log(a, b) // Python 100
      }
      console.log(a, b)
    }
    letsLearnScope()
    console.log(a, b) // JavaScript 10, accessible
    ```
    
    ### Local scope
    
    A variable declared as local can be accessed only in certain block code.
    
    - Block Scope
    - Function Scope
    
    ```jsx
    //scope.js
    let a = 'JavaScript' // is a global scope it will be found anywhere in this file
    let b = 10 // is a global scope it will be found anywhere in this file
    // Function scope
    function letsLearnScope() {
      console.log(a, b) // JavaScript 10, accessible
      let value = false
    // block scope
      if (true) {
        // we can access from the function and outside the function but
        // variables declared inside the if will not be accessed outside the if block
        let a = 'Python'
        let b = 20
        let c = 30
        let d = 40
        value = !value
        console.log(a, b, c, value) // Python 20 30 true
      }
      // we can not access c because c's scope is only the if block
      console.log(a, b, value) // JavaScript 10 true
    }
    letsLearnScope()
    console.log(a, b) // JavaScript 10, accessible
    ```
    
    Now, you have an understanding of scope. A variable declared with *var* only scoped to function but variable declared with *let* or *const* is block scope(function block, if block, loop block, etc). Block in JavaScript is a code in between two curly brackets ({}).
    
    ```jsx
    //scope.js
    function letsLearnScope() {
      var gravity = 9.81
      console.log(gravity)
    
    }
    // console.log(gravity), Uncaught ReferenceError: gravity is not defined
    
    if (true){
      var gravity = 9.81
      console.log(gravity) // 9.81
    }
    console.log(gravity)  // 9.81
    
    for(var i = 0; i < 3; i++){
      console.log(i) // 0, 1, 2
    }
    console.log(i) // 3
    ```
    
    In ES6 and above there is *let* and *const*, so you will not suffer from the sneakiness of *var*. When we use *let* our variable is block scoped and it will not infect other parts of our code.
    
    ```jsx
    //scope.js
    function letsLearnScope() {
      // you can use let or const, but gravity is constant I prefer to use const
      const gravity = 9.81
      console.log(gravity)
    
    }
    // console.log(gravity), Uncaught ReferenceError: gravity is not defined
    
    if (true){
      const  gravity = 9.81
      console.log(gravity) // 9.81
    }
    // console.log(gravity), Uncaught ReferenceError: gravity is not defined
    
    for(let i = 0; i < 3; i++){
      console.log(i) // 0, 1, 2
    }
    // console.log(i), Uncaught ReferenceError: i is not defined
    ```
    
    The scope *let* and *const* are the same. The difference is only reassigning. We can not change or reassign the value of the `const` variable. It is suggested to use *let* and *const*, by using *let* and *const* you will write clean code and avoid hard to debug mistakes. As a rule of thumb, you can use *let* for any value which change, *const* for any constant value, and for an array, object, arrow function and function expression.
    
- **Object**
    
    ### Creating an empty object
    
    An empty object
    
    ```jsx
    const person = {}
    ```
    
    ### Creating an objecting with values
    
    Now, the person object has firstName, lastName, age, location, skills and isMarried properties. The value of properties or keys could be a string, number, boolean, an object, null, undefined or a function.
    
    Let us see some examples of object. Each key has a value in the object.
    
    ```jsx
    const rectangle = {
      length: 20,
      width: 20
    }
    console.log(rectangle) // {length: 20, width: 20}
    
    const person = {
      firstName: 'Asabeneh',
      lastName: 'Yetayeh',
      age: 250,
      country: 'Finland',
      city: 'Helsinki',
      skills: [
        'HTML',
        'CSS',
        'JavaScript',
        'React',
        'Node',
        'MongoDB',
        'Python',
        'D3.js'
      ],
      isMarried: true
    }
    console.log(person)
    ```
    
    ### Getting values from an object
    
    We can access values of object using two methods:
    
    - using . followed by key name if the key-name is a one word
    - using square bracket and a quote
    
    ```jsx
    const person = {
      firstName: 'Asabeneh',
      lastName: 'Yetayeh',
      age: 250,
      country: 'Finland',
      city: 'Helsinki',
      skills: [
        'HTML',
        'CSS',
        'JavaScript',
        'React',
        'Node',
        'MongoDB',
        'Python',
        'D3.js'
      ],
      getFullName: function() {
        return `${this.firstName}${this.lastName}`
      },
      'phone number': '+3584545454545'
    }
    
    // accessing values using .
    console.log(person.firstName)
    console.log(person.lastName)
    console.log(person.age)
    console.log(person.location) // undefined
    
    // value can be accessed using square bracket and key name
    console.log(person['firstName'])
    console.log(person['lastName'])
    console.log(person['age'])
    console.log(person['age'])
    console.log(person['location']) // undefined
    
    // for instance to access the phone number we only use the square bracket method
    console.log(person['phone number'])
    ```
    
    ### Creating object methods
    
     The getFullName is function inside the person object and we call it an object method. The *this* key word refers to the object itself. We can use the word *this* to access the values of different properties of the object. We can not use an arrow function as object method because the word this refers to the window inside an arrow function instead of the object itself. Example of object:
    
    ```
    const person = {
      firstName: 'Asabeneh',
      lastName: 'Yetayeh',
      age: 250,
      country: 'Finland',
      city: 'Helsinki',
      skills: [
        'HTML',
        'CSS',
        'JavaScript',
        'React',
        'Node',
        'MongoDB',
        'Python',
        'D3.js'
      ],
      getFullName: function() {
        return `${this.firstName} ${this.lastName}`
      }
    }
    
    console.log(person.getFullName())
    // Asabeneh Yetayeh
    ```
    
    ### Setting new key for an object
    
    An object is a mutable data structure and we can modify the content of an object after it gets created.
    
    Setting a new keys in an object
    
    ```jsx
    const person = {
      firstName: 'Asabeneh',
      lastName: 'Yetayeh',
      age: 250,
      country: 'Finland',
      city: 'Helsinki',
      skills: [
        'HTML',
        'CSS',
        'JavaScript',
        'React',
        'Node',
        'MongoDB',
        'Python',
        'D3.js'
      ],
      getFullName: function() {
        return `${this.firstName} ${this.lastName}`
      }
    }
    person.nationality = 'Ethiopian'
    person.country = 'Finland'
    person.title = 'teacher'
    person.skills.push('Meteor')
    person.skills.push('SasS')
    person.isMarried = true
    
    person.getPersonInfo = function() {
      let skillsWithoutLastSkill = this.skills
        .splice(0, this.skills.length - 1)
        .join(', ')
      let lastSkill = this.skills.splice(this.skills.length - 1)[0]
    
      let skills = `${skillsWithoutLastSkill}, and ${lastSkill}`
      let fullName = this.getFullName()
      let statement = `${fullName} is a ${this.title}.\nHe lives in ${this.country}.\nHe teaches ${skills}.`
      return statement
    }
    console.log(person)
    console.log(person.getPersonInfo())
    // output Asabeneh Yetayeh is a teacher.
    // He lives in Finland.
    // He teaches HTML, CSS, JavaScript, React, Node, MongoDB, Python, D3.js, Meteor, and SasS.
    ```
    
    ### Object Methods
    
    There are different methods to manipulate an object. Let us see some of the available methods.
    
    *Object.assign*: To copy an object without modifying the original object
    
    ```jsx
    const person = {
      firstName: 'Asabeneh',
      age: 250,
      country: 'Finland',
      city:'Helsinki',
      skills: ['HTML', 'CSS', 'JS'],
      title: 'teacher',
      address: {
        street: 'Heitamienkatu 16',
        pobox: 2002,
        city: 'Helsinki'
      },
      getPersonInfo: function() {
        return `I am ${this.firstName} and I live in ${this.city}, ${this.country}. I am ${this.age}.`
      }
    }
    
    //Object methods: Object.assign, Object.keys, Object.values, Object.entries
    //hasOwnProperty
    
    const copyPerson = Object.assign({}, person)
    console.log(copyPerson)
    ```
    
    ### Getting object keys using Object.keys()
    
    *Object.keys*: To get the keys or properties of an object as an array
    
    ```jsx
    const keys = Object.keys(copyPerson)
    console.log(keys) //['firstName', 'age', 'country','city', 'skills','title', 'address', 'getPersonInfo']
    const address = Object.keys(copyPerson.address)
    console.log(address) //['street', 'pobox', 'city']
    ```
    
    ### Getting object values using Object.values()
    
    *Object.values*:To get values of an object as an array
    
    ```jsx
    const values = Object.values(copyPerson)
    console.log(values)
    ```
    
    ### Getting object keys and values using Object.entries()
    
    *Object.entries*:To get the keys and values in an array
    
    ```jsx
    const entries = Object.entries(copyPerson)
    console.log(entries)
    ```
    
    ### Checking properties using hasOwnProperty()
    
    *hasOwnProperty*: To check if a specific key or property exist in an object
    
    ```jsx
    console.log(copyPerson.hasOwnProperty('name'))
    console.log(copyPerson.hasOwnProperty('score'))
    ```
    
- **Higher Order Function**
    
    Higher order functions are functions which take other function as a parameter or return a function as a value. The function passed as a parameter is called callback.
    
    ### Callback
    
    A callback is a function which can be passed as parameter to other function. See the example below.
    
    ```jsx
    // a callback function, the name of the function could be any name
    const callback = (n) => {
      return n ** 2
    }
    
    // function that takes other function as a callback
    function cube(callback, n) {
      return callback(n) * n
    }
    
    console.log(cube(callback, 3))
    ```
    
    ### Returning function
    
    Higher order functions return function as a value
    
    ```jsx
    // Higher order function returning an other function
    const higherOrder = n => {
      const doSomething = m => {
        const doWhatEver = t => {
          return 2 * n + 3 * m + t
        }
        return doWhatEver
      }
      return doSomething
    }
    console.log(higherOrder(2)(3)(10))
    ```
    
    Let us see were we use call back functions. For instance the *forEach* method uses call back.
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    const sumArray = arr => {
      let sum = 0
      const callback = function(element) {
        sum += element
      }
      arr.forEach(callback)
      return sum
    
    }
    console.log(sumArray(numbers))
     
    // output 15
    ```
    
    The above example can be simplified as follows:
    
    ```jsx
    const numbers = [1, 2, 3, 4]
    
    const sumArray = arr => {
      let sum = 0
      arr.forEach(function(element) {
        sum += element
      })
      return sum
    
    }
    console.log(sumArray(numbers))
    // output 15
    ```
    
    ### Setting time
    
    we can execute some activities in a certain interval of time or we can schedule(wait) for some time to execute some activities.
    
    - setInterval
    - setTimeout
    
    ### Setting Interval using a setInterval function
    
    he setInterval global method take a callback function and a duration as a parameter. The duration is in milliseconds and the callback will be always called in that interval of time.
    
    ```jsx
    // syntax
    function callback() {
      // code goes here
    }
    setInterval(callback, duration)
    ```
    
    ```jsx
    function sayHello() {
      console.log('Hello')
    }
    setInterval(sayHello, 1000) // it prints hello in every second, 1000ms is 1s
    ```
    
    ### Setting a time using a setTimeout
    
    In JavaScript, we use setTimeout higher order function to execute some action at some time in the future. The setTimeout global method take a callback function and a duration as a parameter. The duration is in milliseconds and the callback wait for that amount of time.
    
    ```jsx
    // syntax
    function callback() {
      // code goes here
    }
    setTimeout(callback, duration) // duration in milliseconds
    ```
    
    ```jsx
    function sayHello() {
      console.log('Hello')
    }
    setTimeout(sayHello, 2000) // it prints hello after it waits for 2 seconds.
    ```
    
    ## Functional Programming
    
    Instead of writing regular loop, latest version of JavaScript introduced lots of built in methods which can help us to solve complicated problems. All builtin methods take callback function. In this section, we will see *forEach*, *map*, *filter*, *reduce*, *find*, *every*, *some*, and *sort*.
    
    ### forEach
    
    *forEach*: Iterate an array elements. We use *forEach* only with arrays. It takes a callback function with elements, index parameter and array itself. The index and the array optional.
    
    ```jsx
    arr.forEach(function (element, index, arr) {
      console.log(index, element, arr)
    })
    // The above code can be written using arrow function
    arr.forEach((element, index, arr) => {
      console.log(index, element, arr)
    })
    // The above code can be written using arrow function and explicit return
    arr.forEach((element, index, arr) => console.log(index, element, arr))
    ```
    
    ```jsx
    let sum = 0;
    const numbers = [1, 2, 3, 4, 5];
    numbers.forEach(num => console.log(num))
    console.log(sum)
    // output 
    //1
    //2
    //3
    //4
    //5
    ```
    
    ```jsx
    let sum = 0;
    const numbers = [1, 2, 3, 4, 5];
    numbers.forEach(num => sum += num)
    
    console.log(sum)
    // output 15
    ```
    
    ```jsx
    const countries = ['Finland', 'Denmark', 'Sweden', 'Norway', 'Iceland']
    countries.forEach((element) => console.log(element.toUpperCase()))
    // output FINLAND
    //DENMARK
    //SWEDEN
    //NORWAY
    //ICELAND
    ```
    
    ### map
    
    *map*: Iterate an array elements and modify the array elements. It takes a callback function with elements, index , array parameter and return a new array.
    
    ```jsx
    const modifiedArray = arr.map(function (element, index, arr) {
      return element
    })
    ```
    
    ```jsx
    /*Arrow function and explicit return
    const modifiedArray = arr.map((element,index) => element);
    */
    //Example
    const numbers = [1, 2, 3, 4, 5]
    const numbersSquare = numbers.map((num) => num * num)
    
    console.log(numbersSquare)
    // output [1, 4, 9, 16, 25]
    ```
    
    ```jsx
    const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
    const namesToUpperCase = names.map((name) => name.toUpperCase())
    console.log(namesToUpperCase)
    // output [1, 4, 9, 16, 25]
    ```
    
    ```jsx
    const countries = [
      'Albania',
      'Bolivia',
      'Canada',
      'Denmark',
      'Ethiopia',
      'Finland',
      'Germany',
      'Hungary',
      'Ireland',
      'Japan',
      'Kenya',
    ]
    const countriesToUpperCase = countries.map((country) => country.toUpperCase())
    console.log(countriesToUpperCase)
    
    /*
    // Arrow function
    const countriesToUpperCase = countries.map((country) => {
      return country.toUpperCase();
    })
    //Explicit return arrow function
    const countriesToUpperCase = countries.map(country => country.toUpperCase());
    */
    // output ['ALBANIA', 'BOLIVIA', 'CANADA', 'DENMARK', 'ETHIOPIA', 'FINLAND', 'GERMANY', 'HUNGARY', 'IRELAND', 'JAPAN', 'KENYA']
    ```
    
    ```jsx
    const countriesFirstThreeLetters = countries.map((country) =>
      country.toUpperCase().slice(0, 3)
    )
    ["ALB", "BOL", "CAN", "DEN", "ETH", "FIN", "GER", "HUN", "IRE", "JAP", "KEN"]
    ```
    
    ### filter
    
    *Filter*: Filter out items which full fill filtering conditions and return a new array.
    
    ```jsx
    //Filter countries containing land
    const countriesContainingLand = countries.filter((country) =>
      country.includes('land')
    )
    console.log(countriesContainingLand)
    // output ['Finland', 'Ireland']
    ```
    
    ```jsx
    const countriesEndsByia = countries.filter((country) => country.endsWith('ia'))
    console.log(countriesEndsByia)
    // output ['Albania', 'Bolivia','Ethiopia']
    ```
    
    ```jsx
    const countriesHaveFiveLetters = countries.filter(
      (country) => country.length === 5
    )
    console.log(countriesHaveFiveLetters)
    // output ['Japan', 'Kenya']
    ```
    
    ```jsx
    const scores = [
      { name: 'Asabeneh', score: 95 },
       { name: 'Lidiya', score: 98 },
      { name: 'Mathias', score: 80 },
      { name: 'Elias', score: 50 },
      { name: 'Martha', score: 85 },
      { name: 'John', score: 100 },
    ]
    
    const scoresGreaterEighty = scores.filter((score) => score.score > 80)
    console.log(scoresGreaterEighty)
    
    // output [{name: 'Asabeneh', score: 95}, { name: 'Lidiya', score: 98 },{name: 'Martha', score: 85},{name: 'John', score: 100}]
    ```
    
    ### reduce
    
    *reduce*: Reduce takes a callback function. The call back function takes accumulator, current, and optional initial value as a parameter and returns a single value. It is a good practice to define an initial value for the accumulator value. If we do not specify this parameter, by default accumulator will get array `first value`. If our array is an *empty array*, then `Javascript` will throw an error.
    
    ```jsx
    arr.reduce((acc, cur) => {
      // some operations goes here before returning a value
     return
    }, initialValue)
    ```
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    const sum = numbers.reduce((acc, cur) => acc + cur, 0)
    
    console.log(sum)
    // output 15
    ```
    
    ### every
    
    *every*: Check if all the elements are similar in one aspect. It returns boolean
    
    ```jsx
    const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
    const areAllStr = names.every((name) => typeof name === 'string') // Are all strings?
    
    console.log(areAllStr)
    // output true
    ```
    
    ```jsx
    const bools = [true, true, true, true]
    const areAllTrue = bools.every((b) => b === true) // Are all true?
    
    console.log(areAllTrue) // true
    ```
    
    ### find
    
    *find*: Return the first element which satisfies the condition
    
    ```jsx
    const ages = [24, 22, 25, 32, 35, 18]
    const age = ages.find((age) => age < 20)
    
    console.log(age)
    // output 18
    ```
    
    ```jsx
    const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
    const result = names.find((name) => name.length > 7)
    console.log(result)
    // output Asabeneh
    ```
    
    ```jsx
    const scores = [
      { name: 'Asabeneh', score: 95 },
      { name: 'Mathias', score: 80 },
      { name: 'Elias', score: 50 },
      { name: 'Martha', score: 85 },
      { name: 'John', score: 100 },
    ]
    
    const score = scores.find((user) => user.score > 80)
    console.log(score)
    // output { name: "Asabeneh", score: 95 }
    ```
    
    ### findIndex
    
    *findIndex*: Return the position of the first element which satisfies the condition
    
    ```jsx
    const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
    const ages = [24, 22, 25, 32, 35, 18]
    
    const result = names.findIndex((name) => name.length > 7)
    console.log(result) // 0
    
    const age = ages.findIndex((age) => age < 20)
    console.log(age) // 5
    ```
    
    ### some
    
    *some*: Check if some of the elements are similar in one aspect. It returns boolean
    
    ```jsx
    const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
    const bools = [true, true, true, true]
    
    const areSomeTrue = bools.some((b) =>  b === true)
    
    console.log(areSomeTrue) //true
    ```
    
    ```jsx
    const areAllStr = names.some((name) => typeof name === 'number') // Are all strings ?
    console.log(areAllStr) // false
    ```
    
    ### sort
    
    *sort*: The sort methods arranges the array elements either ascending or descending order. By default, the ***sort()*** method sorts values as strings.This works well for string array items but not for numbers. If number values are sorted as strings and it give us wrong result. Sort method modify the original array. It is recommended to copy the original data before you start using *sort* method.
    
    ### Sorting string values
    
    ```
    const products = ['Milk', 'Coffee', 'Sugar', 'Honey', 'Apple', 'Carrot']
    console.log(products.sort()) // ['Apple', 'Carrot', 'Coffee', 'Honey', 'Milk', 'Sugar']
    //Now the original products array  is also sorted
    ```
    
    ### Sorting Numeric values
    
    Sort converts items to string , since '100' and other numbers compared, 1 which the beginning of the string '100' became the smallest. To avoid this, we use a compare call back function inside the sort method, which return a negative, zero or positive.
    
    ```jsx
    const numbers = [9.81, 3.14, 100, 37]
    // Using sort method to sort number items provide a wrong result. see below
    console.log(numbers.sort()) //[100, 3.14, 37, 9.81]
    numbers.sort(function (a, b) {
      return a - b
    })
    
    console.log(numbers) // [3.14, 9.81, 37, 100]
    
    numbers.sort(function (a, b) {
      return b - a
    })
    console.log(numbers) //[100, 37, 9.81, 3.14]
    ```
    
    ### Sorting Object Arrays
    
    Whenever we sort objects in an array, we use the object key to compare. Let us see the example below.
    
    ```jsx
    objArr.sort(function (a, b) {
      if (a.key < b.key) return -1
      if (a.key > b.key) return 1
      return 0
    })
    
    // or
    
    objArr.sort(function (a, b) {
      if (a['key'] < b['key']) return -1
      if (a['key'] > b['key']) return 1
      return 0
    })
    
    const users = [
      { name: 'Asabeneh', age: 150 },
      { name: 'Brook', age: 50 },
      { name: 'Eyob', age: 100 },
      { name: 'Elias', age: 22 },
    ]
    users.sort((a, b) => {
      if (a.age < b.age) return -1
      if (a.age > b.age) return 1
      return 0
    })
    console.log(users) // sorted ascending
    // [{…}, {…}, {…}, {…}]
    ```
    
- **Functions**
    
    A function is a reusable block of code or programming statements designed to perform a certain task. To store a data to a function, a function has to return certain data types. To get the value we call or invoke a function. Function makes code:
    
    - clean and easy to read
    - reusable
    - easy to test
    
    A function can be declared or created in couple of ways:
    
    - *Declaration function*
    - *Expression function*
    - *Anonymous function*
    - *Arrow function*
    
    ### Function Declaration
    
    Let us see how to declare a function and how to call a function.
    
    ```jsx
    //declaring a function without a parameter
    function functionName() {
      // code goes here
    }
    functionName() // calling function by its name and with parentheses
    ```
    
    ### Function without a parameter and return
    
    Function can be declared without a parameter.
    
    **Example:**
    
    ```jsx
    // function without parameter,  a function which make a number square
    function square() {
      let num = 2
      let sq = num * num
      console.log(sq)
    }
    
    square() // 4
    
    // function without parameter
    function addTwoNumbers() {
      let numOne = 10
      let numTwo = 20
      let sum = numOne + numTwo
    
      console.log(sum)
    }
    
    addTwoNumbers() // a function has to be called by its name to be executed
    ```
    
    ```jsx
      function printFullName (){
          let firstName = 'Asabeneh'
          let lastName = 'Yetayeh'
          let space = ' '
          let fullName = firstName + space + lastName
          console.log(fullName)
    }
    
    printFullName() // calling a function
    ```
    
    ### Function returning value
    
    Function can also return values, if a function does not return values the value of the function is undefined. 
    
    ```jsx
    function printFullName (){
          let firstName = 'Asabeneh'
          let lastName = 'Yetayeh'
          let space = ' '
          let fullName = firstName + space + lastName
          return fullName
    }
    console.log(printFullName())
    ```
    
    ```jsx
      function addTwoNumbers() {
          let numOne = 2
          let numTwo = 3
          let total = numOne + numTwo
          return total
    
      }
    
    console.log(addTwoNumbers())
    ```
    
    ### Function with a parameter
    
    In a function we can pass different data types(number, string, boolean, object, function) as a parameter.
    
    ```jsx
    // function with one parameter
    function functionName(parm1) {
      //code goes her
    }
    functionName(parm1) // during calling or invoking one argument needed
    
    function areaOfCircle(r) {
      let area = Math.PI * r * r
      return area
    }
    
    console.log(areaOfCircle(10)) // should be called with one argument
    
    function square(number) {
      return number * number
    }
    
    console.log(square(10))
    ```
    
    ### Function with two parameters
    
    ```jsx
    // function with two parameters
    function functionName(parm1, parm2) {
      //code goes her
    }
    functionName(parm1, parm2) // during calling or invoking two arguments needed
    // Function without parameter doesn't take input, so lets make a function with parameters
    function sumTwoNumbers(numOne, numTwo) {
      let sum = numOne + numTwo
      console.log(sum)
    }
    sumTwoNumbers(10, 20) // calling functions
    // If a function doesn't return it doesn't store data, so it should return
    
    function sumTwoNumbers(numOne, numTwo) {
      let sum = numOne + numTwo
      return sum
    }
    
    console.log(sumTwoNumbers(10, 20))
    function printFullName(firstName, lastName) {
      return `${firstName} ${lastName}`
    }
    console.log(printFullName('Asabeneh', 'Yetayeh'))
    ```
    
    ### Function with many parameters
    
    ```jsx
    // function with multiple parameters
    function functionName(parm1, parm2, parm3,...){
      //code goes here
    }
    functionName(parm1,parm2,parm3,...) // during calling or invoking three arguments needed
    
    // this function takes array as a parameter and sum up the numbers in the array
    function sumArrayValues(arr) {
      let sum = 0;
      for (let i = 0; i < arr.length; i++) {
        sum = sum + arr[i];
      }
      return sum;
    }
    const numbers = [1, 2, 3, 4, 5];
        //calling a function
    console.log(sumArrayValues(numbers));
    
        const areaOfCircle = (radius) => {
          let area = Math.PI * radius * radius;
          return area;
        }
    console.log(areaOfCircle(10))
    ```
    
    ### Function with unlimited number of parameters
    
    ### Unlimited number of parameters in regular function
    
    A function declaration provides a function scoped arguments array like object. Any thing we passed as argument in the function can be accessed from arguments object inside the functions. example
    
    ```jsx
    // Let us access the arguments object
    
    function sumAllNums() {
     console.log(arguments)
    }
    
    sumAllNums(1, 2, 3, 4)
    // Arguments(4) [1, 2, 3, 4, callee: ƒ, Symbol(Symbol.iterator): ƒ]
    ```
    
    ```jsx
    // function declaration
    
    function sumAllNums() {
      let sum = 0
      for (let i = 0; i < arguments.length; i++) {
        sum += arguments[i]
      }
      return sum
    }
    
    console.log(sumAllNums(1, 2, 3, 4)) // 10
    console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
    console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
    ```
    
    ### Unlimited number of parameters in arrow function
    
    Arrow function does not have the function scoped arguments object. To implement a function which takes unlimited number of arguments in an arrow function we use spread operator followed by any parameter name. Any thing we passed as argument in the function can be accessed as array in the arrow function. Let us see an example
    
    ```jsx
    // Let us access the arguments object
    
    const sumAllNums = (...args) => {
     // console.log(arguments), arguments object not found in arrow function
     // instead we use a parameter followed by spread operator (...)
     console.log(args)
    }
    
    sumAllNums(1, 2, 3, 4)
    // [1, 2, 3, 4]
    ```
    
    ```jsx
    // function declaration
    
    const sumAllNums = (...args) => {
      let sum = 0
      for (const element of args) {
        sum += element
      }
      return sum
    }
    
    console.log(sumAllNums(1, 2, 3, 4)) // 10
    console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
    console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
    ```
    
    ### Anonymous Function
    
    Anonymous function or without name
    
    ```jsx
    const anonymousFun = function() {
      console.log(
        'I am an anonymous function and my value is stored in anonymousFun'
      )
    }
    ```
    
    ### Expression Function
    
    Expression functions are anonymous functions. After we create a function without a name and we assign it to a variable. To return a value from the function we should call the variable. Look at the example below.
    
    ```jsx
    // Function expression
    const square = function(n) {
      return n * n
    }
    
    console.log(square(2)) // -> 4
    ```
    
    ### Self Invoking Functions
    
    Self invoking functions are anonymous functions which do not need to be called to return a value.
    
    ```jsx
    (function(n) {
      console.log(n * n)
    })(2) // 4, but instead of just printing if we want to return and store the data, we do as shown below
    
    let squaredNum = (function(n) {
      return n * n
    })(10)
    
    console.log(squaredNum)
    ```
    
    ### Arrow Function
    
    Arrow function is an alternative to write a function, however function declaration and arrow function have some minor differences.
    
    Arrow function uses arrow instead of the keyword *function* to declare a function. Let us see both function declaration and arrow function.
    
    ```jsx
    // This is how we write normal or declaration function
    // Let us change this declaration function to an arrow function
    function square(n) {
      return n * n
    }
    
    console.log(square(2)) // 4
    
    const square = n => {
      return n * n
    }
    
    console.log(square(2))  // -> 4
    
    // if we have only one line in the code block, it can be written as follows, explicit return
    const square = n => n * n  // -> 4
    ```
    
    ```jsx
    const changeToUpperCase = arr => {
      const newArr = []
      for (const element of arr) {
        newArr.push(element.toUpperCase())
      }
      return newArr
    }
    
    const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
    console.log(changeToUpperCase(countries))
    
    // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
    ```
    
    ```jsx
    const printFullName = (firstName, lastName) => {
      return `${firstName} ${lastName}`
    }
    
    console.log(printFullName('Asabeneh', 'Yetayeh'))
    ```
    
    The above function has only the return statement, therefore, we can explicitly return it as follows.
    
    ```jsx
    const printFullName = (firstName, lastName) => `${firstName} ${lastName}`
    
    console.log(printFullName('Asabeneh', 'Yetayeh'))
    ```
    
    ### Function with default parameters
    
    Sometimes we pass default values to parameters, when we invoke the function if we do not pass an argument the default value will be used. Both function declaration and arrow function can have a default value or values.
    
    ```java
    // syntax
    // Declaring a function
    function functionName(param = value) {
      //codes
    }
    
    // Calling function
    functionName()
    functionName(arg)
    ```
    
    **Example:**
    
    ```jsx
    function greetings(name = 'Peter') {
      let message = `${name}, welcome to 30 Days Of JavaScript!`
      return message
    }
    
    console.log(greetings())
    console.log(greetings('Asabeneh'))
    ```
    
    ```jsx
    function generateFullName(firstName = 'Asabeneh', lastName = 'Yetayeh') {
      let space = ' '
      let fullName = firstName + space + lastName
      return fullName
    }
    
    console.log(generateFullName())
    console.log(generateFullName('David', 'Smith'))
    ```
    
    ```jsx
    function calculateAge(birthYear, currentYear = 2019) {
      let age = currentYear - birthYear
      return age
    }
    
    console.log('Age: ', calculateAge(1819))
    ```
    
    ```jsx
    function weightOfObject(mass, gravity = 9.81) {
      let weight = mass * gravity + ' N' // the value has to be changed to string first
      return weight
    }
    
    console.log('Weight of an object in Newton: ', weightOfObject(100)) // 9.81 gravity at the surface of Earth
    console.log('Weight of an object in Newton: ', weightOfObject(100, 1.62)) // gravity at surface of Moon
    ```
    
    Let us see how we write the above functions with arrow functions
    
    ```jsx
    // syntax
    // Declaring a function
    const functionName = (param = value) => {
      //codes
    }
    
    // Calling function
    functionName()
    functionName(arg)
    ```
    
    **Example:**
    
    ```jsx
    const greetings = (name = 'Peter') => {
      let message = name + ', welcome to 30 Days Of JavaScript!'
      return message
    }
    
    console.log(greetings())
    console.log(greetings('Asabeneh'))
    ```
    
    ```jsx
    const generateFullName = (firstName = 'Asabeneh', lastName = 'Yetayeh') => {
      let space = ' '
      let fullName = firstName + space + lastName
      return fullName
    }
    
    console.log(generateFullName())
    console.log(generateFullName('David', 'Smith'))
    ```
    
    ```jsx
    const calculateAge = (birthYear, currentYear = 2019) => currentYear - birthYear
    console.log('Age: ', calculateAge(1819))
    ```
    
    ```jsx
    const weightOfObject = (mass, gravity = 9.81) => mass * gravity + ' N'
    
    console.log('Weight of an object in Newton: ', weightOfObject(100)) // 9.81 gravity at the surface of Earth
    console.log('Weight of an object in Newton: ', weightOfObject(100, 1.62)) // gravity at surface of Moon
    ```
    
- **Loops**
    
    **for Loop**
    
    ```jsx
    // For loop structure
    for(initialization, condition, increment/decrement){
      // code goes here
    }
    ```
    
    ```jsx
    for(let i = 0; i <= 5; i++){
      console.log(i)
    }
    
    // 0 1 2 3 4 5
    ```
    
    ```jsx
    for(let i = 5; i >= 0; i--){
      console.log(i)
    }
    
    // 5 4 3 2 1 0
    ```
    
    ```jsx
    for(let i = 0; i <= 5; i++){
      console.log(`${i} * ${i} = ${i * i}`)
    }
    ```
    
    ```jsx
    0 * 0 = 0
    1 * 1 = 1
    2 * 2 = 4
    3 * 3 = 9
    4 * 4 = 16
    5 * 5 = 25
    ```
    
    ```jsx
    const countries = ['Finland', 'Sweden', 'Denmark', 'Norway', 'Iceland']
    const newArr = []
    for(let i = 0; i < countries.length; i++){
      newArr.push(countries[i].toUpperCase())
    }
    
    // ["FINLAND", "SWEDEN", "DENMARK", "NORWAY", "ICELAND"]
    ```
    
    Adding all elements in the array
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    let sum = 0
    for(let i = 0; i < numbers.length; i++){
      sum  = sum + numbers[i]  // can be shorten, sum += numbers[i]
    
    }
    
    console.log(sum)  // 15
    ```
    
    Creating a new array based on the existing array
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    const newArr = []
    let sum = 0
    for(let i = 0; i < numbers.length; i++){
      newArr.push( numbers[i] ** 2)
    
    }
    
    console.log(newArr)  // [1, 4, 9, 16, 25]
    ```
    
    ```jsx
    const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
    const newArr = []
    for(let i = 0; i < countries.length; i++){
      newArr.push(countries[i].toUpperCase())
    }
    
    console.log(newArr)  // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
    ```
    
    ### while loop
    
    ```jsx
    let i = 0
    while (i <= 5) {
      console.log(i)
      i++
    }
    
    // 0 1 2 3 4 5
    ```
    
    ### do while loop
    
    ```jsx
    let i = 0
    do {
      console.log(i)
      i++
    } while (i <= 5)
    
    // 0 1 2 3 4 5
    ```
    
    ### for of loop
    
    We use for of loop for arrays. It is very hand way to iterate through an array if we are not interested in the index of each element in the array.
    
    ```jsx
    for (const element of arr) {
      // code goes here
    }
    ```
    
    ```jsx
    const numbers = [1, 2, 3, 4, 5]
    
    for (const num of numbers) {
      console.log(num)
    }
    
    // 1 2 3 4 5
    
    for (const num of numbers) {
      console.log(num * num)
    }
    
    // 1 4 9 16 25
    
    // adding all the numbers in the array
    let sum = 0
    for (const num of numbers) {
      sum = sum + num
    	// can be also shorten like this, sum += num
      // after this we will use the shorter synthax(+=, -=, *=, /= etc)
    }
    console.log(sum) // 15
    
    const webTechs = [
      'HTML',
      'CSS',
      'JavaScript',
      'React',
      'Redux',
      'Node',
      'MongoDB'
    ]
    
    for (const tech of webTechs) {
      console.log(tech.toUpperCase())
    }
    
    // HTML CSS JAVASCRIPT REACT NODE MONGODB
    
    for (const tech of webTechs) {
      console.log(tech[0]) // get only the first letter of each element,  H C J R N M
    }
    ```
    
    ```jsx
    const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
    const newArr = []
    for(const country of countries){
      newArr.push(country.toUpperCase())
    }
    
    console.log(newArr)  // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
    ```
    
    ### break
    
    Break is used to interrupt a loop.
    
    ```jsx
    for(let i = 0; i <= 5; i++){
      if(i == 3){
        break
      }
      console.log(i)
    }
    
    // 0 1 2
    ```
    
    The above code stops if 3 found in the iteration process.
    
    ### continue
    
    We use the keyword *continue* to skip a certain iterations.
    
    ```jsx
    for(let i = 0; i <= 5; i++){
      if(i == 3){
        continue
      }
      console.log(i)
    }
    
    // 0 1 2 4 5
    ```
    

l