# PulseVoltSolutionst10073671
iCE

INSY7314_ST10073671_ICE3
IceTask3
ST10073671
We are having  a simple Node.js + Express API connected to MongoDB Atlas.
We are showing how to connect to a cluster, seed sample data, and expose it through REST endpoints.
Our Features allow 
•	Connects to MongoDB Atlas with credentials stored in .env
•	Uses the Cluster0 database
•	Provides endpoints to:
•	 - GET / → Hello message
•	 - GET /test → Test endpoint
•	 - GET /api/orders → Fetch orders from MongoDB
•	 - POST /api/orders/seed → Seed the database with sample orders
The Environment Variables
Create a .env file in the project root:
ATLAS_URI="mongodb+srv://st10073671:Fred1999@cluster0.seqma9e.mongodb.net/?retryWrites=true&w=majority&authSource=admin&appName=Cluster0"
PORT=3000
DB_NAME=Cluster0
To  Run the App

We start the server node sserver.mjs
Server runs at : http://localhost:3000
Orders
GET /api/orders
Fetches all documents from the orders collection in the Cluster0 database.{
  "message": "Fruits",
  "orders": [
    { "_id": "65f...", "id": "1", "name": "Orange" },
    { "_id": "65f...", "id": "2", "name": "Apple" },
    { "_id": "65f...", "id": "3", "name": "Pear" }
  ]
}
Seed Orders
POST /api/orders/seed
Seeds the orders collection with Orange, Apple, and Pear if empty.
When the app exits, the MongoDB connection is closed gracefully via closeMongo() in db.js.

<img width="451" height="674" alt="image" src="https://github.com/user-attachments/assets/2c75db77-e30b-41cf-bce9-06fd6c4697e9" />

