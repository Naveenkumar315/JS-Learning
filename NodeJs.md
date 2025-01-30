1. what is node js?
    node js is a js runtime environment for executing js code.

2. how node js a runtime environment on serer side? what is v8?
    inside chrome browser v8 is there for to run js code on client side.

3. what is the difference between Runtime environment & Framework?
    Runtime environment: Primarily focuses on providing he necessary infrastructure for code execution, including services like memory management and i/o operations.

    Framework: Primarily focuses on simplifying the development process by offering a structured set of tools, libraries, and best practices.

4. what is the difference between nodejs & Express js.
    Node js is a runtime environment that allows the execution of javascript code server-side

    Express js is a framework built on the top Node js.
        It is designed to simplify the process of building web applications and APIs by providing a set of features like simple routing system, middleware support etc.

5. difference between js and node js(client and server)
    js runs on client side browser, it has html, css & js.
    we can access the dom element by using js through browser.
    handles UI display, interactions, and client-side logic.

    node js runs on server side, can't access the dom element, we can use only from server side. handles data storage/access, authentication, authorization, req and res.

6. what are the 7 Main Features of Node.js?
    1. single Threaded
    2. Asynchronous
    3. Event-Driven
    4. V8 Javascript Engine
    5. Cross-Platform
    6. Npm-Node Package Manager
    7. Real-Time Capabilities

7. What is Single Threaded Programming?
    single thread will wait for to complete one task before it execution.
    task1 -> task2 -> task3 - hear task 2 will wait for until the task1 completed.

8. What is Synchronous Programming?
    In a synchronous program, each task is performed one after the other, and the program waits for each operation to complete before moving on to the next one.

    task1 -> task2 -> task3 - hear task 2 will wait for until the task1 completed.

    disadvantage - its a blocker, and it will take more time.

9. what is Multi Threaded Programming?

10. What is Asynchronous Programming?
    In Node js asynchronous flow can be achieved by its single-threaded, non-blocking, and event-driven architecture.

    In Node js if there are 4 task(t1,t2,t3,t4) to be completed for an event. Then below steps will be executed.

    First, Thread T1 will be created.

    Thread T1 initiates Task1, but it won't wait for Task1 to complete. Instead, T1 proceeds to initiate Task2, then Task3 and Task4(This asynchronous execution allows T1 to efficiently handle multiple tasks concurrently).

    whenever Task1 completes, an event is emitted.

    Thread T1, being event-driven, promptly responds to this event interrupting its current task and delivering the result of Task1.

11. difference between synchronous & asynchronous programming?
    synchronous
    1. In synchronous programming, task are executed one after another in a sequential manner.

    synchronous
    In asynchronous programming, task can start, run, and complete in parallel.

    synchronous
    2. Each task must complete before the program moves on to the next task.

    asynchronous
    Tasks can be executed independently of each other.

    synchronous
    3. Execution of code is blocked until a task is finished.

    asynchronous
    Asynchronous operations are typically non-blocking.

    synchronous
    4. Synchronous operations can lead to blocking and unresponsiveness.

    asynchronous
    it enables better concurrency and responsiveness.

12. What are Event, Event Emitter, Event Queue, Event Loop & Event Driven?
    Event: Signals that somethings has happened in a program.

    Event Emitter: Create or emit events. It allows creating and handling custom events.
    <!-- 
        const EventEmitter = require('events');

        class MyEmitter extends EventEmitter {}

        const myEmitter = new MyEmitter();

        // Register an event
        myEmitter.on('data_received', (data) => {
            console.log(`Data received: ${data}`);
        });

        // Emit event with data
        myEmitter.emit('data_received', 'Hello World');

        EventEmitter is used to register and emit events dynamically.
        The .on() method listens for an event.
         The .emit() method triggers an event.
     -->

    Event Queue: Events emitted queued(stored) in event queue.

    Event Handler(Event Listener): Function that responds to specific events

    Event Loop: The event loop picks up event from the event queue and executes them in the order they were added.

    Event
        A signal that something has happened
        'greet' event emitted in the first example
    EventEmitter
        A class for handling and emitting events
        myEmitter.on('event', callback)
    Event Queue	
        Stores events waiting to be processed
        setTimeout(() => {...}, 1000); adds event to queue
    Event Loop
        Continuously checks and executes events from the queue
        console.log() executes first, while async tasks wait
    Event-Driven
        Execution happens based on events, not sequentially
        server.on('request', callback)
