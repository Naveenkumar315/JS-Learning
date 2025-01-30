1. difference between null and undefined in js?
    undefined:
    undefined: when a variable is declared but has not been assigned a value, it is automatically initialized with undefined.

    null:
    null: null variables are intentionally assigned the null value.

let, const is block scope
var is function scope

2. what is the use of typeof operator?
    typeof operator is used to determine the type of each variable.

3. what is type coercion in js?
    is the automatic conversion, is used during String and Number concatenation.
    42 + '42' = '4242'
    string + number
    number + boolean 
    42 + 1 // output 43

Operators & Conditions
---------------------

4.what is operator precedence?
    As per operator precedence, operators with higher precedence are evaluated first.
 BODMAS - Brackets-Order-Division-Multiplications-Additions-Subtraction

 let a = 6, b = 3, c = 2;
 let result = a + b * c + (a - b)
 output: 15


5. what is the difference between unary, binary, and ternary operators?
    Operators based on number of operands
    unary:
    let a = 5
    // Unary operator single operand
    let b = -a;
    output: -5;
    ++a;
    output: 6

    Binary:
    let x = 10
    let y = 3
    // Binary operator two operands
    let z = x + y;
    output: 13

    Ternary:
    Ternary operator - Three operands
    let result = condition ? 'Yes' : 'No'
    output: 'Yes'

6. what is short-circuit evaluation in js?
    AND
    let result = false && test()
    if any one of the condition is false the && operator will return false, but in this case first condition itself it's false. so it return false

    OR
    let result = true || someFunction();
    // Output: true

7. what is a loop? what are the types of loops in JS?
    A loop is a programming way to run a piece of code repeatedly until a certain condition is met.
    types:
    for, while, do-while, for...of, for...in

8. what is the difference between while and for loops?
    for loop allows to iterate a block of code a specific number of times.
    for loop is better for condition with initialization and with increment because all can be set in just one line of code.

    while loop execute a block of code while a certain condition is true.
    while loop is better when there is only condition, no initialization, no increment.

    <!-- while loop -->
    <!-- 
        let j = 0;
        while(j < 5){
            console.log(j)
            j++;
        }
     -->

    <!-- do-while loop -->
    <!-- 
        let k = 0;
        do{
            console.log(k);
            k++
        }while(k > 1)
     -->

9. what is the difference between break and continue statement?
    <!-- break -->
    the break statement is used to terminate the loop.

    <!-- 
        for(let i=0;i<5;i++){
            if(i === 3){
                break;
            }
            console.log(i)
        }
        output: 0,1,2
     -->

    <!-- continue -->
    the continue statement is used to skip the current iteration of the loop and move on to the next iteration.

    <!-- 
        for(let i=0;i<5;i++){
            if(i === 3){
                continue;
            }
            console.log(i)
        }
        output: 0,1,2,4
     -->

10. what is the difference between for and for...of loop in js?

    for loop is slightly more complex having more lines of code whereas for...of is much simpler and better for iterating arrays.

    <!-- 
        let arr = [1,2,3,4,5]
        for(let val of arr){
            console.log(val)
        }
     -->

11. what is the difference between for...of and for...in loop?
    <!-- for of  -->
    for...of loop is used to loop through the values of an object like arrays, strings.

    it allows you to access each value directly, without having to use an index.
    
     <!-- 
     let array = [1,2,3]
        for(let val of array){
            console.log(val)
        } 
        output: 1 2 3 -->

    <!-- for-in loop -->
        for...in loop is used to loop through the properties of an object.

        it allows you to iterate over the keys of an object and access the values associated by using keys as the index.
    <!-- for-in loop -->
    <!-- 
        const person = {
            name: 'Happy',
            role: 'Developer'
        }
        for(let key in person){
            console.log(person[key])
        } 
        output: Happy Developer
    -->

12. what is forEach method? compare it will for...of and fo...in loop?
    forEach() is a method available on arrays or object that allows you to iterate over each element of the array and perform some action on each element.
    