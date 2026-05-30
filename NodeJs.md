# What is Node_Js?

Node.js ek open-source, cross-platform JavaScript runtime environment hai jo server-side aur networking applications banane ke liye use hota hai. Iska use JavaScript ko browser ke bahar run karne ke liye kiya jata hai. Node.js ko Chrome ke V8 JavaScript engine par build kiya gaya hai, jo JavaScript ko fast aur efficient banata hai.

Node.js ka main benefit yeh hai ki yeh non-blocking, event-driven architecture use karta hai, jo high-performance applications ko handle karne mein madad karta hai. Iska matlab hai ki jab ek task (jaise file read karna ya database se data lana) chal raha hota hai, tab server doosre tasks ko bina rukke process kar sakta hai.

# Node.js key features:

#### Asynchronous and Event-Driven:
Node.js ka architecture event-driven hai, jo asynchronous programming ko support karta hai. Iska matlab hai ki Node.js non-blocking I/O operations ko handle kar sakta hai, jisme ek task dusre task ke complete hone ka wait kiye bina execute hota hai.

#### Single-Threaded: 
Node.js single-threaded model ko use karta hai, jisme ek hi thread mein multiple tasks perform hote hain. Yeh model high concurrency ko handle karne mein madad karta hai.

#### Fast Execution: 
Node.js, V8 JavaScript engine (jo Chrome mein use hota hai) ka use karta hai, jo JavaScript code ko machine code mein convert karke fast execution provide karta hai.

#### Non-blocking I/O: 
Node.js ka event loop non-blocking hota hai, jo disk, file system, network calls, etc., ko asynchronously process karta hai. Isse performance improve hoti hai, especially I/O-bound tasks mein.

#### NPM (Node Package Manager): 
Node.js ka ek major feature NPM hai, jo thousands of libraries aur packages provide karta hai. Developers in packages ko apne applications mein easily integrate kar sakte hain.

#### Cross-Platform: 
Node.js cross-platform hai, iska matlab hai ke aap Node.js applications ko Windows, macOS, aur Linux pe run kar sakte hain bina kisi additional configuration ke.

#### Scalable: 
Node.js ko horizontally scale karna bohot asaan hai. Aap multiple instances run kar sakte hain aur load balancers ka use karke application ki performance aur scalability ko improve kar sakte hain.

#### Real-Time Applications: 
Node.js real-time applications (jaise chat applications, gaming apps, etc.) banane ke liye ideal hai, kyunki yeh fast I/O operations handle karta hai aur low latency ke saath real-time communication support karta hai.

#### Community and Ecosystem: 
Node.js ka ek bohot bada aur active community hai jo regularly new modules aur updates release karte hain, jo developers ko naye tools aur features provide karte hain.

#### Server-Side JavaScript: 
Node.js, JavaScript ko server-side programming mein use karne ka option deta hai, jo traditionally client-side language thi. Isse full-stack development mein ease aati hai, kyunki front-end aur back-end dono mein ek hi language ka use hota hai.

# V-8 Engine

Node.js me Chrome V8 engine ek JavaScript engine hai jo JavaScript code ko directly machine code me convert karta hai, jisse code bahut tezi se execute hota hai. V8 engine Google ke dwara develop kiya gaya hai aur ye primarily Google Chrome browser me use hota hai, lekin Node.js me bhi iska istemal hota hai.

Node.js me V8 engine ka role yeh hai ke wo JavaScript ko fast execute kare bina kisi browser ke, server side pe. Jab aap Node.js me JavaScript likhte hain, toh V8 engine us code ko compile karke native machine code me convert kar deta hai, jo ki CPU ke liye directly understandable hota hai. Yeh process JavaScript ke execution ko kaafi tez bana deta hai.

# Features

#### 1. Just-In-Time (JIT) Compilation:
* V8 engine JavaScript ko directly machine code me compile karta hai jab code execute hota hai (runtime par). Iska matlab hai ki JavaScript ko pehle bytecode me convert karne ki bajaye, V8 usse directly CPU ke samajhne layak machine code me compile kar deta hai.
* Yeh process JavaScript code ki execution speed ko bahut improve karta hai.

#### 2. Memory Management (Garbage Collection):
* V8 automatic memory management karta hai. Isme garbage collection ka mechanism hota hai jo automatically unused objects ko memory se remove kar leta hai, jisse application ki memory efficient tarike se use hoti hai aur memory leaks se bachav hota hai.
* V8 engine ka garbage collector incremental aur generational garbage collection strategies use karta hai, jo performance ko better banata hai.

#### 3. Optimized Execution:
* V8 engine repeatedly run hone wale code ko optimize karta hai. Jab ek function ya code ka part baar-baar execute hota hai, V8 usse optimize karne ke liye uska machine code create karta hai, jo future me aur fast run hota hai.
* Yeh hota hai "Hot Code Path Optimization," jisme V8 code ka analysis karta hai aur frequently run hone wale parts ko specially optimize karta hai.

#### 4. Efficient Object Representation:
* V8 objects ko efficient tarike se represent karta hai. Yeh engine memory mein objects ko compactly store karta hai, jisse memory ki wastage kam hoti hai.
* V8 ka approach inline caching aur hidden classes ka use karta hai, jo object property lookup ko fast banata hai.

#### 5. C++ Written:
* V8 engine ko C++ me likha gaya hai, jo naturally fast aur efficient hota hai. C++ ke performance benefits ko use karke, V8 ko high-speed JavaScript execution ke liye design kiya gaya hai.

#### 6. Cross-Platform Compatibility:
* V8 engine platform independent hai, yaani yeh Linux, Windows, macOS, aur other operating systems pe efficiently run kar sakta hai. Iska design aisa hai ki different environments me optimized performance de sake.

#### 7. Parallelism and Multi-Core Utilization:
* V8 ka JIT compiler modern processors ke multiple cores ko efficiently utilize karta hai, jisse execution speed ko aur better banaya ja sakta hai.
* Yeh engine asynchronous code ko parallel execute karne ke liye optimized hai, jo Node.js me scalability ko improve karta hai.

#### 8. ECMAScript Standard Compliance:
* V8 engine latest ECMAScript specifications ko support karta hai. Yeh ensure karta hai ki JavaScript me naye features aur improvements ko quickly adopt kiya ja sake, jisse developers ko naye features ka use karne me koi problem na ho.

#### 9. Inline Caching:
* V8 engine inline caching technique use karta hai, jo property access ke operations ko fast karta hai. Jab aap ek property access karte ho, V8 cache mein uski location store kar leta hai, taaki next time wo faster access ho sake.

#### 10. Efficient String Handling:
* V8 strings ko efficiently handle karta hai. JavaScript me strings kaafi frequent hoti hain, aur V8 unhe optimize karne ke liye compressed strings aur string interning ka use karta hai, jo memory usage ko kam karta hai.

# RunTime Env:-

Node.js me "runtime environment" ka matlab hota hai wo environment jisme JavaScript code run karta hai. Node.js ek open-source, cross-platform runtime environment hai jo JavaScript ko server-side pe run karne ke liye use hota hai.

JavaScript pehle sirf browser ke andar run hota tha (client-side), lekin Node.js ke zariye, JavaScript ko ab server pe bhi run kar sakte hain. Node.js me runtime environment ka kaam hai.

#### V8 Engine:
Node.js ka core part Google ka V8 engine hota hai jo JavaScript ko machine code me compile karta hai aur usko execute karta hai. V8 engine ko pehle Chrome browser me use kiya gaya tha, lekin ab Node.js me bhi use hota hai.

#### Event-driven Architecture:
Node.js ek asynchronous, event-driven architecture follow karta hai. Iska matlab hai ki jab koi task run hota hai, toh wo thread ko block nahi karta, aur Node.js apne event loop ke zariye tasks ko handle karta hai.

#### Libraries/Modules: 
Node.js ka runtime environment libraries aur built-in modules provide karta hai jese ki fs (file system), http (server banane ke liye), path (file paths handle karne ke liye) etc. Ye modules developer ko aasan banate hain server-side tasks karne me.

#### Non-blocking I/O: 
Node.js me I/O (Input/Output) operations non-blocking hote hain. Matlab jab data ko read ya write karte hain (jaise database se data fetch karna), toh Node.js apne event loop ke zariye baaki operations ko handle karta hai bina kisi delay ke.

# REPL

REPL ka matlab hai Read-Eval-Print Loop. Yeh ek interactive programming environment hota hai jisme aap code likhte hain, usse turant execute karte hain, aur uska result dekhte hain.

JavaScript mein REPL ka use kaafi common hai, especially jab aap directly browser ke developer tools mein ya Node.js mein code run karte hain.

##### REPL ka kaam kaise karta hai:

* Read: Aap jo code likhte hain, woh system read karta hai.
* Eval: System us code ko evaluate (execute) karta hai.
* Print: Result ko print karke aapko output dikhata hai.
* Loop: Yeh process repeat hota rehta hai jab tak aap naya code nahi likhte.

`Node.js: Agar aap terminal mein node likhte hain, toh aap Node.js ka REPL mode activate karte hain jahan aap JavaScript code likh ke turant result dekh sakte hain.`

##### Read:
* Jab aap REPL environment mein kuch likhte hain (jaise koi JavaScript expression ya statement), toh sabse pehle woh input system ke dwara read kiya jata hai.
* Example: Agar aap likhte hain let a = 10, toh yeh read kiya jata hai aur system samajhta hai ki aap variable a ko 10 assign kar rahe hain.

##### Eval (Evaluate):
* Jab input ko read kar liya jaata hai, toh system us input ko evaluate karta hai.
* Evaluate ka matlab hai, us code ko execute karna, jo result generate karega.
* Example: Agar aap likhte hain 2 + 3, toh yeh evaluate karke result 5 generate karega.

##### Print:
* Evaluate karne ke baad, system result ko print (display) karta hai.
* Yeh step aapko turant result dikhata hai, jisse aap samajh paate hain ki aapka code sahi kaam kar raha hai ya nahi.
* Example: Agar aap let a = 10; a * 2 likhte hain, toh output hoga 20.

##### Loop:
* Yeh process loop ki tarah continuous chalta rehta hai, jab tak aap REPL environment mein naye expressions likhte rahte hain.
* Yeh loop aapko continuous interaction ka experience deta hai, jisme aap har bar naya code likh ke turant result dekh sakte hain.

# Buffer Data

Buffer Node.js mein ek powerful concept hai jo binary data ko efficiently handle karne ke liye use hota hai. Iska use mostly tab hota hai jab aapko raw binary data (jaise images, audio, video files, or network streams) ko directly manage karna ho. JavaScript ke normal types (strings aur arrays) binary data ko handle nahi karte, isliye Node.js mein Buffer class ko introduce kiya gaya hai.

## Buffer Methods

##### Buffer.concat(): 
Jab aapke paas multiple buffers hoti hain aur aap unko combine karna chahte ho, to Buffer.concat() ka use kiya jata hai. Is method se aap ek naya buffer bana sakte hain jo in buffers ko combine kare.


```python
const buf1 = Buffer.from('Hello');
const buf2 = Buffer.from('World');
const combinedBuffer = Buffer.concat([buf1, buf2]);
console.log(combinedBuffer.toString()); // Output: 'HelloWorld'
```

##### Buffer.compare(): 
Agar aapko do buffers ko compare karna ho, to Buffer.compare() method ka use kiya jata hai. Yeh function buffer ke beech ki comparison karta hai aur bataata hai ki ek buffer doosre se chhota, bara, ya equal hai.


```python
const buf1 = Buffer.from('abc');
const buf2 = Buffer.from('abd');
const result = Buffer.compare(buf1, buf2);
console.log(result); // Output: -1, because 'abc' < 'abd'
```

##### Buffer.slice(): 
Agar aapko buffer ka ek part chahiye, to aap slice() method ka use kar sakte ho. Yeh method ek naya buffer return karta hai jo original buffer ke ek subset ko represent karta hai.


```python
const buf = Buffer.from('Hello, Node.js!');
const slicedBuffer = buf.slice(0, 5); // Extracts 'Hello'
console.log(slicedBuffer.toString()); // Output: 'Hello'
```

##### Buffer.from() with encoding: 
Jab aap ek string ko buffer mein convert karte hain, to aap encoding specify kar sakte hain.


```python
const buf = Buffer.from('Hello, Node.js!', 'utf8');
console.log(buf); // Output: <Buffer 48 65 6c 6c 6f 2c 20 4e 6f 64 65 2e 6a 73 21>
```

##### Buffer.toString() with encoding: 
Buffer se string banate waqt, aap encoding specify kar sakte hain.


```python
const buf = Buffer.from('SGVsbG8sIE5vZGUuanMh', 'base64');
console.log(buf.toString('utf8')); // Output: 'Hello, Node.js!'
```

# Types of Module:-

### 1. Core Modules: 
These are built-in modules that come with Node.js. You don't need to install them separately. Examples include:

* http (for creating servers)
* fs (for file system operations)
* path (for handling and transforming file paths)
* os (for operating system-related utility methods)
* events (for event-driven programming)


```python
const http = require('http');
```

### 2.Local Modules: 
These are modules that you create in your project. They can be in any file you like, and you can export functionality from one file and import it into another using require().


```python
# Math.js

module.exports.add = (a, b) => a + b;

# app.js

const math = require('./math');
console.log(math.add(2, 3));  // Output: 5
```

### 3. Third-Party Modules: 
These are external modules that are installed via npm (Node Package Manager). You can install them using commands like npm install <module-name>. Examples include:

* express (a web application framework)
* lodash (a utility library)
* mongoose (a MongoDB ODM)


```python
const express = require('express');
const app = express();
```

# Create Server in Node:-


```python
const http = require('http');

// server banate hain
const server = http.createServer((req, res) => {
    res.writeHead(200, {'Content-Type': 'text/plain'});

    res.end('Hello, Node.js server!');
});

server.listen(3000, () => {
    console.log('Server running at http://localhost:3000/');
});
```

#### Explanation:
* http.createServer() ek server create karta hai.
* req (request) aur res (response) parameters mein client ke request aur server ka response hota hai.
* res.writeHead() response header set karta hai, jisme status code aur content type specify karte hain.
* res.end() se response send kiya jata hai aur server client ko response de deta hai.
* server.listen(3000) se server 3000 port par sunne lagta hai.

# Routing in NodeJs?


```python
const http = require('http');

const server = http.createServer((req, res) => {
  // URL aur method ko check karte hain
  if (req.url === '/' && req.method === 'GET') {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>Welcome to the Home Page!</h1>');
  } else if (req.url === '/about' && req.method === 'GET') {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>This is the About Page.</h1>');
  } else if (req.url === '/contact' && req.method === 'GET') {
    res.writeHead(200, { 'Content-Type': 'text/html' });
    res.end('<h1>Contact us at: contact@example.com</h1>');
  } else {
    res.writeHead(404, { 'Content-Type': 'text/html' });
    res.end('<h1>Page Not Found!</h1>');
  }
});

server.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

```

# Event // EventEmitter :-

Node.js me Event module ek built-in module hota hai jo event-driven programming ko support karta hai. Is module ka use events ko handle karne ke liye hota hai. Node.js me everything asynchronous hota hai, aur events ke through hum asynchronous operations ko manage kar sakte hain.

##### Key Concepts:
* EventEmitter Class: EventEmitter ek class hai jo events ko handle karti hai. Iska use hum event-driven programming me karte hain. Agar aap kisi bhi asynchronous task ko perform kar rahe hain, jaise file reading, HTTP request, etc., to aap EventEmitter ka use karke event trigger kar sakte hain jab task complete ho.
* Events: Event ek signal hai jo indicate karta hai ke koi specific task complete ho gaya hai. For example, "data" event trigger ho sakta hai jab koi data stream ho.
* Listeners: Listener wo function hote hain jo event ke trigger hone par execute hote hain. Jab hum ek event emit karte hain, to listener wo function hote hain jo execute hota hai.

### Simple Example:-


```python
const EventEmitter = require('events');

// EventEmitter ka ek instance banate hain
const myEmitter = new EventEmitter();

// Event listener set karte hain
myEmitter.on('greet', () => {
  console.log('Hello, EventEmitter!');
});

// Event trigger karte hain
myEmitter.emit('greet');

# Output ==> Hello, EventEmitter!
```

#### Explanation:
* Humne greet naam ka ek event banaya aur usse handle karne ke liye on() method se ek listener set kiya.
* Jab emit() method call hota hai, tab listener execute hota hai aur output me "Hello, EventEmitter!" print hota hai.

### Multiple Listeners



```python
const EventEmitter = require('events');
const myEmitter = new EventEmitter();

// Pehla listener
myEmitter.on('event', () => {
  console.log('Listener 1 triggered!');
});

// Doosra listener
myEmitter.on('event', () => {
  console.log('Listener 2 triggered!');
});

// Event trigger karte hain
myEmitter.emit('event');

#Output==> Listener 1 triggered!
           Listener 2 triggered!
```

#### Explanation:
* Humne event naam ka ek event banaya aur uske liye do alag listeners set kiye hain.
* Jab emit() method call hota hai, dono listeners execute hote hain aur dono messages print hote hain.

### Passing Arguments with Events


```python
const EventEmitter = require('events');
const myEmitter = new EventEmitter();

// Listener jo arguments ko handle karega
myEmitter.on('greet', (name, age) => {
  console.log(`Hello, ${name}! You are ${age} years old.`);
});

// Event trigger karte hain aur arguments pass karte hain
myEmitter.emit('greet', 'Alice', 25);

#Output==> Hello, Alice! You are 25 years old.

```

### Once Listener
Agar aap chahte hain ki koi event sirf ek baar trigger ho, to aap once() method ka use kar sakte hain. Yeh listener event ke pehle trigger hone ke baad automatically remove ho jata hai.


```python
const EventEmitter = require('events');
const myEmitter = new EventEmitter();

myEmitter.once('event', () => {
  console.log('This will only be triggered once!');
});

// First time event trigger karte hain
myEmitter.emit('event');

// Second time event trigger karte hain (kuch nahi hoga)
myEmitter.emit('event');

#Output ===> This will only be triggered once!
```

#### Explanation:
* once() method ke through humne listener ko set kiya hai jo sirf ek baar trigger hoga.
* Jab pehli baar emit() call hota hai, listener execute hota hai. Dusri baar trigger karne par kuch nahi hota, kyunki once listener ko remove kar diya gaya hai.

### Event with Async Operations (Simulating File Reading)
Yeh example ek realistic scenario ko dikhata hai jahan hum asynchronous task (jaise file reading) ke liye events ka use karte hain.


```python
const EventEmitter = require('events');
const myEmitter = new EventEmitter();

// Simulate asynchronous file reading (using setTimeout)
myEmitter.on('readFile', () => {
  console.log('Reading file...');
  setTimeout(() => {
    console.log('File read complete!');
    myEmitter.emit('fileReady');  // Another event trigger
  }, 2000);
});

myEmitter.on('fileReady', () => {
  console.log('File is ready for processing.');
});

// Trigger the file reading event
myEmitter.emit('readFile');

# Output===> Reading file...
            File read complete!
            File is ready for processing.
```

#### Explanation:
* Humne readFile event ko trigger kiya aur uske andar ek asynchronous task (simulated using setTimeout) rakha.
* Jab file reading complete hoti hai, fileReady event trigger hota hai aur listener execute hota hai.

# Nodejs Streams:-

Node.js me Streams ek powerful concept hai jo large amounts of data ko efficiently handle karne ke liye use hota hai. Stream ek abstract interface hai, jiska use data ko asynchronously process karne ke liye kiya jata hai.

##### Stream Kya Hai?
Aapko sochna hoga jaise ek pipe. Imagine karo ek pipe me paani chal raha ho. Jab aap us pipe ko dekhte ho, to aap pura paani ek sath nahi dekh rahe hote, balki paani ka ek chhota hissa dheere dheere nikalta hai. Streams bhi waise hi kaam karti hain, lekin data ke saath.

##### Stream ka Use Kahan Hoti Hai?

`Pehla example:` File reading Jab aap kisi bade file ko read karte ho (jaise 1 GB ka file), to agar aap poora file ek sath memory me load karoge, to aapka system slow ho sakta hai, ya memory full ho sakti hai. Stream ka use karke, hum file ko chhote-chhote parts me read kar sakte hain (chunks me), isse pura file ek sath memory me nahi aata aur system smooth chalti hai.

`Dusra example:` Web requests Jab aap internet se data fetch karte ho, to aapko pura data ek sath nahi milta, wo dheere dheere aata hai. Streams ka use hota hai is data ko handle karne ke liye. Jab ek chhota data ka hissa aata hai, aap uss data pe kaam kar sakte ho, jab tak baaki data aata hai.

### Streams ki types:

`Readable Streams:` Ye wo streams hoti hain jahan se aap data ko read kar sakte hain. Jaise ki file system se data read karna ya HTTP response.
* Example: fs.createReadStream()

`Writable Streams:` Ye wo streams hoti hain jahan aap data ko write kar sakte hain. Jaise ki file system me data likhna ya HTTP request bhejna.
* Example: fs.createWriteStream()

`Duplex Streams:` Ye wo streams hoti hain jahan aap data ko read bhi kar sakte hain aur write bhi kar sakte hain ek hi stream ke andar.
* Example: net.Socket (Network communication me use hoti hain)

`Transform Streams:` Ye duplex streams ka ek special case hoti hain, jo data ko read karte waqt usko transform bhi karte hain. Jaise ki compression, encryption, etc.
* Example: zlib.createGzip() (Jo data ko compress karne ke liye use hota hai)

### Example:
Agar aap ek file ko read kar rahe hain, to pure file ko ek sath memory me load karne ki bajaye, aap usko stream ki madad se chhote-chhote chunks me read kar sakte hain. Isse performance improve hoti hai aur memory ka consumption bhi kam hota hai.


```python
const fs = require('fs');
const readableStream = fs.createReadStream('largefile.txt');

readableStream.on('data', (chunk) => {
  console.log(`Received ${chunk.length} bytes of data.`);
});

readableStream.on('end', () => {
  console.log('End of stream.');
});
```

#### Benefits:
`Memory Efficient:` Pura data ek sath load nahi hota, sirf chhota hissa load hota hai.

`Fast:` Aap data ke parts ko process karte ho jab wo aata hai, isse application fast chalti hai.

`Easy to Use:` Streams ka use karte hue aap ko asynchronous programming ka faida milta hai, jo system ko block nahi karta.


```python

```
