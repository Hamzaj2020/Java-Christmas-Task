# Java-Christmas-Task
Engineering 50 Java Christmas Tasks

Intellij and Java 13

**Methodology**

Read through the code to find out what needs to be corrected for each problem. After every change, I've retested the code and noted the differences. The aim of the task was to test if the FizzBuzz Code works according to specification.

**Testing**

1)

divisibleBy(4,2) should return true (i.e. 4 is taken to be divisible by 2)
Result before changes: false
Result after change : true
Problems found: Does not return true
2)

divisibleBy(3,2) should return false (i.e. 3 is taken to NOT be divisible by 2)
Result before changes: false
3)

This tests whether the actual returned values are between 1 and 15. fizzBuzzGenerator(1,15) should return ["1", "2", "Fizz", "4", "Buzz", "Fizz", "7", "8", "Fizz", "buzz", "11", "Fizz", "13", "14", "FizzBuzz"]

*problems found*:
spelling mistake in the 9th element "buzz". This should be "Buzz"
Only 14 returned values instead of 15
Incorrect Spelling "Buz". This should be "Buzz"

**Changes**

1.) Change At: FizzBuzzGenerator > divisibleBy() return numerator % Denominator == 2; to return numerator % Denominator == 0;

Reason: solves initial problem of not returning true and incorrect triggering of FizzBuzz word

2.) Change At: FizzBuzzGenerator > FizzBuzz() for (int i = startNumber; i <endNumber ; i++) { to for (int i = startNumber; i <= endNumber ; i++) {

Reason: Returns expected 15 values

3.) Changed logical operator At: FizzBuzzGenerator > FizzBuzz() if(divisibleBy(i, 3) || divisibleBy(i, 5)) fizzBuzzList.add("FizzBuzz"); to if(divisibleBy(i, 3) && divisibleBy(i, 5)) fizzBuzzList.add("FizzBuzz");

Reason: ensures that the actual value returned was "FizzBuzz" instead of "Fizz".

4.) Changed: At FizzBuzzGenerator > FizzBuzz() else if (divisibleBy(i, 5)) fizzBuzzList.add("Buz"); to else if (divisibleBy(i, 5)) fizzBuzzList.add("Buzz");

Reason: corrects the spelling mistake of "Buz". This should be "Buzz"
