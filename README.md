21 Savage Demo App

A full-stack web application dedicated to 21 Savage, featuring an interactive community message board powered by Node.js, Express, and the native MongoDB driver, complete with upvoting, downvoting, and full CRUD functionality.

Live Demo
Render Deployment: savage-demo-qi33.onrender.com


<img width="1341" height="673" alt="Screenshot 2026-10-29 at 1 46 54 AM" src="https://github.com/user-attachments/assets/e0ae9008-8e7b-433c-bc31-941fd652b96f" />


Features
Interactive Message Board: Post messages, thoughts, and fan comments directly to the community feed.

Dynamic Voting System: Upvote or downvote messages with counters stored and updated in real time.

Full CRUD Capabilities: Seamlessly create, read, update, and delete entries via asynchronous client-server communication.

Native MongoDB Driver: Direct database integration connecting via MongoClient and URI configuration.

Server-Side Rendering: Utilizes EJS (Embedded JavaScript) templating to dynamically render messages sorted by database queries.

Routes & Endpoints
GET/ — Renders the main application dashboard and loads sorted messages from MongoDB.

POST/messages — Submits a new message document to the database.

PUT /messages — Increments the upvote count for a specific message.

PUT /down — Decrements the vote count for a specific message.

DELETE /messages — Removes a message document from the database.

How It Works
Database Connection: The application connects directly to MongoDB using the native Node.js driver (MongoClient) upon server startup.

Client Interaction: Frontend scripts capture user actions (submitting messages, clicking thumbs up/down, or deleting items) and send asynchronous requests to the Express server.

Persistence: Express routes handle incoming payloads, executing database queries (insertOne, findOneAndUpdate, findOneAndDelete) to update records and refresh the UI.

How to Set Up
Prerequisites Node.js installed on your machine

A MongoDB database connection URI

Installation Commands Clone the repository: git clone https://github.com/your-username/your-repo-name.git

Navigate into the project folder: cd your-repo-name

Install dependencies:
npm install

Configure Connection: Update the MongoDB connection string (URL) in your server file or environment configuration to match your database cluster.

Run the application: npm start

The server will start on http://localhost:3000 (or your configured port).

Built With
Node.js

Express.js

MongoDB

EJS

HTML5 & CSS3 image
