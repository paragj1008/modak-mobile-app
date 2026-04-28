# Modak Mobile App

A comprehensive mobile application for MODAK that enables customers to create orders and provides full admin management capabilities. Built with React Native for mobile and Python (Flask) for backend.

## 🎯 Project Overview

The Modak Mobile App is a full-featured e-commerce platform that provides:
- **Customer Portal**: Browse products, manage cart, place orders, track shipments
- **Admin Dashboard**: Manage inventory, orders, payments, and customer relationships
- **Real-time Updates**: Order status tracking and notifications
- **Secure Payments**: Integrated payment gateway (Stripe/Razorpay)

## ✨ Features

### Customer Features
- 🔐 User Authentication (Email, Social Login)
- 🛍️ Product Catalog with Search & Filter
- 🛒 Shopping Cart Management
- 💳 Secure Checkout Process
- 📦 Order Tracking & History
- ⭐ Product Reviews & Ratings
- 📝 Order Management (Cancel, Return, Refund)

### Admin Features
- 📊 Sales Dashboard & Analytics
- 📋 Order Management & Status Updates
- 📦 Inventory Management
- 💰 Payment Processing & Refunds
- 👥 Customer Management
- 📈 Business Metrics & Reports

## 🛠️ Tech Stack

### Frontend (Mobile)
- **React Native** - Cross-platform mobile development
- **Expo** - Managed React Native framework
- **Redux** - State management
- **React Navigation** - Navigation library
- **React Native Paper** - UI components
- **Axios** - HTTP client

### Backend
- **Python 3.9+** - Server language
- **Flask** - Web framework
- **SQLAlchemy** - ORM
- **PostgreSQL** - Database
- **JWT** - Authentication
- **Redis** - Caching
- **Celery** - Async tasks

### Payment & Services
- **Stripe/Razorpay** - Payment gateway
- **Firebase** - Push notifications
- **SendGrid** - Email service

## 📁 Project Structure

```
modak-mobile-app/
├── mobile/                          # React Native application
│   ├── src/
│   │   ├── components/             # Reusable UI components
│   │   ├── screens/                # App screens
│   │   ├── navigation/             # Navigation configuration
│   │   ├── services/               # API & external services
│   │   ├── store/                  # Redux store
│   │   └── utils/                  # Utility functions
│   ├── assets/                     # Images, fonts, icons
│   └── package.json
│
├── backend/                         # Python Flask API
│   ├── app/
│   │   ├── models/                 # Database models
│   │   ├── routes/                 # API endpoints
│   │   ├── services/               # Business logic
│   │   ├── middleware/             # Auth, logging, etc
│   │   └── utils/                  # Helper functions
│   ├── tests/                      # Unit & integration tests
│   ├── migrations/                 # Database migrations
│   ├── config.py                   # Configuration
│   ├── requirements.txt            # Python dependencies
│   └── run.py                      # Entry point
│
├── docs/                           # Documentation
├── PROJECT_REQUIREMENTS.md         # Detailed requirements
├── ARCHITECTURE.md                 # System architecture
└── README.md                       # This file
```

## 🚀 Quick Start

### Prerequisites
- Node.js 14+ & npm
- Python 3.9+
- PostgreSQL 12+
- Git

### Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set environment variables
cp .env.example .env

# Run database migrations
python migrations.py

# Start server
python run.py
```

The backend will run on `http://localhost:5000`

### Mobile Setup

```bash
# Navigate to mobile directory
cd mobile

# Install dependencies
npm install

# Start Expo development server
npx expo start

# Scan QR code with Expo app on your phone
# Or press 'a' for Android emulator, 'i' for iOS simulator
```

## 📋 API Documentation

### Authentication Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/refresh-token` - Refresh JWT token
- `POST /api/auth/logout` - User logout

### Product Endpoints
- `GET /api/products` - Get all products
- `GET /api/products/{id}` - Get product details
- `GET /api/products/search?q=query` - Search products
- `GET /api/categories` - Get all categories

### Order Endpoints
- `POST /api/orders` - Create new order
- `GET /api/orders` - Get user's orders
- `GET /api/orders/{id}` - Get order details
- `PUT /api/orders/{id}/cancel` - Cancel order

### Admin Endpoints
- `GET /api/admin/orders` - Get all orders
- `PUT /api/admin/orders/{id}/status` - Update order status
- `POST /api/admin/products` - Add product
- `PUT /api/admin/products/{id}` - Update product
- `GET /api/admin/dashboard` - Dashboard metrics

## 🔒 Security Features

- JWT-based authentication
- Password hashing (bcrypt)
- SQL injection prevention
- CORS configuration
- Rate limiting
- Data encryption at rest
- PCI compliance for payments
- Two-factor authentication (Admin)

## 📱 Supported Platforms

- iOS 11+
- Android 5+

## 🧪 Testing

### Backend Tests
```bash
cd backend
pytest
```

### Mobile Tests
```bash
cd mobile
npm test
```

## 🚢 Deployment

### Backend Deployment
- Heroku, AWS, or DigitalOcean
- Docker containerization available

### Mobile Deployment
- iOS: Apple App Store
- Android: Google Play Store
- Expo for easy OTA updates

## 📚 Documentation

- [PROJECT_REQUIREMENTS.md](./PROJECT_REQUIREMENTS.md) - Detailed feature specifications
- [ARCHITECTURE.md](./ARCHITECTURE.md) - System design & architecture
- [CONTRIBUTING.md](./CONTRIBUTING.md) - Development guidelines

## 🤝 Contributing

We welcome contributions! Please read [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📝 Development Timeline

- **Phase 1 (Week 1-2)**: Setup & Authentication
- **Phase 2 (Week 3-4)**: Product Catalog & Cart
- **Phase 3 (Week 5-6)**: Orders & Checkout
- **Phase 4 (Week 7-8)**: Admin Features
- **Phase 5 (Week 9-10)**: Testing & Optimization

## 🐛 Known Issues

None currently. Check [Issues](https://github.com/paragj1008/modak-mobile-app/issues) for ongoing discussions.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support & Contact

- 📧 Email: support@modak.com
- 💬 Discussions: [GitHub Discussions](https://github.com/paragj1008/modak-mobile-app/discussions)
- 🐛 Report Issues: [GitHub Issues](https://github.com/paragj1008/modak-mobile-app/issues)

## 🙏 Acknowledgments

Built with ❤️ by the Modak Team

---

**Last Updated**: 2026-04-28 14:14:27
**Version**: 1.0.0