# Exam Part 4 – Testing

<!--====================  START: Insert your Student ID  =================  -->
> Student ID: UP937317
<!--====================  END:   Insert your Student ID  =================  -->

Testing is paramount to building a robust software project. Recommend a testing
strategy for SCRAMBLES Ltd.

a) Provide an overview of the testing strategy.

b) Recommend tooling to assist with the testing.

c) Provide a testing example for a particular function or feature.

***[15 Marks]***

<!--===============  START:   Edit the Markdown below here  ==============  -->

a)

As our code base will grow we will first be doing unit testing on each class/method we consider crutial. After these tests will pass we will move to Component testing. Each of our individual features in the system will be tester separately. After features are acccpeted we will test the whole system and its characteristics.

b)

As the whole system will be written in python(micro python to be specific) we will be using testing frameworks that were made specificaly for our selected language.
We will be using framework hyphothesis for our python Unit tests:
<https://hypothesis.readthedocs.io/en/latest/>

For our SQL queries unit tests we will be using framework tSQLt:
<https://tsqlt.org/>

For our mobile application written in Java  we will be using testing framework junit:
<https://junit.org/junit4/>

c)

given method for checking the light level frim the Light sensor for automatic closing and opening of the door. (pseudo code)

def chechLightLeve(int level)
    if leve > 6 and level < 26
        openDoor()
    else
        doNothing()

This function takes parameter as light leven (integer) and we have to test several inputs for this function. Arounf boundaries, then in each particiton and some cases then would couse error (these need to be hadled)

| input | expected result |
| ----- | --------------- |
|3|doNothing|
|20|openDoor|
|45|doNothing|
|5|doNothing|
|6|openDoor|
|7|openDoor|
|25|openDoor|
|26|openDoor|
|27|doNothing|
|-2|doNothing|
|string "hello"|doNothing|
|3.5|doNothing|
||doNothing|

All of these cases have to be sanitized in our function after the unit tests.

<!--===============  END:   Edit the Markdown above here  ================  -->