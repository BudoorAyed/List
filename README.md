NodeJS Notes App
A simple Node.js and Express.js application that allows users to create, update, delete, and search notes. The app supports Google OAuth authentication and uses MongoDB for data storage.

🚀 Features
•	User authentication with Google OAuth.
•	Create, edit, and delete notes.
•	Search functionality for finding notes.
•	Uses MongoDB for data storage.
•	EJS as the templating engine.
•	Session-based authentication.

📦 Installation
1.	Clone this repository:
2.	git clone https://github.com/yourusername/nodesjs_notes.git
cd nodesjs_notes
3.	Install dependencies:
npm install
4.	Create a .env file in the root directory and add the following:
5.	MONGODB_URI=your_mongodb_connection_string
6.	GOOGLE_CLIENT_ID=your_google_client_id
7.	GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:5000/google/callback
8.	Start the development server:
npm start

🔗 Routes
Authentication
Method	Route	Description
GET	/auth/google	Start Google OAuth authentication
GET	/google/callback	Handle Google OAuth callback
GET	/logout	Logout user

Notes (Dashboard)
Method	Route	Description
GET	/dashboard	View all notes
GET	/dashboard/item/:id	View a single note
POST	/dashboard/add	Add a new note
PUT	/dashboard/item/:id	Update an existing note
DELETE	/dashboard/item-delete/:id	Delete a note

Other Routes
Method	Route	Description
GET	/	Homepage
GET	/about	About page

📂 Project Structure
.
├── public/              # Static files (CSS, JS, images)
├── views/               # EJS templates
├── server/
│   ├── config/          # Database connection
│   ├── controllers/     # Route controllers
│   ├── middleware/      # Authentication middleware
│   ├── models/          # Mongoose models
│   ├── routes/          # Express routes
├── .env                 # Environment variables
├── app.js               # Main entry point
├── package.json         # Dependencies and scripts

🛠️ Built With
•	Node.js
•	Express.js
•	MongoDB + Mongoose
•	EJS (Templating Engine)
•	Google OAuth (passport-google-oauth20)
•	express-session
•	Method Override (for PUT/DELETE requests)

