🚗 FLEMAN - Fleet Management System
Project Information
Project Name: FLEMAN (Fleet Management System)
Project Type: Full Stack Web Application
Status: Active Development ✅

👨‍💼 Project Author
DetailInformationNameSujal SawalkarRoll Number75BatchA4BranchComputer TechnologyRegistration Number23070627

📋 Project Overview
FLEMAN is a comprehensive web-based Fleet Management System designed to digitize and optimize vehicle rental and fleet operations. It provides a centralized platform for managing vehicle inventory, streamlining booking operations, automating billing processes, and delivering an exceptional user experience for both customers and administrators.
Problem Statement
Traditional fleet management operations are hindered by:

Manual vehicle tracking and availability management
Paper-based booking systems leading to double bookings
Time-consuming invoice generation prone to errors
Lack of centralized communication and real-time visibility
Poor customer experience without dedicated online platform
Scattered data and inefficient staff workflows

Solution
FLEMAN solves these challenges with an integrated digital ecosystem that automates vehicle operations, provides real-time inventory management, streamlines booking processes, and ensures accurate billing.

✨ Key Features
👥 For Customers

✅ User registration and secure authentication with JWT
✅ Browse available vehicles with detailed specifications and filters
✅ Multi-step booking workflow with location and date selection
✅ Add-on services selection (GPS, Insurance, Child Seat, etc.)
✅ Real-time booking confirmation with instant invoice generation
✅ View complete booking history and manage reservations
✅ Modify or cancel bookings (up to 24 hours before pickup)
✅ Download invoices in PDF format

👨‍💼 For Staff/Coordinators

✅ Real-time vehicle inventory management and tracking
✅ Live availability monitoring across multiple locations
✅ Comprehensive booking management and status updates
✅ Customer management and communication tools
✅ Invoice generation and billing management
✅ Location/hub management and configuration
✅ Staff dashboard with key performance metrics
✅ Generate reports for audits and analysis

🔧 For Administrators

✅ Complete system configuration and user management
✅ Role-based access control (Admin, Agent, Staff, Customer)
✅ Multi-location hub management
✅ Dynamic pricing model configuration
✅ Add-on service and rate management
✅ Comprehensive system analytics and reporting
✅ User activity monitoring and audit logs


🛠️ Technology Stack
Backend

Language: Java 11+
Framework: Spring Boot 2.x
ORM: Spring Data JPA with Hibernate
Security: Spring Security with JWT (JSON Web Tokens)
Database: MySQL 8.0+
Build Tool: Apache Maven

Frontend (Customer Portal)

Framework: Next.js 13+
Library: React 18+
Styling: Tailwind CSS
Language: JavaScript (ES6+)
State Management: React Hooks

Frontend (Staff Dashboard)

Framework: Next.js 13+
Library: React 18+
Styling: Tailwind CSS
Language: JavaScript (ES6+)

Additional Tools

Version Control: Git & GitHub
API Architecture: RESTful Web Services
Authentication: JWT Tokens
Database Connection Pool: HikariCP


📁 Project Structure
FLEMAN/
├── FlemanFrontEnd/
│   ├── User/
│   │   └── fleeman_next/              # Customer Portal (Next.js)
│   │       ├── app/                   # Pages and routes
│   │       ├── public/                # Static assets
│   │       ├── package.json           # Dependencies
│   │       └── next.config.js         # Next.js configuration
│   │
│   └── Staff/
│       └── FleetFrontEndUpdate/       # Staff Dashboard (Next.js)
│           ├── app/                   # Pages and routes
│           ├── public/                # Static assets
│           ├── package.json           # Dependencies
│           └── next.config.js         # Next.js configuration
│
├── FlemanWithJava/                     # Backend (Spring Boot)
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/
│   │   │   │   ├── controller/        # REST Controllers (12+ classes)
│   │   │   │   ├── service/           # Business Logic (20+ classes)
│   │   │   │   ├── repository/        # Data Access (12+ repositories)
│   │   │   │   ├── models/            # Entity Classes (15+ models)
│   │   │   │   ├── dto/               # Data Transfer Objects (15+ DTOs)
│   │   │   │   ├── utils/             # Utility Classes
│   │   │   │   └── security/          # Security Configuration
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/                      # Unit Tests
│   ├── pom.xml                        # Maven Dependencies
│   ├── mvnw & mvnw.cmd               # Maven Wrapper
│   └── README.md                      # Backend Documentation
│
└── README.md                          # This file

🚀 Getting Started
Prerequisites

Java 11 or higher
Node.js 16+ and npm
MySQL 8.0+
Git

Installation & Setup
1. Clone Repository
bashgit clone https://github.com/Sujal-Sawalkar/FLEMAN.git
cd FLEMAN
2. Backend Setup (Spring Boot)
bashcd FlemanWithJava

# Install dependencies
mvn clean install

# Configure database
# Update src/main/resources/application.properties with your MySQL credentials
# spring.datasource.url=jdbc:mysql://localhost:3306/fleman_db
# spring.datasource.username=root
# spring.datasource.password=your_password

# Run application
mvn spring-boot:run

# Backend runs on: http://localhost:8080
3. Frontend - Customer Portal Setup
bashcd FlemanFrontEnd/User/fleeman_next

# Install dependencies
npm install

# Run development server
npm run dev

# Portal runs on: http://localhost:3000
4. Frontend - Staff Dashboard Setup
bashcd FlemanFrontEnd/Staff/FleetFrontEndUpdate

# Install dependencies
npm install

# Run development server
npm run dev

# Dashboard runs on: http://localhost:3001

📊 Database Schema
The system uses MySQL with 15+ normalized tables:
Core Entities:

MemberDetails - Customer/User information
AuthenticationTable - Login credentials
AuthRoles - Role definitions
VehicleDetails - Vehicle information
CarDetails - Car-specific details
BookingDetails - Booking records
BookingConfirmationDetails - Booking confirmations
AddonDetails - Additional services
AddonBook - Add-on service bookings
InvoiceHeaderTable - Billing records
LocationDetails - Pickup/return locations
CityDetails - City information
StateDetails - State information
AgentDetails - Agent/staff information
PaymentDetails - Payment records


🔐 Security Features

JWT Authentication: Stateless authentication with secure token generation
Role-Based Access Control: Different permission levels for Admin, Agent, Staff, and Customer
Password Encryption: Industry-standard encryption for password storage
HTTPS/TLS: Secure communication (to be implemented in production)
Input Validation: Prevents SQL injection and XSS attacks
CORS Configuration: Properly configured cross-origin resource sharing
Audit Logging: Comprehensive logging of user actions


📚 API Documentation
Authentication Endpoints
POST /api/auth/register          # User registration
POST /api/auth/login             # User authentication
POST /api/auth/logout            # Session termination
POST /api/auth/refresh-token     # Token refresh
Vehicle Endpoints
GET  /api/vehicles               # List all vehicles
GET  /api/vehicles/{id}          # Get vehicle details
POST /api/vehicles               # Create vehicle (Admin only)
PUT  /api/vehicles/{id}          # Update vehicle
Booking Endpoints
POST /api/bookings               # Create booking
GET  /api/bookings/{id}          # Get booking details
GET  /api/bookings/customer/{id} # Customer bookings
PUT  /api/bookings/{id}          # Modify booking
DELETE /api/bookings/{id}        # Cancel booking
Invoice Endpoints
GET  /api/invoices/{id}          # Get invoice
POST /api/invoices               # Generate invoice
GET  /api/invoices/booking/{id}  # Invoice by booking
Location Endpoints
GET  /api/locations              # List locations
POST /api/locations              # Create location (Admin)
For detailed API documentation, see FlemanWithJava/README.md

🧪 Testing
Backend Testing
bashcd FlemanWithJava
mvn test                          # Run unit tests
Frontend Testing
bashcd FlemanFrontEnd/User/fleeman_next
npm test                          # Run component tests

📈 Performance Metrics

Expected API Response Time: < 200ms
Expected Page Load Time: < 2 seconds
Database Query Time: < 100ms
Concurrent Users: 1000+
Code Coverage Target: 70%+


🔄 Basic Procedure Steps
Customer - Book Vehicle (8 Steps)

Login to customer portal
Click "Make Booking"
Select pickup location & date
Select return date & location
Choose vehicle from list
Add optional services
Review & confirm booking
Complete payment

Staff - Generate Invoice (4 Steps)

Go to "Invoices" section
Select completed booking
Click "Generate Invoice"
Invoice sent to customer email

Admin - Add Vehicle (5 Steps)

Login to admin panel
Go to "Vehicle Management"
Click "Add New Vehicle"
Enter: Make, Model, Year, License Plate, Type, Rate
Save vehicle


🚀 Deployment
Local Development
bash# Backend: http://localhost:8080
# Customer Portal: http://localhost:3000
# Staff Dashboard: http://localhost:3001
# Database: localhost:3306 (MySQL)
Production Deployment Options

Cloud Platforms: AWS (EC2, RDS), Azure, Google Cloud
Container Deployment: Docker & Kubernetes
PaaS Solutions: Heroku, Railway, Render
Traditional Hosting: VPS or Dedicated Servers


📊 System Architecture
┌─────────────────────────────────────────┐
│      PRESENTATION LAYER (Frontend)     │
│  Customer Portal | Staff Dashboard     │
│     (Next.js + React + Tailwind)       │
└──────────────────┬──────────────────────┘
                   │
        ┌──────────┴──────────┐
        │   REST API Layer    │
        │   (Spring Boot)     │
        └──────────┬──────────┘
                   │
┌──────────────────┴──────────────────┐
│   BUSINESS LOGIC LAYER (Services)  │
│  Vehicle | Booking | Invoice       │
│  Location | User Management        │
└──────────────────┬──────────────────┘
                   │
┌──────────────────┴──────────────────┐
│   DATA ACCESS LAYER (Repositories) │
│        Spring Data JPA             │
└──────────────────┬──────────────────┘
                   │
┌──────────────────┴──────────────────┐
│      DATABASE LAYER (MySQL)        │
│  15+ Normalized Tables             │
│  ACID Compliance                   │
└────────────────────────────────────┘

📝 Documentation

Backend Documentation: FlemanWithJava/README.md
Customer Portal Docs: FlemanFrontEnd/User/fleeman_next/README.md
Staff Dashboard Docs: FlemanFrontEnd/Staff/FleetFrontEndUpdate/README.md
API Documentation: Available in backend README
Database Schema: See Database Schema section above


🤝 Contributing
This is an academic project. For contributions, please:

Fork the repository
Create a feature branch (git checkout -b feature/AmazingFeature)
Commit changes (git commit -m 'Add AmazingFeature')
Push to branch (git push origin feature/AmazingFeature)
Open a Pull Request


📋 Requirements Met
✅ Full Stack Java Application - Spring Boot backend + Next.js frontend
✅ Database Integration - MySQL with proper normalization
✅ REST API - 30+ endpoints for all operations
✅ Authentication & Authorization - JWT-based with role-based access
✅ User Roles - Admin, Agent, Staff, Customer
✅ Multi-module Frontend - Customer portal + Staff dashboard
✅ Real-time Operations - Vehicle availability, booking management
✅ Automated Billing - Invoice generation and rate calculation
✅ GitHub Repository - Public repository with version control
✅ Documentation - Comprehensive README and code comments

🐛 Known Issues & Future Enhancements
Current Limitations

Payment gateway integration pending
Mobile application not yet developed
SMS notification system to be implemented

Planned Enhancements

Mobile application (React Native)
Payment gateway integration (Stripe/PayPal)
SMS/Email notifications
AI-based dynamic pricing
GPS vehicle tracking
Microservices migration


📞 Support & Contact
Project Author: Sujal Sawalkar
Registration Number: 23070627
GitHub: Sujal-Sawalkar
Email: sujal.sawalkar@example.com
For issues, questions, or suggestions, please open an issue on GitHub.

📄 License
This project is created for academic purposes as part of the Computer Technology program (Batch A4, 2024).

🙏 Acknowledgments

Spring Boot Framework
Next.js & React Community
MySQL Database
Tailwind CSS
GitHub for version control
Academic Institution and Mentors


Last Updated: December 2024
Project Version: 1.0
Status: Active Development ✅

This Fleet Management System demonstrates modern full-stack development practices combining Java backend architecture with responsive frontend design, providing a complete solution for fleet operations management.
