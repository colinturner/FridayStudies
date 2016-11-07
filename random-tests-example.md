## Random Tests - Codewars - A Full Example

```
// Codewar's user solution
function sumUser(a,b) {
    return a+b;
}


// Your predefined solution
function sumKataAuthor(a,b) {
    return a+b;
}


// A function generating a random number in a range between min and max
function getRandomNumber(min, max) {
  return Math.floor(Math.random() * (max + 1 - min) + min);
}


// Run test 10 times
for (var i = 0; i < 10; i++) {

  // Generate random numbers between 0 and 100 for the tests
  var a = getRandomNumber(0, 100);
  var b = getRandomNumber(0, 100);
  
  // Show the numbers to the user so that it is easier
  //  for them to debug their solution
  console.log('input a was:', a, 'input b was:', b);
  
  // Compare user's function with a working solution
  Test.assertEquals(sumUser(a, b), sumKataAuthor(a, b));
}
```
