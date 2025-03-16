# **Blog API and Web App**

A full-stack blog application that allows users to create, edit, view, and delete blog posts. The application consists of a front-end for user interactions, a back-end API for data management, and a connected in-memory or database-driven data store.

---

## **Features**
- **Dynamic Blog Management**:
  - Create, edit, and delete blog posts via an intuitive interface.
- **RESTful API**:
  - Supports CRUD operations for posts: Create, Read, Update, and Delete.
- **Real-Time Updates**:
  - Front-end dynamically fetches blog posts using the back-end API.
- **Responsive Design**:
  - Optimized for both desktop and mobile devices.
- **Seamless Integration**:
  - Combines a front-end client, back-end server, and API layer for smooth functionality.

---

## **Technologies Used**
- **Node.js**: Backend runtime for server-side development.
- **Express.js**: Framework for building RESTful APIs and routing.
- **Axios**: For making HTTP requests between the backend and API.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic HTML in the front-end.
- **CSS**: Custom styles for the front-end interface.
- **body-parser**: Middleware for parsing form data.
- **In-Memory Data Store**: Stores blog posts for demonstration purposes.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: Installed on your local machine.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/Blog-API-WebApp.git
   cd Blog-API-WebApp
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the API server:
   ```bash
   node index.js
   ```
   The API will run at:
   ```plaintext
   http://localhost:4000
   ```

4. Start the front-end server:
   ```bash
   node server.js
   ```
   The front-end server will run at:
   ```plaintext
   http://localhost:3000
   ```

---

## **API Endpoints**
### **Base URL**: `http://localhost:4000`

| HTTP Method | Endpoint        | Description                            |
|-------------|-----------------|----------------------------------------|
| **GET**     | `/posts`        | Fetch all blog posts.                  |
| **GET**     | `/posts/:id`    | Fetch a specific blog post by ID.      |
| **POST**    | `/posts`        | Create a new blog post.                |
| **PATCH**   | `/posts/:id`    | Update specific fields of a blog post. |
| **DELETE**  | `/posts/:id`    | Delete a blog post by ID.              |

---

## **Usage**

### **Front-End Features**:
1. **View All Posts**:
   - Displays all posts fetched from the back-end API.
2. **Create New Post**:
   - Use the "New Post" button to navigate to the post creation form.
3. **Edit Post**:
   - Click "Edit" on a blog post to modify its content.
4. **Delete Post**:
   - Click "Delete" on a blog post to remove it permanently.

### **Back-End API**:
- Acts as a bridge between the client-side and the in-memory database.
- Supports all CRUD operations as described in the API Endpoints section.

---

## **File Structure**
### **Backend (server.js)**:
- **Routes**:
  - `/`: Fetches all posts and displays them.
  - `/new`: Renders the "New Post" creation page.
  - `/edit/:id`: Renders the post editing page for a specific ID.
  - `/api/posts`: Handles creating, updating, and deleting posts.
- **Communication**:
  - Makes API calls to the back-end via Axios to handle data operations.

### **API Server (index.js)**:
- **In-Memory Data Store**:
  - Stores and manages blog post data for demonstration purposes.
- **Endpoints**:
  - Implements endpoints for fetching, creating, updating, and deleting posts.

### **Front-End**:
1. **index.ejs**:
   - Displays all blog posts in a list with options to edit or delete.
2. **modify.ejs**:
   - Contains forms for creating or editing blog posts.

---

## **Database Structure (In-Memory)**

| Field Name   | Data Type | Description                          |
|--------------|-----------|--------------------------------------|
| **id**       | INTEGER   | Unique identifier for each post.    |
| **title**    | TEXT      | Title of the blog post.             |
| **content**  | TEXT      | Main content of the blog post.      |
| **author**   | TEXT      | Name of the author.                 |
| **date**     | TIMESTAMP | Timestamp when the post was created.|

---

## **Demo Workflow**
1. **Homepage** (`http://localhost:3000`):
   - Displays the list of blog posts.
   - Options to create, edit, or delete posts.
2. **New Post** (`http://localhost:3000/new`):
   - Form to add a new blog post.
3. **Edit Post** (`http://localhost:3000/edit/:id`):
   - Form to edit an existing blog post.

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Inspired by the need for a simple blog management tool.
- Thanks to open-source frameworks and tools for making this project possible.
