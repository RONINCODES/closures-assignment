E1)
var lastWord = 'welcome';
console.log(lastWord);
lastWord = 'goodbye';

console.log(lastWord) - prints out 'welcome' because it is defined above the console.log.

E2)
var message = "Up here!";

function shout() {
  console.log(message);
}

shout();

console.log(message) did print out 'Up Here', because the local variable 'message', was defined above the function 'shout'.


E3)
var muffins = 'two dozen';
var purchasedMuffins;

function getMuffins() {
  return muffins;
}
purchasedMuffins = getMuffins();
console.log(purchasedMuffins);

--returns two dozen - because var muffins was defined above the function getMuffins(). And so can be used anywhere in the program.


E4)
var chore = 'laundry';

function doChores() {
  var chore = 'sneak out';

  function reportActivity() {
    console.log(chore);
  }

  reportActivity();
}

doChores(); // calling doChores(), which then calls reportActivity()


-- returns 'sneak out'
because doChores() and reportActivity() both rely on the local variable of var chore that was set within the function doChores.

E5)
var letter;
var contents = 'Looking for gold';

function getMail() {

  function changeContents() {
    var contents = 'Struck it rich!';
  }

  changeContents();
  return contents;
}

letter = getMail();
console.log(letter);


--> returns 'looking for gold - not sure why??


E6)

var decision;

function firstIdea() {
  var decision = 'Buy a new car';
  return decision;
}

function secondIdea() {
  console.log(decision);
}

firstIdea();
secondIdea();

--> returns undefined not sure why?


BLOCKS
E1)

##### added the line below to make function print out the address..
var address = '123 Happy St.'
function buildHouse(address) {

  return 'Building house at ' + address;
}
buildHouse('123 Happy St.');
console.log(address);
