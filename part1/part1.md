1. 'i' will store the length of the 'prices' array since 'i' is declared using the keyword 'var', and 'var' has no block scope. Thus, 'console.log()' still has access to 'i' even though it is declared in the for loop.
2. Since 'discountedPrice' is declared using 'var', it tolerates redeclarations. In other words, 'discountedPrice' is reset to a new value that is 'prices[i] * (1 - discount);' each loop iteration.
3. 'finalPrice' is reset to a new value that is 'Math.round(discountedPrice * 100) / 100;' each loop iteration since it is declared outside of the for loop.
4. The function returns the 'discounted' array, which has the value '[ 50, 100, 150 ]'. The 'discounted' array is local to the whole function since it is declared outside of the for loop, and it can be modified since it is declared not using a 'const'. During each loop iteration, the function appends the 'finalPrice' after subtracting the 'discountedPrice'.
5. This will cause an error because 'i' is declared using 'let' which is local to the for loop. Thus, only codes inside the for loop has access to 'i'. Trying to access 'i' outside of the for loop will cause an error since 'i' is not defined.
6. This will cause an error because 'discountedPrice' is declared using 'let'. Similar to question 5, 'discountedPrice' is local to the for loop. So, accessing 'discountedPrice' outside of the for loop causes an error.
7. 'finalPrice' is reset to a new value that is 'Math.round(discountedPrice * 100) / 100;' each loop iteration since it is declared outside of the for loop.
8. The function returns the 'discounted' array, which has the value '[ 50, 100, 150 ]'. The 'discounted' array is local to the whole function since it is declared outside of the for loop, and it can be modified since it is declared not using a 'const'. During each loop iteration, the function appends the 'finalPrice' after subtracting the 'discountedPrice'. 
9. Similar to question 5, this will cause an error because 'i' is declared using 'let' which is local to the for loop. Thus, only codes inside the for loop has access to 'i'. Trying to access 'i' outside of the for loop will cause an error since 'i' is not defined.
10. We don't have access to the variable 'discountedPrice' outside of the for loop since it is declared using 'const' inside the for loop, so it is local to the for loop and can only be accessed inside the for loop.
11. 'finalPrice' is declared using 'const', meaning that it cannot be modified. So, 'finalPrice' will stay at value 0 and attempting to modify 'finalPrice' will cause an error.
12. Similar to question 11, 'discounted' is declared using 'const', meaning that it cannot be modified. So, 'discounted' stays at '[]'.
    
13. 
    A. student.name
    B. student['Grad Year']
    C. student.greeting()
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0]
    
14. 
    A. 32. Since '3' is a string, 2 is converted to a string and is concatenated to 3, resulting to the string '32'.
    B. 1. '3' is converted to a number, and the subtraction is performed. Resulting to 3 - 2 = 1, which is also a number.
    C. 3. null is 0. So, 3 + 0 = 3, which has the type number.
    D. 3null. null is converted to string 'null' and concatenated to 3, resulting to 3null, which is a string.
    E. 4. Since 'true' is the number 1. So, 1 + 3 = 4, which is a number.
    F. 1. Since 'true' is the number 1 and 'null' is the number 0. So, 1 + 0 = 1, which is a number.
    G. 3undefined. undefined is converted to "undefined" then concatenated to 3.
    H. NaN. undefined is converted to NaN, 3 - NaN results in an error, which is NaN.
15. 
    A. true. '2' is converted to 2, which is > 1.
    B. false. The first character of '2' is '2' and the first character of '12' is 1. '2' > '1', thus false.
    C. true. string '2' becomes the numebr 2, and 2 == 2. 
    D. false. Since we are applying strict equality here. So, there is no type conversion '2' is a string and 2 is a number, so they don't have the same type. Thus, false.
    E. false. true is represented as 1, which is not equal to 2.
    F. true. Boolean(2) is true (any non 0 value). So, true === true.
16. == converts types when comparing different data types, whereas === (strict equality) does not.
17. Since true is represented as 1, '2 == true' will evaluate to false. But any non 0 value is true, so 'else if' evaluates to true and executes the statement inside.
19. [ 6, 8, 10 ]. when calling modifyArray([1,2,3], doSomething), doSomething is passed in as the callback function. Inside the for loop, 
the function(x) {return x * 2} that takes a parameter x and returns x * 2 is passed in as argument for callback in doSomething.
During each iteration, a value v from 'array' is passed into the first parameter of doSomething. 
Then, doSomething performs (v + 2) and pass the result to function(x) as its argument. 
function(x) returns x * 2, which is (v + 2) * 2. This result is the return value of doSomething.
Lastly, we push that value to newArr.
21. 
1
4
3
2
The two lines with 'setTimeout' are executed asynchronously with console.log(1) and console.log(4). console.log(3) is executed afer waiting for 0 milliseconds after console.log(4) finishes executing, and console.log(2) waits for 1 second.
