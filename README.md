# E-Commerce API Structure

## Overview
This document provides an overview of the structure of the e-commerce platform for sports-related products. The platform allows users to browse, purchase, and review sports-related products while providing an administrative dashboard for managing products, orders, and users.

## Features
### For Customers
- Browse and search sports-related products by category, subcategory, and group.
- Add items to the shopping cart and place orders.
- Make secure payments using integrated payment gateways.
- Leave reviews and ratings for purchased items.
- Receive notifications about order status and promotions.

### For Admins
- Manage products, categories, and subcategories.
- Process and track customer orders.
- Manage users and their roles.
- View reports and analytics.

## Technologies Used
- **Backend**: Node.js with Express.js
- **Database**: MongoDB (Mongoose ODM)
- **Authentication**: JSON Web Token (JWT), bcrypt for password hashing
- **Payments**: Integration with payment gateways (e.g., Stripe, PayPal)
- **File Storage**: Cloudinary for image uploads
- **Internationalization**: i18next for multi-language support
- **Email Service**: Nodemailer for transactional emails
- **Security**: Helmet, CORS, Rate Limiting

## Project Structure
```
.
├── app.js
├── controllers
│   ├── adminController.js
│   ├── authControllers.js
│   ├── categoryControllers.js
│   ├── currencyControllers.js
│   ├── errorControllers.js
│   ├── groupControllers.js
│   ├── homePagePhotoController.js
│   ├── itemControllers.js
│   ├── notificationControllers.js
│   ├── orderControllers.js
│   ├── paymentController.js
│   ├── reviewController.js
│   ├── shoppingCartControllers.js
│   ├── staticReviewController.js
│   ├── subcategoryControllers.js
│   ├── userControllers.js
│   └── wellknownController.js
├── dbConnect.js
├── i18nConfig.js
├── loop.js
├── models
│   ├── Category.js
│   ├── Currency.js
│   ├── Group.js
│   ├── HomePagePhoto.js
│   ├── Item.js
│   ├── locales
│   │   ├── ar.json
│   │   └── en.json
│   ├── Notification.js
│   ├── Order.js
│   ├── Review.js
│   ├── ShoppingCart.js
│   ├── StatikReviews.js
│   ├── Subcategory.js
│   └── User.js
├── public
│   └── html
│       └── email-verified.html
├── routes
│   ├── adminRoutes.js
│   ├── categoryRoutes.js
│   ├── currencyRoutes.js
│   ├── groupRoutes.js
│   ├── homePagePhotoRoutes.js
│   ├── itemRoutes.js
│   ├── mostSoldNewest.js
│   ├── orderRoutes.js
│   ├── paymentRoutes.js
│   ├── reviewRoutes.js
│   ├── shoppingCartRoutes.js
│   ├── steticReviewRoutes.js
│   ├── userRoutes.js
│   └── wellknown.js
├── server.js
├── utils
│   ├── ApiFeatures.js
│   ├── appError.js
│   ├── catchAsync.js
│   ├── checkItem.js
│   ├── countries.js
│   ├── createAdminOrderNotification.js
│   ├── createnotificationEmail.js
│   ├── createOrderCompletionEmail.js
│   ├── dummyData
│   │   ├── Category.json
│   │   ├── Group.json
│   │   ├── insertDeletData.js
│   │   ├── Item.json
│   │   └── Subcategory.json
│   ├── getExchangeRate.js
│   ├── logo.png
│   ├── mailer.js
│   ├── receipt.js
│   ├── sendEmail.js
│   ├── sendNotification.js
│   ├── sendResetPassword.js
└── README.md
```

## API Endpoints
### Authentication
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - User login
- `POST /api/auth/forgot-password` - Send password reset link
- `POST /api/auth/reset-password` - Reset user password

### Product Management
- `GET /api/items` - Get all products
- `POST /api/items` - Add a new product (Admin only)
- `PUT /api/items/:id` - Update a product (Admin only)
- `DELETE /api/items/:id` - Delete a product (Admin only)

### Order Management
- `POST /api/orders` - Create a new order
- `GET /api/orders/:id` - Get order details
- `PUT /api/orders/:id/status` - Update order status (Admin only)

### User Management
- `GET /api/users` - Get all users (Admin only)
- `GET /api/users/:id` - Get user details
- `DELETE /api/users/:id` - Delete user (Admin only)

### Review Management
- `POST /api/reviews` - Submit a product review
- `GET /api/reviews/:id` - Get reviews for a product

## Special Thanks
A special thanks to all contributors and developers who have helped in building and improving this e-commerce platform.

## License
This project is licensed under the ISC License.

## Contact
For inquiries or support, reach out to [youssef22772002salah@gmail.com].

