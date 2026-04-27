1. Line 12 will print "3". The variable i begins at 0 and increments 1 up to the length of prices, which is 3. Line 12 prints this variable.
2. Line 13 will print "150". The variable discountedPrice at each iteration of the for loop is set to 0.5 times the i-th element in prices. The last time discountedPrice was updated was for price 300, so it was set to a value of 150. Line 13 prints the last updated value of this variable.
3. Line 14 will print "150". Each iteration of the for loop updates finalPrice with discountedPrice times 100, rounded to the nearest integer, then divided by 100. The last time iteration sets discountedPrice to 150, so finalPrice will be set to 150. Line 14 then prints this value.
4. This function will return the array [50, 100, 150]. Each iteration of the for loop appends finalPrice computed from each element of prices, which means we push 50, 100, then 150 to the discounted array, which is what is returned.
5. This code errors, as i is not defined for line 12. Because we declared i with let rather than var in the for loop, it is only in scope for the for loop. Thus, we can't access it later on.
6. This code errors, as discountedPrice is not defined for line 13. We declared discountedPrice with let in the for loop, meaning it is only in scope in the loop, not after, where we try to print it.
7. Line 14 will print "150". This follows the same behavior as problem 3 because where finalPrice was declared gives it full scope in the function (its block-scope is the whole function), so the functionality is similar to var.
8. The function will return the array [50, 100, 150]. This follows the same behavior as problem 4, even though the array discounted is declared with let (again, its block-scope is the whole function).
9. This code errors, as i is not defined for line 11. We declared i with let in the for loop, so its block scope is the for loop only. It is not defined for the console log statement.
10. Line 12 will print "3". There are no other errors in the code as we don't modify any const variables after declaration. The length variable was set to 3 in line 4 and is printed accordingly in line 12.
11. The function will return the array [50, 100, 150]. The discounted array can still be mutated despite being declared with const (it is only a constant reference), so we can push the prices times the discount without issue. Thus, we push 50, 100, then 150 to the array and that is returned.
12. Notations
    A. student.name
    B. student['Grad Year']
    C. student.greeting()
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0]
13. Arithmetic
    A. '32' - One side is a string so JS does string concatenation.
    B. 1 - The minus operator forces numeric conversion.
    C. 3 - null becomes 0 in numeric addition.
    D. '3null' - One side is a string so JS does string concatenation.
    E. 4 - true becomes 1.
    F. 0 - false and null both are converted to 0.
    G. '3undefined' - One side is a string, JS does string concatenation.
    H. NaN - The minus operator forces numeric conversion, and undefined becomes NaN.
14. Comparison
    A. true - Numeric conversion occurs, 2 > 1.
    B. false - Lexicographic comparison occurs, '2' is after '1'.
    C. true - == allows type coercion, so '2' becomes 2.
    D. false - === requires same value and type, 2 is int and '2' is string.
    E. false - true becomes 1 and 1 != 2
    F. true - Boolean(2) returns primitive true, both sides are true.
15. The == operator checks for equality after type conversion while the === operator checks for equality without type conversion (both the value and type must match).
16. See part2-question16.js
17. The result will be [2, 4, 6]. modifyArray receives two args, array [1, 2, 3] and function doSomething. It creates empty array newArr then loops through the items in [1, 2, 3]. It calls the callback (doSomething) on each item and pushes it; thus, we push 2, 4, then 6 into newArr. Finally, we return newArr, which is [2, 4, 6].
18. See part2-question18.js
19. The output is
```
1
4
3
2
```
When printNums runs, line 2 prints 1 immediately. Line 3 prints 2 after a 1000 ms delay. Line 4 prints 3 after a 0 ms delay (however it does not run immediately, it waits for current synchronous code to finish). Then, line 5 prints 4 immediately. Thus, 1 is printed first, then 4. 3 is printed after 4 (due to the 0 ms delay), then 2 is printed (after 1 second).