---
layout: post
title:  "Lets talk about testing"
date:   2017-09-07 12:31:01 +0300
---

Today i would like to talk about testing. 
I always find posts about "unit testing", "integration testing" etc. In this post I will try to avoid such terms and i will focus on what exactly a test is and why we need a test suite.

First of all we need to understand what a test is. A test is nothing more than a procedure that checks if something works as expected.
Let's see an example.
If we want to test if the fridge works fine, we can put a thermometer in it and we check if the temperature is the expected.

Again, a test is a process to check if something works as expected.
The result of a tests should be 'success' or 'failure', nothing more, nothing less. Let's call a successful test GREEN and a failed test RED.


In programming, the testing procedure is exactly the same with the procedure that has been described in the previous paragraph. The fridge is the piece of code that we want to test (a function, a class, an HTML page etc), lets call it 'System Under Test or SUT', the thermometer is the input to the SUT and the temperature is the output of the SUT. 
Let's see some examples

* we created the following class
  class Person
  	attr_accessor :first_name
  end

and we want to test that the assignment of the first_name attribute of a Person instance works as expected. What we can do is to open a console, create a new object, set the first_name and read the first_name attribute. If we compare this example with the example with the fridge, we will see that the setter of the first_name is the fridge, the assignment action is the thermometer and the value of the first_name attribute is the temperature.

* We created an HTML/Javascript page where there is a button that when is clicked changes its color. 
In this case we can test the functionality of the button by loading the HTML page in a browser, clicking the button and checking its color. If the color is not changed the test is RED, if the color is changed the test is GREEN.


The previous test scerarios were performed manually. 

Now let's suppose that we have an application with many features and thousands of lines of code and we make a change in a core module of our code base, then we need to run all the scenarios by hand. This costs time but the most important is that this kind of testing is error prone, maybe we will not check a result extensivelly or maybe we will forget to run a scenario.

What if we could write code that executes our scenarios and prints the result of each test? Pretty cool, right?
We can make changes in our code, run our automated test suite and review the test results to check if the application works as expected. 

Using automated tests we can significally improve our productivity, make our lives easier and painless but the most important is that an automated test suite could save much time that can be used to brew our favorite beer. :)