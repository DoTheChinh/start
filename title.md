# HTML + Javascript Exercise

### Knowledge round-up

- **Javascript**

	- What are the differences between a variable that is: `null`, `undefined`?
		+ a variable return null when this variable is declared or defined 
		+ a valiable return underfined when this variable is not declared and defined
	- What is `use strict`? what are the advantages and disadvantages to using it?
			+advantages : 
				-It catches some common coding bloopers, throwing exceptions. 
				-It prevents, or throws errors, when relatively “unsafe” actions are taken (such as gaining access to the global object). 
				-It disables features that are confusing or poorly thought out. 
			+disadvantages : 
				-It will not allow us to use the “with” statement. This statement will causes security and performance problems. 
				-It will not allow us to use the “arguments.caller” property, due to security concernsWe do not have an alternate to this property, but we can hard code an additional parameter.
	- What are the differences between `==` and `===`? Write an example for each case (if any)?
			+ use "==" when if want to compare with 2 variable is the same value
			+ use "===" when if want to compare with 2 variable is the same both value and type of variable
	- What is different between declaration: `var`, `const` and `let`?
			+var : is now the weakest signal available when you define a variable in JavaScript. The variable may or may not be reassigned, and the variable may or may not be used for an entire function, or just for the purpose of a block or loop. 
			+const :is a signal that the identifier won’t be reassigned. 
			+let : is a signal that the variable may be reassigned, such as a counter in a loop, or a value swap in an algorithm. It also signals that the variable will be used only in the block it’s defined in, which is not always the entire containing function.

### Playground
1. Write a JavaScript program to compute the sum of the two given integers. If the two values are same, then returns triple their sum.
```
Input: a = 5, b = 10
Output: 15

Input: a = 5, b = 5
Output: 30

Code :
	function total( a, b ) {
		if ( a === b ) return a + b;
		else return 3 * ( a + b );
	}
	document.write(total(a, b));
```

2. Write a JavaScript program to compute the absolute difference between a specified number and 19. Returns triple their absolute difference if the specified number is greater than 19.

```
Input: a = 12
Output: 7

Input: a = 19
Output: 0

Input: a = 22
Output: 9

Code : function greater_number(a) {
				let num = 19;
				if( a < num ) return num - a;
				else if( a == num ) return 0;
				else retunr 3 * ( num - a );
			}
			document.write(greater_number(a));
```

3. A masked number is a string that consists of digits and one asterisk (*) that should be replaced by exactly one digit. Given a masked number find all the possible options to replace the asterisk with a digit to produce an integer divisible by 3.

```
Input: a = '1*9'
Output: ['129', '159', '189']

Code : 	funtion number_divisible_by_n(number, n) {
					let result = [];
					let num = 0;
					for( let i = 0; i < 10; i++) {
						num = a.repalce("*", i);
						if ( num % n == 0 ) {
							result.push = num;
						}					
					}
						return result;
					}
				console.log(number_divisible_by_n(number, 3));

```


4. A masked number is a string that consists of digits and one asterisk (*) that should be replaced by exactly one digit. Given a masked number find all the possible options to replace the asterisk with a digit to produce an integer divisible by 6.

```
Input: a = '1*9'
Output: []
```

```
Input: a = '1234567890*'
Output: ['12345678900', 
 '12345678906']

Code: 
				console.log(number_divisible_by_n(number, 6));
```