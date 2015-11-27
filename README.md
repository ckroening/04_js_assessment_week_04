# js_assessment_week_04

In this assessment, you will be working with functions and how the are processed in a chronological fashion. Navigate to the files below. There you will find a series of statements. Your task is, at the two points indicated, email me what the expressions would evaluate to (had we assigned it or logged it for example).

PLEASE try to work this out on paper BEFORE bringing the code into an editor yourself. I am more interested in you working through the challenge and potentially being wrong, than just getting email the right answer.

http://goo.gl/Ay9sR7


var theNumber = 1;

var michelangelo = function(value){
value = (value * 2);
return value;
}

var donatello = function(value, anotherValue){
value = anotherValue + value;
anotherValue = value * anotherValue;
return anotherValue;
}

var leonardo = function(value){
var anotherValue = value;
value *= 4;
theNumber = value / 2;
return (value + anotherValue);
}

var raphael = function(value, anotherValue, yetAnotherValue){
value = value * anotherValue + yetAnotherValue;
return yetAnotherValue;
}

//In your email, tell me what the answer to this expression would be:
michelangelo(theNumber) + leonardo(theNumber);

theNumber = theNumber * 2;

//In your email, tell me what the answer to this expression would be:
(donatello(theNumber, 2)) - (raphael(3, 2, theNumber));