# Quiz-KNow-Me

//how much you know about me
var read = require("readline-sync");
var name = read.question("What is your name:");
var score = 0
var right=0
var wrong=0
// welcoming user
console.log("Hello " + name);
console.log("========");
console.log("Let's see how much you know about Ayush ;)");
//info about game
console.log("Note:-Each question is of 2 points :)");
console.log("========");
//creating function
function quiz(q, a) {
  var answer = read.question(q);
  if (answer.toLowerCase() === a.toLowerCase()) {
    score = score + 2
    right=right+1
  } else {
    score = score;
    wrong=wrong+1 
  }
}
//creating array of questions and answers
var ques = [
  "1. What is my favorite color?","Black",
  "2. What does I like most(Sweet/Spicy)?","Spicy",
  "3. Favorite Dish?","Chicken",
  "4. Favorite actor?","Hrithik", 
  "5. Favorite Singer?","Darshan",
]
//using for loop to access questions 
for (var i = 0; i<ques.length; i=i+2) {
  var qu=i
  var an=i+1
  quiz(ques[qu],ques[an])
}
//giving results
console.log("========");
console.log("You gave ",right," right answers.");
console.log("You gave ",wrong," wrong answers.");
console.log("Your final score is: ", score)
