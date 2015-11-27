# js_assessment_week_04

In this assessment, you will be working with functions and how the are processed in a chronological fashion. Navigate to the files below. There you will find a series of statements. Your task is, at the two points indicated, email me what the expressions would evaluate to (had we assigned it or logged it for example).

PLEASE try to work this out on paper BEFORE bringing the code into an editor yourself. I am more interested in you working through the challenge and potentially being wrong, than just getting email the right answer.

http://goo.gl/Ay9sR7

codestack:
-------------------

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

answer
-----------------------------------
1. variable theNumber defined: 1.
2. four functions defined: mich, dona, leo, raph.

3. figure out: michelango(theNumber) + leonardo(theNumber); 
    (use functions from code stack)
    michelangelo = function(1) { value = 1 * 2 = 2; return 2; } = 2.
    leonardo = function(1) { anotherValue = 1; value = 4 * 1 = 4; theNumber = 4/2 = 2; return (4 + 1 = 5); } = 5.
        (theNumber is a global variable so its value initially remains 1 even though it was changed locally in the first function.)
        (theNumber is explicitly called in this function so its global value does NOW change since it is not passed only as an argument parameter for value.)
        (theNumber is now globally RESET to 2 from within a local calling of it in leo fxn.)
   
    michelangelo + leonardo = 2 + 5 = 7.

4. additional adjustment to theNumber: theNumber = theNumber * 2 = 2 * 2 = 4. Once again globally RESET.

5. figure out (donatello (theNumber, 2)) - (raphael(3, 2, theNumber));
    (use functions from code stack)
    donatello = function(4, 2) { value = 2 + 4 = 6; anotherValue = 6 * 2 = 12; return 12; } = 12.
    raphael = function(3, 2, 4) { value = 3 * 2 + 4 = 10; return 4; } = 4.

    donatello - raphael = 12 - 4 = 8.


