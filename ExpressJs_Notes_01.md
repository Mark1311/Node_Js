# What is ExpressJs ?

Express.js ek lightweight aur flexible framework hai jo Node.js ke upar build hota hai. Yeh web applications aur RESTful APIs banane ke liye kaafi popular hai. Express ko specifically Node.js ko simplify karne ke liye design kiya gaya hai, jisse developers ko complex web applications banate waqt zyada problems na aaye.

Express.js ek web application framework hai jo Node.js ke upar kaam karta hai. Yeh framework developers ko web applications aur APIs banane ke liye ek simple aur flexible way provide karta hai.

```js
// Used for Import express

const express = required('express')
const app = express();
```

# Features

#### Routing:
* Express mein aap easily different HTTP methods ko handle kar sakte hain jaise GET, POST, PUT, DELETE, etc.
* Aap specific URL patterns ko match karne ke liye routes define kar sakte hain. Yeh request ko different handlers tak forward karta hai.


```python
app.get('/about', (req, res) => {
  res.send('About Page');
});

app.post('/submit', (req, res) => {
  res.send('Data submitted');
});
```

### Middleware:
* Middleware functions Express mein ek important role play karte hain. Yeh functions incoming request ke beech mein run hote hain aur request ko modify karte hain ya response ko change karte hain.
* Middleware ko use karke aap tasks jaise authentication, logging, error handling, data validation, etc. easily kar sakte hain.


```python
// Simple Middleware
app.use((req, res, next) => {
  console.log('Request received at: ' + new Date());
  next();  // Call next middleware or route handler
});

```

### Template Engines:
* Express aapko dynamic web pages banane ke liye template engines ka support deta hai. Kuch common template engines hain EJS, Pug, Handlebars, etc.
* Yeh engine aapko dynamic content ko HTML pages mein inject karne mein madad karte hain


```python
app.set('view engine', 'ejs');
app.get('/', (req, res) => {
  res.render('index', { title: 'Express App' });
});
```

### Static Files:
* Express static files serve karne ke liye express.static middleware provide karta hai. Aap easily CSS, JavaScript, images, etc. ko serve kar sakte hain bina kisi complex configuration ke.


```python
app.use(express.static('public'));  // 'public' folder se static files serve karega
```

### Error Handling:
* Express mein error handling kaafi flexible hai. Aap custom error handlers bana sakte hain jo error message ko format karke user ko return kar sake.


```python
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something went wrong!');
});
```

### Support for APIs:
* Express kaafi asaani se RESTful APIs create karne mein madad karta hai. Aap routes define karke client requests ko handle kar sakte hain (for example, data ko fetch karna ya submit karna).


```python
app.get('/api/users', (req, res) => {
  res.json([{ name: 'John' }, { name: 'Jane' }]);  // Sample API response
});
```

### Request and Response Handling:
* Express mein request aur response ko manage karna asaan hai. Aap query parameters, request bodies, headers, cookies, etc. ko easily handle kar sakte hain.
* Express automatically JSON data ko parse karne ka kaam karta hai jab client request mein application/json content type bhejta hai.


```python
app.post('/api/login', (req, res) => {
  const { username, password } = req.body;
  if(username === 'admin' && password === '1234') {
    res.send('Login successful');
  } else {
    res.status(400).send('Invalid credentials');
  }
});
```

### Routing Parameters:
* Aap URL mein dynamic segments (route parameters) use kar sakte hain. Yeh aapko URLs ko specific data ke saath link karne mein madad karte hain.


```python
app.get('/user/:id', (req, res) => {
  const userId = req.params.id;
  res.send('User ID is: ' + userId);
});
```

# Advantage

##### 1. Lightweight and Minimalistic
* Express.js kaafi lightweight aur minimalistic hai, jo aapko sirf zaroori features provide karta hai. Yeh unnecessary features ko avoid karta hai, jisse aapko ek clean aur fast framework milta hai.

* Aap apne project ki specific requirements ke hisaab se libraries aur middleware easily add kar sakte hain.

##### 2. Routing and Middleware Support
* Express.js ka routing system kaafi flexible hai, jisme aap easily different HTTP methods (GET, POST, PUT, DELETE) ke saath routes define kar sakte hain.

* Express middleware ka support deta hai jo request aur response ko handle karne mein madad karta hai. Aap custom middleware bhi create kar sakte hain (authentication, logging, error handling, etc.).

##### 3. Fast Development Process
* Express.js ki simplicity ki wajah se development process kaafi fast ho jata hai. Aap jaldi se routes, templates, aur APIs set up kar sakte hain. Yeh aapko quickly prototypes aur fully functional web apps banane ki suvidha deta hai.

* Express ka built-in support for RESTful APIs aur templates (jaise EJS, Pug) kaafi time-saving hai.

##### 4. Asynchronous and Non-blocking
* Express.js, Node.js ke asynchronous nature ka pura fayda uthata hai. Yeh kaafi efficient hota hai, kyunki non-blocking I/O operations ki wajah se ek request ke complete hone ka wait nahi karna padta.

* Yeh scalability ko improve karta hai, jisme high-volume concurrent requests ko efficiently handle kiya ja sakta hai.

##### 5. Flexibility and Customization
* Express aapko full control deta hai apne application ke structure aur functionality pe. Aap apne project ke requirements ke hisaab se routes, middleware, and view engines ko easily customize kar sakte hain.

* Aap apni choice ka database (MongoDB, MySQL, etc.) aur other libraries use kar sakte hain.

##### 6. Support for Template Engines
* Express.js template engines ko support karta hai, jaise EJS, Pug, aur Handlebars. Yeh aapko dynamic HTML pages banane mein madad karte hain, jisme data ko server-side se inject kiya jata hai.

##### 7. Scalability
* Express.js ko easily scale kiya ja sakta hai. Aap apne application ko aise structure kar sakte hain jisse large-scale applications handle kiye ja sakte hain, jaise microservices architecture.

* Node.js ki non-blocking nature aur Express ki modularity ke wajah se applications ko horizontally scale karna possible hota hai.

##### 8. Huge Ecosystem of Modules
* Express.js ko Node.js ecosystem se integration ka faayda milta hai. NPM (Node Package Manager) se aapko thousands of modules milte hain jo aapke application ko easily extend kar sakte hain.

* Aap authentication, logging, validation, and other tasks ke liye pre-built modules use kar sakte hain.

##### 9. Great Community and Documentation
* Express.js ka ek bahut bada aur active community hai, jisse aapko tutorials, forum discussions, and open-source contributions milti hain.

* Express ka documentation kaafi achha hai, jisme step-by-step guides aur examples diye gaye hain, jo development process ko simple banate hain.

##### 10. Cross-platform
* Express.js cross-platform hai, jo aapko Windows, macOS, aur Linux jaise platforms pe develop aur deploy karne ki flexibility deta hai.

##### 11. Easy to Learn
* Agar aap JavaScript se familiar hain, toh Express.js ko seekhna kaafi asaan hota hai. Express ka syntax simple aur intuitive hai, jo quickly web server aur APIs banane mein help karta hai.

##### 12. Supports Multiple Databases
* Express.js ke saath aap easily different types of databases integrate kar sakte hain, jaise MongoDB, MySQL, PostgreSQL, etc. Yeh aapko apne application ka data store karne ke liye flexibility deta hai.

##### 13. Security Features
* Express.js mein built-in security features bhi hote hain. Aap easily tools jaise Helmet ko integrate kar sakte hain jo HTTP headers ko secure karne mein madad karta hai.

* Aap CORS (Cross-Origin Resource Sharing) ko configure kar sakte hain, taaki security breaches ko avoid kiya ja sake.

##### 14. Error Handling
* Express.js mein error handling kaafi efficient hai. Aap custom error handling middleware create kar sakte hain jo application ke errors ko manage kar sake aur users ko appropriate responses de sake.

# Simple Routing


```python
// Import express module
const express = require('express');

// <<<====== or =====>>>

// Express ko import kiya (Modern ES Module tarika)
import express from 'express';

// Create an Express application
const app = express();

// Define the port on which the server will run
const port = 3000;

// Define a simple route
app.get('/', (req, res) => {
  res.send('Hello, World!');
});

// Define another route
app.get('/about', (req, res) => {
  res.send('This is the about page');
});

// Start the server and listen on the specified port
app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});

```

# Serve HTML File in Express:- 


```python
const express = require('express');
const path = require('path');
const app = express();
const port = 3000;

// Static file serving (optional, for CSS/JS images, etc.)
app.use(express.static(path.join(__dirname, 'public')));

// Route to serve the HTML file
app.get('/', (req, res) => {
  res.sendFile(path.join(__dirname, 'index.html'));
});

// Start the server
app.listen(port, () => {
  console.log(`Server is running at http://localhost:${port}`);
});

```

# Send Html Raw Data in Express:-


```python
const express = require('express');
const app = express();

app.get('/html', (req, res) => {
  res.send('<h1>This is HTML content!</h1>');
});

app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

NOte:- If We used Template Engine, so we {user= res.render()}this method.
```

# Send Json Raw Data in Express:-


```python
const express = require('express');
const app = express();

app.get('/jsondata', (req, res) => {
  const data = {
    message: "This is JSON data",
    status: "success"
  };
  res.json(data);
});

app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

```
# Output

{
  "message": "This is JSON data",
  "status": "success"
}

# Send Json Data from Another Json File:-


```python
// data.json File
{
  "message": "This is data from another file",
  "status": "success"
}

```


```python
// app.js File
const express = require('express');
const app = express();

// Import the JSON data from another file
const jsonData = require('./data.json');

// Route to send JSON data from the imported file
app.get('/json', (req, res) => {
  res.json(jsonData);
});

// Start the Express server
app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

```

# Send Data in Express Using Template Engine:-

## Example_01:-

npm install express ejs


```python
const express = require('express');
const app = express();

// Set the view engine to EJS
app.set('view engine', 'ejs');

// Create a route that sends HTML using EJS template
app.get('/html', (req, res) => {
  res.render('index', { title: 'My Web Page', message: 'Hello from EJS!' });
});

app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

```


```python
### views/index.ejs File Name:-

<!DOCTYPE html>
<html>
<head>
  <title><%= title %></title>
</head>
<body>
  <h1><%= message %></h1>
</body>
</html>

```

# Example_02:-


```python
## views/index.ejs File Name

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>User Information</title>
</head>
<body>
  <h1>Welcome, <%= user.name %>!</h1>
  <p>Age: <%= user.age %></p>
</body>
</html>

```


```python
const express = require('express');
const path = require('path');

const app = express();

// Set the view engine to EJS
app.set('view engine', 'ejs');

// Set the folder where views (templates) will be stored
app.set('views', path.join(__dirname, 'views'));

// Serve a route
app.get('/', (req, res) => {
  // Data you want to send to your template
  const user = {
    name: 'John Doe',
    age: 30,
  };

  // Render the template and pass the data to it
  res.render('index', { user });
});

// Start the server
app.listen(3000, () => {
  console.log('Server is running on http://localhost:3000');
});

```

# middleware 

Express.js me middleware ek function hota hai jo request aur response cycle ke beech me execute hota hai. Ye functions HTTP requests ko process karte hain, jaise ki request data ko validate karna, logging, authentication, authorization, error handling, etc. Middleware request ko modify kar sakte hain ya response bhejne se pehle kuch operations perform kar sakte hain.

Jab koi user aapke server par request bhejta hai, toh wo request seedhe aapke final route handler (jaise app.get()) tak nahi pahonchti. Uske beech mein ek ya kai saare functions hote hain jinse hokar request ko guzarna padta hai—inhi beech wale functions ko hum Middleware kehte hain.

### Example:-
```js
const express = require('express');
const app = express();

// 1. Ek Custom Middleware Function
const checkSecurity = (req, res, next) => {
    const password = req.query.pass;
    
    if (password === 'secret123') {
        next(); // Agar password sahi hai, toh agle step par bhejo
    } else {
        res.send("Galat Password! Aap andar nahi ja sakte."); // Wahin se rok diya
    }
};

// 2. Middleware ko apply karna
app.use(checkSecurity); 

// 3. Final Route
app.get('/dashboard', (req, res) => {
    res.send("Welcome to the Secret Dashboard!");
});
```

# Type of Middleware

##### Application-level middleware: 
Ye middleware poori application pe apply hota hai. Aap isse app-level pe define karte hain.


```python
app.use((req, res, next) => {
  console.log("Request received");
  next(); // Request ko next middleware ya route handler pe pass karte hain
});

```

##### Router-level middleware: 
Ye middleware specific route ya router pe apply hota hai. Agar aap sirf ek route ke liye middleware chahte hain, to aap use router ke saath define kar sakte hain.


```python
const router = express.Router();
router.use((req, res, next) => {
  console.log("Router-level middleware");
  next();
});
```

##### Error-handling middleware: 
Ye special type ka middleware hota hai jo errors handle karta hai. Agar koi error middleware me throw hoti hai, to error-handling middleware usse catch karta hai.


```python
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something went wrong!');
});
```

##### Built-in middleware: 
Express kuch built-in middleware functions provide karta hai, jaise express.json() jo request body ko JSON me parse karta hai, ya express.static() jo static files serve karta hai.

##### Custome Middleware
custom middleware functions allow you to add extra functionality to the request-response cycle. Here's an example of how to create and use custom middleware in an Express.js application:


```python
const logRequestDetails = (req, res, next) => {
  console.log(`Request Method: ${req.method}`);
  console.log(`Request URL: ${req.url}`);
  next(); // Pass control to the next middleware or route handler
};

// Use the custom middleware
app.use(logRequestDetails);
```

###### Custom Middleware for Specific Routes


```python
// Only for the '/about' route
app.get('/about', logRequestDetails, (req, res) => {
  res.send('About Page');
});
```

# Example of All Types of Middleware in Express:



```python
const express = require('express');
const morgan = require('morgan'); // Third-party middleware for logging
const cors = require('cors'); // Third-party middleware for Cross-Origin Resource Sharing

const app = express();
const port = 3000;

// Built-in middleware to parse JSON requests
app.use(express.json()); 

// Built-in middleware to parse URL-encoded data
app.use(express.urlencoded({ extended: true }));

// Built-in middleware to serve static files from the "public" folder
app.use(express.static('public'));

// Third-party middleware: HTTP request logger (Morgan)
app.use(morgan('dev')); 

// Third-party middleware: Enable Cross-Origin Requests (CORS)
app.use(cors());

// Custom Middleware: Logs request details
const logRequestDetails = (req, res, next) => {
  console.log(`Request Method: ${req.method}`);
  console.log(`Request URL: ${req.url}`);
  next();
};

// Apply custom middleware to all routes
app.use(logRequestDetails);

// Route handler (GET)
app.get('/', (req, res) => {
  res.send('Hello, World!');
});

// Route handler (GET)
app.get('/about', (req, res) => {
  res.send('About Page');
});

// Route handler with custom middleware (for specific route)
app.get('/special', (req, res, next) => {
  console.log('Special route hit');
  next(); // Pass control to the next middleware or route handler
}, (req, res) => {
  res.send('Special Route');
});

// Error-handling middleware
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something went wrong!');
});

// Start server
app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});

```
# app.use() aur app.get() 

> app.use() ka istemal Middleware register karne ke liye hota hai (jo har request par ya kisi specific path ke sabhi methods par chalta hai).  
> app.get() ka istemal ek specific URL par sirf GET request (data fetch karne) ko handle karne ke liye hota hai.  

### app.use() (The Middleware Handler)
- Kaam kaise karta hai: Yeh HTTP method (GET/POST) nahi dekhta. Agar path match ho gaya (ya koi path nahi diya), toh yeh execute ho jayega.
- Kiske liye use hota hai: Logging, parsing (body-parser), cookies check karna, sessions manage karna, ya static files (images/CSS) serve karne ke liye.
```js
Kaam kaise karta hai: Yeh HTTP method (GET/POST) nahi dekhta. Agar path match ho gaya (ya koi path nahi diya), toh yeh execute ho jayega.

Kiske liye use hota hai: Logging, parsing (body-parser), cookies check karna, sessions manage karna, ya static files (images/CSS) serve karne ke liye.
```
### app.get() (The Route Handler)
Yeh ek Routing method hai. Yeh tabhi trigger hota hai jab do conditions match hoti hain:
1. URL match hona chahiye (Path match).
2. HTTP Request ka method sirf GET hona chahiye.
- Kaam kaise karta hai: Yeh specific hota hai. Agar user ne POST request bheji hai, toh app.get() use handle nahi karega.
- Kiske liye use hota hai: User ko koi web page dikhane ke liye ya server se data (API response) bhejne ke liye.
```js
// Yeh tabhi chalega jab user sirf homepage ('/') par GET request karega
app.get('/', (req, res) => {
    res.send("Welcome to Homepage!");
});
```

> app.use() Security guard ki tarah hai jo entrance par khada hai. Woh har aane wale guest ko check karega, chahe wo khana khane aaya ho ya room book karne.

> app.get() Receptionist ya Waiter ki tarah hai, jo tabhi kaam karega jab aap uske paas jaakar ek specific order (jaise: "Mujhe menu card do" - GET Request) doge.

| Feature | `app.use()` | `app.get()` |
| :--- | :--- | :--- |
| **Primary Role** | Middleware register karne ke liye. | Specific GET route ko handle karne ke liye. |
| **HTTP Method** | Kisi bhi HTTP method (GET, POST, PUT, DELETE) par chal jata hai. | **Sirf** GET request par chalta hai. |
| **Path Matching** | Yeh **Prefix matching** karta hai. (Agar `/user` likha hai, toh `/user/profile` aur `/user/settings` dono par chalega). | Yeh **Exact matching** karta hai. (Agar `/user` likha hai, toh sirf `/user` par hi chalega). |
| **`next()` function** | Ismein `next()` call karna zaroori hota hai taaki request aage badh sake, warna browser ghumta rahega. | Ismein aamtaur par `res.send()` ya `res.json()` karke response end kar diya jata hai. |

# next() function
Jab bhi Express mein koi request aati hai, toh wo ek ke baad ek kai saare Middlewares (functions) se hokar guzarti hai. next() function ka kaam agale middleware ya route handler ko trigger karna hota hai

### next() Function ka Asli Role Kya Hai?
Express mein jab aap koi middleware likhte hain, toh usmein teen arguments hote hain: req (request), res (response), aur next.
```js
app.use((req, res, next) => {
    console.log("Middleware 1: Request aayi");
    next(); // Yeh request ko agle middleware/route par bhej dega
});

app.get('/', (req, res) => {
    res.send("Hello World!"); // Yahan response khatam ho gaya
});
```

### Agar next() ko call NA karein toh kya hoga?
-  Aapka browser ya client Hanging State (infinite loading) mein chala jayega, aur kuch samay baad Timeout ho jayega.
- Agar aapne apne middleware mein na toh next() ko call kiya aur na hi res.send() ya res.json() karke response ko end kiya, toh Express ko samajh nahi aata ki ab aage kya karna hai.

# Ek basic server setup karke dikhao.
```js
// 1. Express module ko import karein
const express = require('express');

// 2. Express ka ek instance (app) banayein
const app = express();

// 3. Port number define karein jahan server chalega
const PORT = 3000;

// 4. Ek basic GET route banayein (Homepage ke liye)
app.get('/', (req, res) => {
    res.send('Arrey waah! Aapka Express server sahi se chal raha hai.');
});

// 5. Server ko listen mode mein dalein taaki wo requests accept kar sake
app.listen(PORT, () => {
    console.log(`Server successfully chal raha hai http://localhost:${PORT} par`);
});
```

# Ek basic CRUD API (Create, Read, Update, Delete) ka structure likh kar dikhao.

```js
const express = require('express');
const app = express();
const PORT = 3000;

// Middleware: Taaki hamara server incoming JSON data ko samajh sake
app.use(express.json());

// Dummy Database (Hum filhal memory mein data store kar rahe hain)
let users = [
    { id: 1, name: 'Rahul', email: 'rahul@example.com' },
    { id: 2, name: 'Sneha', email: 'sneha@example.com' }
];

// ==========================================
// 1. READ (Get all users or a single user)
// ==========================================

// Sabhi users ko dekhne ke liye
app.get('/api/users', (req, res) => {
    res.status(200).json(users);
});

// Kisi ek specific user ko uski ID se dekhne ke liye
app.get('/api/users/:id', (req, res) => {
    const userId = parseInt(req.params.id);
    const user = users.find(u => u.id === userId);

    if (!user) {
        return res.status(404).json({ message: "User nahi mila!" });
    }
    res.status(200).json(user);
});

// ==========================================
// 2. CREATE (Naya user add karne ke liye)
// ==========================================
app.post('/api/users', (req, res) => {
    // Browser/Postman se aane wala data req.body mein hota hai
    const { name, email } = req.body;

    if (!name || !email) {
        return res.status(400).json({ message: "Name aur Email zaroori hain!" });
    }

    const newUser = {
        id: users.length + 1, // Ek nayi ID generate ki
        name: name,
        email: email
    };

    users.push(newUser); // Array mein add kar diya
    res.status(201).json({ message: "User successfully ban gaya!", data: newUser });
});

// ==========================================
// 3. UPDATE (Kisi user ka data badalne ke liye)
// ==========================================
app.put('/api/users/:id', (req, res) => {
    const userId = parseInt(req.params.id);
    const user = users.find(u => u.id === userId);

    if (!user) {
        return res.status(404).json({ message: "User nahi mila jise update kiya ja sake!" });
    }

    const { name, email } = req.body;

    // Agar naya naam ya email diya hai toh update karo, nahi toh purana hi rehne do
    if (name) user.name = name;
    if (email) user.email = email;

    res.status(200).json({ message: "User update ho gaya!", data: user });
});

// ==========================================
// 4. DELETE (Kisi user ko hatane ke liye)
// ==========================================
app.delete('/api/users/:id', (req, res) => {
    const userId = parseInt(req.params.id);
    const userIndex = users.findIndex(u => u.id === userId);

    if (userIndex === -1) {
        return res.status(404).json({ message: "User nahi mila jise delete kiya ja sake!" });
    }

    // Array se user ko hata diya
    const deletedUser = users.splice(userIndex, 1);

    res.status(200).json({ message: "User successfully delete ho gaya!", data: deletedUser[0] });
});

// Server ko start karna
app.listen(PORT, () => {
    console.log(`CRUD API server chal raha hai: http://localhost:${PORT}`);
});
```

# req.params, req.query, aur req.body mein kya difference hai?
| Feature | `req.params` (Route Parameters) | `req.query` (Query Parameters) | `req.body` (Request Body) |
| :--- | :--- | :--- | :--- |
| **Yeh kya hai?** | Yeh URL ka ek hissa hote hain jo **fixed pattern** mein hote hain. | Yeh URL ke aakhiri mein `?` ke baad aane wale **key-value pairs** hote hain. | Yeh user ka **hidden data** hota hai jo request ke andar chhupa hota hai. |
| **Data Kahan Se Aata Hai?** | URL ke andar hi chhupa hota hai (Route Path se). | URL ke bilkul aakhiri se (Search/Filter query se). | HTTP Request ki **Body** se (aamtaur par JSON format mein). |
| **Mukhya Istemal (Use Case)** | Kisi **specific resource** ko uski ID se pehchanne ke liye. | Data ko **Filter, Sort, Search, ya Paginate** karne ke liye. | Naya data **Create** karne ya purane ko **Update/Submit** karne ke liye. |
| **HTTP Methods** | Zyadatar `GET`, `PUT`, `DELETE` mein use hota hai. | Zyadatar `GET` requests mein use hota hai. | Sirf `POST`, `PUT`, `PATCH` mein use hota hai (GET mein nahi). |
| **Express Route Code** | `app.get('/user/:id', ...)` *(Yahan `:` lagana zaroori hai)* | `app.get('/search', ...)` *(Route mein kuch extra nahi likhna padta)* | `app.post('/login', ...)` *(Iske liye `express.json()` middleware lagta hai)* |
| **Browser URL Example** | `http://localhost:3000/user/25` | `http://localhost:3000/search?city=Delhi&sort=asc` | `http://localhost:3000/register` *(URL mein data nahi dikhta)* |
| **Server par Output (`req...`)** | `{ id: "25" }` | `{ city: "Delhi", sort: "asc" }` | `{ "username": "amit", "pass": "123" }` |

# res.send(), res.json(), aur res.end() mein kya farq hai?
| Feature | `res.send()` | `res.json()` | `res.end()` |
| :--- | :--- | :--- | :--- |
| **Mukhya Kaam** | Yeh ek **HTTP response** bhejta hai jo kisi bhi type (String, HTML, Buffer, Object, Array) ka ho sakta hai. | Yeh **sirf aur sirf JSON data** bhejne ke liye bana hai. | Yeh bina koi data bheje **Response Cycle ko jaldi khatam (end)** karne ke liye hota hai. |
| **Content-Type Header** | Yeh data ke hisaab se **automatically** header set kar deta hai (e.g., String ke liye `text/html`, Object ke liye `application/json`). | Yeh hamesha Content-Type ko **`application/json`** par set karta hai. | Ismein koi data nahi jata, isliye yeh koi Content-Type header set **nahi** karta. |
| **Data Type Support** | String, Buffer, Object, Array, ya HTML Code. | Object, Array, Number, String, ya Boolean (jo JSON mein convert ho sake). | Sirf String ya Buffer (isliye ismein data bhejna aviod kiya jata hai). |
| **Formatting** | Agar aap ismein object bhejenge, toh yeh internally `res.json()` ko hi call kar deta hai. | Yeh data ko `JSON.stringify()` karke bhejta hai aur Express settings (jaise spaces formatting) ko follow karta hai. | Yeh raw data bhejta hai bina kisi processing ya formatting ke. |
| **Mukhya Use Case** | Jab aapko koi simple text message, HTML page, ya generic data response bhejna ho. | Jab aap **REST API** bana rahe hon aur frontend ko sirf JSON data dena ho. | HTTP Status codes (jaise `404` ya `204 No Content`) bhejkar request ko jaldi close karna ho. |
| **Code Example** | `res.send("<h1>Hello</h1>");` | `res.json({ status: "success", data: [] });` | `res.status(404).end();` |

# Express application mein static files (jaise images, CSS) ko kaise serve kiya jata hai?
Express.js mein static files (jaise images, CSS, JavaScript files, ya PDFs) ko serve karne ke liye Express ka ek built-in middleware use kiya jata hai, jiska naam hai express.static().

Iske liye aapko koi alag se routes (app.get) banane ki zaroori nahi hoti. Bas ek line ka code likhna padta hai aur Express poore folder ki files ko automatically accessible bana deta hai.

#### Step 1: Ek Folder Banayein
```text
my-app/
├── index.js
├── package.json
└── public/
    ├── css/
    │   └── style.css
    └── images/
        └── logo.png
```
#### Step 2: Server Code Mein Middleware Add Karein (index.js)
```js
const express = require('express');
const path = require('path'); // Node.js ka built-in module
const app = express();

// Static files serve karne ke liye middleware (Sabse best aur safe tareeka)
app.use(express.static(path.join(__dirname, 'public')));

app.get('/', (req, res) => {
    res.send('Static files setup ho gayi hai!');
});

app.listen(3000, () => {
    console.log('Server running on port 3000');
});
```

# CORS kya hai aur ise Express mein kaise resolve karte hain?
Answer: Cross-Origin Resource Sharing (CORS) ek security feature hai jo browser apply karta hai. Agar aapka frontend localhost:3000 par hai aur backend localhost:5000 par, to browser request block kar dega.

Solution: Hum cors npm package install karke use karte hain:
```js
const cors = require('cors');
app.use(cors()); // Sabhi origins ke liye allow karne ke liye
```