1. Line 9 will print "values added: 20"
2. Line 13 will print "final result: 20"
3. We should avoid var here as its function-scoped and can cause confusion. The declaration in line 5 makes it seem like result should only be accessible in the if statement, but because it uses var, it still exists after the block. We should instead use something like const or let.
4. Line 9 will print "values added: 20"
5. The code errors, as result is not defined because let means it is block scoped. The result variable exists only in the if block. 
6. The code errors, as assignment to constant variable is illegal and occurs in line 7.
7. The code errors, as result is not defined because const means it is block scoped. The result variable exists only in the if block.