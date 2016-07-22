# Paralell/Concurrency Programming

# 1. Callback Pattern [^2]

Callback functions are derived from a programming paradigm known as functional programming. At a fundamental level, functional programming specifies the use of functions as arguments. Functional programming was—and still is, though to a much lesser extent today—seen as an esoteric technique of specially trained, master programmers.

Fortunately, the techniques of functional programming have been elucidated so that mere mortals like you and me can understand and use them with ease. One of the chief techniques in functional programming happens to be callback functions. As you will read shortly, implementing callback functions is as easy as passing regular variables as arguments. This technique is so simple that I wonder why it is mostly covered in advanced JavaScript topics.

[code lang="javascript"]
function getN(){
    return 10;
}

var n = getN();

function getAsyncN(callback){
    setTimeout(function(){
        callback(10);
    }, 1000);
}

function afterGetAsyncN(result){
    var n = 10;
    console.log(n);
}

getAsyncN(afterGetAsyncN);
[/code]

# 2. Promise Pattern [^1] [^3]

### What is a promise?

The core idea behind promises is that `a promise` represents `the result of an asynchronous operation`.

A promise is in one of three different states:

* pending - The initial state of a promise.
* fulfilled - The state of a promise representing a successful operation.
* rejected - The state of a promise representing a failed operation.

Once a promise is fulfilled or rejected, it is immutable (i.e. it can never change again).

[code lang="javascript"]
function aPromise(message){
    return new Promise(function(fulfill, reject){
        if(message == "success"){
            fulfill("it is a success Promise");
        }
        if(message == "fail"){
            reject("it is a fail Promise");
        }
    });
}
[/code]

Usage:

[code lang="javascript"]
aPromise("success").then(function(successMessage){
  console.log(successMessage)
}, function(failMessage){
  console.log(failMessage)
})
// it is a success Promise
[/code]

[code lang="javascript"]
aPromise("fail").then(function(successMessage){
  console.log(successMessage)
}, function(failMessage){
  console.log(failMessage)
})
// it is a fail Promise
[/code]

[^1]: Promise Paterns: [https://www.promisejs.org/patterns/](https://www.promisejs.org/patterns/)
[^2]: [Understand JavaScript Callback Functions and Use Them](http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/)
[^3]: [Promise, Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

