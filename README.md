# INTERVIEWS
Code, IDEs, Tools utilized during interviews.

* Everything here is related to the JavaScript stack, if a tool, concept, or anything is more related to other language it will be specified in parenthesis.
* **(Recommended)** means either is widely used (top 3), or widely used by almost everyone.
* **(= or == or ===)** means actuallys means or equals.
* widely used means exactly that

# 1 - IDE
Basically if the problem is:
* JavaScript they use JSFiddle.net
* React or Angular they use CodeSandBox.io
* Visual Studio Code is used for all of them too.

| Language | JSFiddle.net | Plnkr.co | codesandbox.io |
| --- | --- | --- | --- |
| JavaScript | Yes | Yes | Yes |
| React | No | ? | Yes |
| Angular | No | ? | Yes |

## 1.1 JSFiddle.net
* Add libraries with `Resources > cdnjs` for jQuery, and others.
* Result has a Console (Beta) for `console.log()`

## 1.2 CodeSandBox.io
* Angular Template: https://codesandbox.io/s/angular
* React Template: https://codesandbox.io/s/react-new

# 2 - HTML/ CSS / JAVASCRIPT
## 2.1 HTML
## 2.2 CSS
CSS pre-processors
* SASS (Recommended)
* LESS
## 2.3 JavaScript
```javascript

// What values will boo and bar have at the end?

const ar1 = [7,15,10,2,8,1,7,0];
const ar2 =[0,0,0];

const foo = [...ar1]
    .filter((a) => a % 2 ===1)
    .sort()
    .slice(0,2)
    .map((a) => a + 5)
    .some((a) => a > 15);

const bar = ar1.concat(ar2) === [...ar1, ...ar2] ||
        ar1.reduce((a,b) => a * b, 1) === ar2.reduce((a,b) => a+b,1);

console.log(foo);   // true
console.log(bar);   // false

```

# 3 - NODEJS

# 4 - REACT

```javascript
// Make a Textarea for the results, and 2 buttons (Previous and Next).
// Everytime user press Next or Previous there is a REST call to endpoint:
// http://jsonplaceholder.typicode.com/posts/1
// Where 1 == User ID.
// When Next User ID = 2, and REST must reflect that http://..etc..../posts/2
// The Endpoint answer with User info in JSON.
// Show the User info in TextArea.
// Previous must go previous
```
# 5 - ANGULAR

# 6 - ENDPOINTS / JSON / API

## 6.1 jsonplaceholder.typicode.com
Fake REST API that returns request of type GET/POST for testing.
* GET URL example: `http://jsonplaceholder.typicode.com/posts/1` where `1`== userId will return JSON with some user information.

## 6.2 Swagger
* Makes easier generate APIs to connect Angular and Java EE

# 7 - TESTING
## 7.1 Jasmine (Recommended)
* Default testing framework in Angular
* Behavior Driven Development (BDD) testing framework.
* Human readable easy syntax.
* It doesn't require a DOM
* It doesn't depend on other JS frameworks.

## 7.2 Mocha
* Widely used.
* It runs on Node.js and the Browser
* Easy asynchronous testing.

## 7.3 Karma (Recommended)
* Default testing tool in Angular
* Framework agnostic, it can work with Jasmine
* Easy integration with Jenkins/Travis/CI pipeline

## 7.4 Jest (from Interviewer)

## 7.5 Protractor (from Interviewer)

## 7.6 Siesta
* Unit and UI testing tool.
* Test Node.js processes and web pages.
* Capable of running in headless environment with Puppeteer and headless Webdriver.
  * Puppetter is a Node.js library to control headless Chrome for testing, and related stuff.
  * Headless WebDriver: Like Selenium WebDriver uses Browser's headless mode (launch browser without GUI/Invisible Window) to run tests faster with fewer resources.

## 7.7 Others
* Sentry.io Helps monitoring/fix crashes on real time


# 8 - BUILD & OTHERS

## Coding Flow

* (A): Angular/React/Vanilla JS/NodeJS Code

```
(A) --> Webpack(Live Watch)/Linting --> Testing --> Gulp (Live Watch, generate Prod/Dev distr folders)
```

## 8.1 Bundlers & Others
### 8.1.1 Webpack
* Widely used for front-end
* It's a bundler for all (html/js/css, even assets)
* It can uglify

### 8.1.2 Babel
* Widely used in back-end
* Trannslates new JS Syntax to ES6/7

## 8.2 LINTERS
Makes coding follow rules (spelling, naming, space/tabs, etc) for:
* Formatting and Style
* Coding standards and conventions

### 8.2.1 ESLint (Recommended)

### 8.2.2 JSLint
### 8.2.3 JSHint

## 8.3 Build 
## 8.3.1 Gulp (Recommended)
* Read files as streams and pipes them out to different tasks (modify files, build files, uglify, webpack, Mocha test, automate release)
* Gulp tasks are written in a `gulpfile.js`
```javascript
var gulp = require('gulp'); // Required
// Include plugins
var pluginA = require('pluginA');
var pluginB = require('pluginB');
// Define tasks
gulp.task('task-A', function() {
  gulp.src('some-source-files') // Input Files
  .pipe(pluginA())  // Apply plugins
  .pipe(pluginB())
  .pipe(gulp.dest('some-destination')); // Output files
});
```

## 8.3.2 Grunt
* It's still used widely and competes with Gulp
* It's based on configuration files.

## 8.3.3 Broccoli (JS)
* Was widely used in the past, but not too much anymore.
* Connects inputs to outputs.


# 9 - BENCHMARKING
There are tools to measure how fast or how much storage algorithms perform.Most of them use `benchmark.js` as library.
* Benchmark.js (Recommended) to use it locally: https://benchmarkjs.com/
* JSPerf (often down)
* JSBench.me
* MeasureThat.net
* JSFiddle template ready to go: https://jsfiddle.net/533hc71h/
* JSFIddle template improved: https://jsfiddle.net/2e8fcuhb/2/
* Plunker template: https://plnkr.co/edit/pJg5LsiSNqlc6immmGsW?preview

# 10 - ALGORITHMS
**Big-Oh Notation**
Gives worst-case scenario of an algorithm complexity in terms of `Time` or `Space`.
| Big-Oh | Complexity | Description |
| --- | --- | --- |
| O(1) | Constant | Fastest or Best |
| O(log n) | Logarithmic | Proportional to input size in terms of log |
| O(n) | Linear | Proportional to input size |
| O(n log n) | Log-Linear / QuasiLinear | Proportional to input size and a logarithmic factor |
| O(n^2) | Square / Polinomial | Bad, Proportional to square, cubic, polinomial |
| O(2^n) | Exponential | |
| O(n!) | Factorial | Worst of the Worst| 

* `Time` Complexity: Number of operations performed by algorithm in big-Oh notation. Less number of operations == most efficien.
* `Space` Complexity: Storage needed by an algorithm in big-Oh notation. 

![](img/big-oh.png)

## Fibonacci
Given a number N return the index value of the Fibonacci sequence, where the sequence is `[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...]`


```javascript
    // Solution 1 - While
    // Time Complexity = O(n) OK
    // Space Complexity = O(1)
function fibonacci_1(num) {
    var a = 1, b = 0, temp;
    while (num >= 0) {
        temp = a;
        a = a + b;
        b = temp;
        num--;
    }
  return b;
}
    // Solution 2 - Recursive
    // Time Complexity = O(2^N) REALLY BAD
    // Space Complexity = O(n)
function fibonacci(num) {
    if (num <= 1)
        return 1;
    return fibonacci(num - 1) + fibonacci(num - 2);
}

    // Solution 3 - Hash / Memoization
    // Time Complexity = O(n) OK
    // Space Complexity = O(n)
function fibonacci(num, memo) {
    memo = memo || {};

    if (memo[num]) return memo[num];
    if (num <= 1) return 1;

    return memo[num] = fibonacci(num - 1, memo) + fibonacci(num - 2, memo);    

```

* https://medium.com/developers-writing/fibonacci-sequence-algorithm-in-javascript-b253dc7e320e
