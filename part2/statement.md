Asynchronous execution is not just an obscure JavaScript magicians concept. We need it for a good reason. Take the following example. Click on the "Run my code" button to start the demo.

Both buttons do the same job: an http request is done to get a distant file and then print it. The request is very slow on purpose (the server will wait 5 seconds to respond).

One button executes synchronous code and the other button executes asynchronous code. As you can see, when you click on the first button, the user interface just freezes during the code execution. This is because the main thread can't execute the code and refresh the user interface at the same time. When you click on the second button, the main thread finishes its job with the user interface and then the code is executed.

@[Why we need asynchronous]({"layout": "aside", "stubs": ["code.html"], "command": "node server.js", "project":"part2"})

The given example uses [jQuery](http://jquery.com/) to perform the http request.

In the future, synchronous http requests will be not supported anymore by browsers. Dealing with asynchronous execution is just a must have in the JavaScript world.
