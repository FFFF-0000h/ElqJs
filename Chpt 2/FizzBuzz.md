Write a program that uses console.log to print all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, print "`Fizz`" instead of the number, and for numbers divisible by 5 (and not 3), print "`Buzz`" instead. When you have that working, modify your program to print "`FizzBuzz`" for numbers that are divisible by both 3 and 5 (and still print "`Fizz`" or "`Buzz`" for numbers divisible by only one of those). (This is actually an interview question that has been claimed to weed out a significant percentage of programmer candidates. So if you solved it, your labor market value just went up.)

```javascript
for (let n = 1; n <= 100; n++) {
  if (n%3 == 0 && n%5 == 0) {
 	console.log("FizzBuzz");
  } else if (n%3 == 0) {
 	console.log("Fizz");
  } else if (n%5 == 0) {
 	console.log("Buzz");
  } else {
 	console.log(n);
  } 
}
```

Another way to solve this?

```javascript
for (let i = 1; i < 100; i++) {
	let buzzer = ""
	if (i%3 == 0) {
		buzzer += "Fizz"
	}
	if (i%5 == 0) {
		buzzer += "Buzz"
	}
		console.log(buzzer || i);
}
```