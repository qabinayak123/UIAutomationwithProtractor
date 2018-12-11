# UIAutomationwithProtractor
Protracttor
--------------
Setup
------
1.1JavaPath(System Variable)
1.2Download and install Nodejs
1.3node -v
1.4npm -v
1.5webdriver-manager update
1.6webdriver-manager start
Jasmine
-------
Describe-Test Suite
it-Test Case
Spec-In Jasmine we called as test file.(TestFile) in Java called (Class File).
Every spec should have Describe and it blocks.
These 2 are mandatoryfor writing Test cases in javascript.
Configuration File-For running Test cases(Specfile).
In one Describe we can write multiple "it".
ctrl+space for auto suggestion
Promises
---------
Javascript is Asynchronus language(means non sequential any step may be executed,Webdriverjs and protractor also asynchronus)
www.sohamkamani.com
www.spin.atomicobject.com
www.bridge360blog.com
Every javascript returns promise
promise resembles state of your step
3 state
1.pending,2.resolved,3.Rejected 
Synchronus:You will move to next step only after promise for current step is either resolved or rejected(Java/Python)
Asynchronus:javascript moves to next step even if promise is pending.
90%(All the action we perform on the browser) of our protractor API will not move to next step until promise is resolved.
Note:If we want to perform any action on browser that supports by promise but if we want to retrive nything from browser-then that particular functionality related methods have not support of promise.
e.g-getTitle(),getText()
solution is using-then(function(){
                   })
JavaScript Basics
-----------------
printing in the console
-----
console.log("Hello World");
javascript DataTypes
--------
It is a dynamic type language,means we need not to specify type of the variable because it is dynamically used by JavaScript engine,you need to use var here to specify the data type.It can hold any type of values such as numbers,strings etc.
var a=4;
var b="Hello";
console.log(a);
console.log(b);
Javascript Conditional Statements
-------
if(){
console.log(executes if condition is true)
}else{
console.log(executes if condition is false)
}
if(){
console.log(executes if condition is true)
}else if{
console.log(executes else if condition is true)
}else{
console.log(executes if and else if conditions are false)
}
Javascript loops
-------
for(var i=1;i<100;i++){
}
While and do While Loop
--------
var j=1;
while(j<5)
{
console.log(j)
j++
}
var k=10;
do{
console.log(k);
k++;
}while(k<6)
Javascript Functions
--------
function add(a,b)
{
return a+b;
}
console.log(add(2,3));
Importance of Javascript ararys
------------
var a=4;
var b=["hello","world","4","goodbye"];
for(var i=0;i<b.length;i++)
{
console.log(b[i]);
}
var c=new Array();  [Empty array declaration]
Javascript String function
---------
var name="Rahul";   //String literal declaration
name.charAt(3);
name.concat("Shetty");
var name2=new String("Rahul");  //String object declaration
Importance of Object in javascript
------
Later
Ways of creating JavaScript Objects
------
Later
Understanding Global variables of Protarctor
--------------------------
Global variables in Protractor:
browser
element-interact with DOM element.requires on eparameter,locator strategy for locating the element.locator says protractor how to find DOM element.
most common locators are:
by.css,by.id,by.name,by.model,by.binding
some more about locators:
Function---------Description
---------------------------
addLocator---add a locator to this instance of ProtractorBy.
binding------Find an element by text binding
exactbinding-----find an element by exact binding
model-------find an element by ng-model expression.
buttonText-----find a button by text
partialButtonText-----Find a button by partial text
repeater-----Find elements inside ng-repeater
exactRepeater-----find an element by exact repeater
cssContainingText-----Find elements by CSS which contain a certain string.
options----find an element by ng-options expression
deepCss-----Find an element by css selector within the shadow DOM.
css:tagname[attribute='value']
Jasmine Assertions to validate Protracttor tests
-----------------------------
expect(element(by.css("locator")).getText()).toBe("8");
Jasmine takes care about promise resolve.
Running protractor tests on firefox and Internet Explorer
-----------------------------
capabilities:{
'browserName':'firefox'
}
bydefault IEdriver server will not be present we need to update it
webdriver-manager update --ie
even without starting selenium server we can run our test case by commenting selenium address in configuration.js
Running Protrcator tests on Non Angular Sites
----------------------------------------------
For angular application protractor will automatically wait for all the elements to load in the page.
we need to tell the protractor that our application is  jot angular.
browser.waitForAngularEnabled(fasle)
Importance of chain locators with example
-----------------------------------------
Whenever we see ng-repeat then we can use repeater locator.
resolving promises for multiple element we need to use each rather than then
taganame--locator
getAttribute--Retriving Values
