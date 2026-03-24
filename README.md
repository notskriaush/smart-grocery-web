🚀 Smart Grocery Basket

Full-stack web application that helps users optimize grocery shopping by comparing prices across stores and generating recipes based on selected products.

The project combines backend price analysis, user basket logic, authentication, and AI-powered recipe generation.

🎯 Problem

Grocery shopping is often inefficient:

Prices vary across stores
It is difficult to find the cheapest option for a full basket
Users often don’t know what to cook with the products they buy

This project solves these problems by:

comparing basket prices across stores
suggesting the cheapest store
generating recipes based on selected items
💡 Key Features
🛒 Smart Basket
Add products to a basket
Automatically calculate total cost across multiple stores
Identify the cheapest store for the entire basket
📊 Price Comparison
Backend calculates basket prices across stores
Supports overlapping product availability
Uses latest available pricing data
🔐 Authentication & User Profile
User login system
AI features are available only for authenticated users
Users can save generated recipes to their personal profile
Saved recipes can be accessed later
🍳 Recipe System
Predefined recipes with ingredient-to-product mapping
Each ingredient is linked to a real product from the database
Ability to add all recipe ingredients to basket in one click
🤖 AI Recipe Generation
Generate recipes dynamically based on basket contents
Uses OpenAI API
Returns structured recipes (ingredients + steps)
Integrated directly into the basket flow
🧠 AI Integration
Backend collects basket data
Sends request to AI service
Receives structured recipes
Returns them to frontend

This demonstrates:

API integration
prompt design
structured data handling
🛠️ Tech Stack
Backend
Java 21
Spring Boot
REST API
Maven
Database
PostgreSQL (Dockerized)
Frontend
Vue 3
Vite
Node.js
Infrastructure
Docker & Docker Compose
Environment configuration via .env
🧱 Project Structure
smart-grocery-web/
│
├── client/                # Frontend (Vue + Vite)
├── grocery-backend/       # Backend (Spring Boot)
│   ├── src/
│   ├── pom.xml
│   └── Dockerfile
│
├── docker-compose.yml
└── README.md
▶️ Live Demo

🔗 [Add your deployed link here]

⚠️ Note:
If the website has been inactive for ~15 minutes, the server may go to sleep.
Please wait 1–3 minutes for it to start again.

⚙️ How to Run Locally
Requirements
Docker Desktop
Git
Steps
git clone https://github.com/cherriesc/smart-grocery-web.git
cd smart-grocery-web
docker compose up --build

Backend will be available at:

http://localhost:8080

Start frontend:

cd client
npm install
npm run dev

Open:

http://localhost:5173
🔌 Backend API (Examples)
Get products
GET /products
Get stores
GET /stores
Compare basket
POST /basket/compare

Example:

{
  "items": [
    { "productId": 1, "quantity": 2 },
    { "productId": 2, "quantity": 1 }
  ]
}
🗄️ Database
PostgreSQL running in Docker
Database name: grocery
Seeded with sample product and store data
👨‍💻 My Role
Designed and implemented backend architecture
Developed REST API for:
products
stores
basket comparison
recipes
authentication
Implemented basket price calculation logic
Integrated OpenAI API for recipe generation
Designed database schema (PostgreSQL)
Configured Docker environment
👥 Team
Backend: You
Frontend: Team members (Vue, UI/UX, integration)
📸 Screenshots

(Add screenshots here)

📄 License

This project is intended for educational and demonstration purposes.
