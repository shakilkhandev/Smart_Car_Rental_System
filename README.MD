Smart Car Rental System
A complete Car Rental Management System built with Laravel, Vue.js, and Inertia.js. AutoFleetX offers a seamless experience for both customers and admins, streamlining every aspect of car rental operations.

📌 Features
🧑‍💼 Customer
Create Rental Requests: Choose a car, set rental duration, and submit your request. Confirmation emails are sent automatically.

Secure Authentication: Login and registration with access control.

Rental Tracking: Monitor rental status from your dashboard.

Profile Management: Update personal details anytime.



👨‍💻 Admin
Admin Login: Secure access (registration disabled).

Car Inventory Management: Add, edit, or remove cars.

Rental Oversight: View and update rental statuses.

Manual Rental Creation: Create rentals for customers directly.

Rental History Access: View complete rental logs.

🛠️ Tech Stack
Backend: Laravel

Frontend: Vue.js

Routing/Data: Inertia.js

Database: MySQL

Package Managers: Composer & npm

🚀 Installation Guide
Clone the Repository:   https://github.com/shakilkhandev/Smart_Car_Rental_System.git

bash
git clone 
cd car_rental
Set up Environment:

bash
cp .env.example .env
php artisan key:generate
Install Dependencies:

bash
composer install
npm install
Configure Database: Update .env with your DB credentials:

env
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
Build Frontend:

bash
npm run build
Start the App:

bash
php artisan serve
📄 Usage
Customers register and rent cars.

Admins manage inventory and rental statuses.

Users can update profiles and track rentals.

📊 Project Structure
├── app/          # Laravel Backend
├── resources/    # Vue.js Frontend
├── routes/       # Web Routes
└── database/     # Migrations
🤝 Contributions
Open to contributions! Submit a PR or raise an issue.

📧 Contact
For questions or feedback, reach out to: shakilkhanfv@gmail.com 