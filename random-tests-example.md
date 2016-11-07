## Random Tests - Codewars - A Full Example

In the following snippet, you can see how you can add a random test for your Kata. Assuming the user solution to your Kata is as followed:

```
function sumUser(a,b) {
    return a+b;
}
```

Then you would add the following code block under "Test Cases":

```
// Your predefined solution: 
function sumKataAuthor(a,b) {
    return a+b;
}


// A function generating a random number in a range between min and max:
function getRandomNumber(min, max) {
  return Math.floor(Math.random() * (max + 1 - min) + min);
}


// Run test 10 times (or as many times as you like!):
for (var i = 0; i < 10; i++) {

  // Generate random input numbers between 0 and 100 for each test: 
  var a = getRandomNumber(0, 100);
  var b = getRandomNumber(0, 100);
  
  // Adding console.log of the inputs used in the test may help
  // the user understand and debug their solution: 
  console.log('input a was:', a, 'input b was:', b);
  
  // Compare user's function with a working solution:
  Test.assertEquals(sumUser(a, b), sumKataAuthor(a, b));
}
```
