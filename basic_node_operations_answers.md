>**1. Run the commands sort, wc and uniq on the commands.js file. Explain how they work and what the output was.**  

`sort` takes a filename and sorts each line alphabetically.

```
done(data);
if (err) throw err;
});
const fileName = fullPath[0];
done(userInput);
fs.readFile(fileName, (err, data) => {
break;
break;
commandLibrary.cat(userInputArray.slice(1));
commandLibrary.echo(userInputArray.slice(1).join(" "));
//we will add the functionality of echo next within the object commandLibrary
case "cat":
case "echo":
process.stdout.write('\nprompt> ');
process.stdout.write(output);
"echo": function(userInput) {
//the cat command
}
},
"cat": function(fullPath) {
//the echo command
}
const command = userInputArray[0];
const userInputArray = userInput.split(" ");
switch (command) {
//parses the user input to understand which command was typed





//where we will store our commands
//where we will store the logic of our commands
//write out data
}
}
};
const commandLibrary = {
const fs = require("fs");
function done(output) {
function evaluateCmd(userInput) {
module.exports.commandLibrary = commandLibrary;
module.exports.evaluateCmd = evaluateCmd;
```

`wc` (wordcount) takes a filename and prints out the new lines, number of words and number of bytes.  
`43  118 1143 commands.js`

`uniq` (unique) takes a filename and filters out adjacent duplicate lines.
```
const fs = require("fs");

//write out data
function done(output) {
    process.stdout.write(output);
    process.stdout.write('\nprompt> ');
}

//where we will store our commands
function evaluateCmd(userInput) {
 //parses the user input to understand which command was typed
  const userInputArray = userInput.split(" ");
  const command = userInputArray[0];

  switch (command) {
    case "echo":
     //we will add the functionality of echo next within the object commandLibrary
      commandLibrary.echo(userInputArray.slice(1).join(" "));
      break;
    case "cat":
      commandLibrary.cat(userInputArray.slice(1));
      break;
  }
}

//where we will store the logic of our commands
const commandLibrary = {
  //the echo command
   "echo": function(userInput) {
       done(userInput);
   },
   //the cat command
  "cat": function(fullPath) {   
       const fileName = fullPath[0];
       fs.readFile(fileName, (err, data) => {
           if (err) throw err;
           done(data);
       });
   }
};

module.exports.commandLibrary = commandLibrary;
module.exports.evaluateCmd = evaluateCmd;
```
>**2. Using the pipe (|) connect at least two commands and run it on commands.js. Explain what the output was and why the specific data was outputted.**  
Here `sort` and `wc` have been used on `commands.js`. This first sorts the lines in `commands.js` and then prints out the number of newline, word, and byte counts for the file.
```
$ sort commands.js | wc
     43     118    1143
```


>**6. In this checkpoint, you encountered built-in JavaScript methods as well as the new ES6 syntax. Review the information below before attempting the programming challenge.**  
```
function reverseString(inputString) {
   //solve problem
   let wordArray = inputString.split(" ");
   let resultArray = [];
   wordArray.forEach((word) => {
     resultArray.push(word.split('').reverse().join(''));
   })
   return resultArray.join(" ");
}
```
