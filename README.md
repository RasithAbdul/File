Q1 . MongoDB is a NoSQL database because it stores data in flexible, JSON-like documents, allowing for dynamic schemas and scalability.
Q2 . To insert a document into a MongoDB collection, use the insertOne() method.
Q3 . db.collection.find({age:{$gt : 20 } }); age : $gt is mean greater than .
Q4 . To update a document in MongoDB to set a new value for a field, use the updateOne() method with the $set operator.
Q5 . Express.js is used in a web application to create server-side web applications and APIs, providing routing and middleware capability.
Q6 . const express = require('express'); 
const app = express(); 
app.listen(3000, () =>{
 console.log('Server running on port 3000');
})
Q7 . app.get('/hello', (req, res) =>{
 res.send('Hello, World!');
})
Q8 . React is used in web development to build user interfaces with reusable components, enabling efficient, dynamic, and interactive UI updates.
Q9 . State represents a component’s internal data that can change over time, while props are immutable values passed from parent to child components.
Q10 . const Welcome = () => <h1>Welcome to the MERN Stack!</h1>;
Q11 . To handle a button click event in a React component, define a function and pass it to the onClick() property of the button.
Q12 . Node.js is a runtime environment for executing JavaScript on the server side, differing from traditional web servers by its non-blocking, event-driven architecture.
Q13 . console.log('Hello, Node.js!');
Q14 . Use const moduleName = require('module'); to import and then use moduleName to access the module's functionality. example const express =require('express')
Q15 . const server = http.createServer((req, res) => {
 res.end('Hello, World!');
 }).listen(port);
Q16 . mongoose.connect('mongodb://localhost:27017/mern-app')
.then(() => {
    console.log('DB Connected!')
})
Q17 .1-> Install Express and run 
         2-> create Express app setup basic server
         3-> define route
       example : 
const express = require('express');
const app = express();
const port = 3000;

app.get('/api/hello', (req, res) => {
  res.json({ message: 'Hello, API!' });
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
Q18 . First install packages are need axios for fetch data from server express cors 
and here is the code  for server :
 const express = require('express');
const cors = require('cors');
const app = express();
const port = 5000;

// Middleware
app.use(cors());

// API endpoint
app.get('/api/message', (req, res) => {
  res.json({ message: 'Hello from the backend!' });
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
here is the code  for client :
import React, { useState, useEffect } from 'react';
import axios from 'axios';

function App() {
  const [message, setMessage] = useState('');

  useEffect(() => {
    axios.get('http://localhost:5000/api/message')
      .then(response => setMessage(response.data.message))
      .catch(error => console.error('Error fetching the message:', error));
  }, []);

  return (
    <div className="App">
      <h1>{message}</h1>
    </div>
  );
}

export default App;
Q19 . 1-> check server running on console
         2->check port
        3->check the method routes 
        4->check  middleware like body parse any blocks on console
        5->restart the server once again
        6-> check our code first
Q20 . 1->Organize your MERN stack project with clear directory structures
          2->use environment variables for sensitive data
          3-> implement proper error handling and security
