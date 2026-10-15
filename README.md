# SwiftBasket V1

A full-stack e-commerce web application built with **Node.js, Express, EJS, MongoDB, and Mongoose**. SwiftBasket V1 is the first release of the project, focused on essential shopping experiences, session-based authentication, product management, and administrative functionality.

> **Version:** 1.0.0
> **Status:** MVP Completed
> **Project Type:** Full-Stack Web Application
> **Primary Purpose:** Learning, portfolio development, and establishing a foundation for future releases.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Application Architecture](#application-architecture)
- [Getting Started](#getting-started)
- [Environment Configuration](#environment-configuration)
- [Authentication](#authentication)
- [Admin Dashboard](#admin-dashboard)
- [Current Limitations](#current-limitations)
- [Roadmap](#roadmap)
- [Version History](#version-history)
- [Contributing](#contributing)
- [License](#license)

## Overview

SwiftBasket is a full-stack e-commerce web application designed to provide a foundation for online shopping and product administration.

Version 1 focuses on the core functionality required for an e-commerce application, including product listings, product details, user authentication, responsive interfaces, product management, and an admin dashboard.

The application uses server-side rendering with EJS, Express for server-side application logic, and MongoDB for data storage through Mongoose.

SwiftBasket V1 establishes the initial application structure while leaving room for future improvements, including token-based authentication, shopping cart functionality, order processing, user profiles, and payment integration.

### Project Objectives

- Build a functional full-stack web application.
- Implement server-side rendering using EJS.
- Manage application data using MongoDB and Mongoose.
- Implement session-based user authentication.
- Provide product management and administrative functionality.
- Establish a foundation for future e-commerce features.

## Features

### Implemented in V1

The following features are part of the completed MVP.

- **Product Listing:** Display available products in the application.
- **Product Details:** Provide individual product detail views.
- **User Authentication:** Support email/password authentication using sessions.
- **Responsive Design:** Build an interface intended to work across different screen sizes.
- **Product Management:** Provide functionality for managing products.
- **Admin Dashboard:** Provide an administrative interface for application management.

*Note: The exact behavior, permissions, validation rules, and implementation details depend on the current codebase.*

### Planned for V2

The following features are planned for a future release and are not presented as implemented functionality.

- **JWT Authentication:** Introduce token-based authentication to replace or evolve the current session-based approach.
- **Shopping Cart:** Allow users to add products to a cart and manage quantities.
- **Buy / Checkout:** Introduce a purchasing flow for selected products.
- **User Profile:** Allow users to manage their profile information.
- **Payment Integration:** Add an online payment workflow.
- **Additional E-commerce Features:** Expand the application with further shopping and account-management functionality.

## Technology Stack

| Technology                   | Purpose                                 |
| ---------------------------- | --------------------------------------- |
| Node.js                      | JavaScript runtime for the backend      |
| Express.js                   | Web framework and request handling      |
| EJS                          | Server-side HTML templating             |
| MongoDB                      | NoSQL database                          |
| Mongoose                     | MongoDB object modeling                 |
| Session-based authentication | Maintaining authenticated user sessions |
| HTML and CSS                 | Web page structure and styling          |

The frontend is rendered using EJS templates rather than a separate React-based frontend.

## Application Architecture

SwiftBasket V1 follows a server-rendered web application architecture.

```text
User's Browser
      |
      | HTTP Requests
      v
Express.js Server
      |
      +---- Authentication & Sessions
      |
      +---- Application Routes
      |
      +---- Controllers / Business Logic
      |
      +---- EJS Templates
      |
      v
Mongoose
      |
      v
MongoDB Database
```

### How It Works

1. A user visits the application through a web browser.
2. Express receives the incoming HTTP request and routes it to the appropriate handler.
3. The application performs the required operations, including database access when necessary.
4. Mongoose communicates with MongoDB to read or modify application data.
5. Express renders the appropriate EJS template and returns the resulting HTML to the browser.
6. For authenticated requests, the application uses its session-based authentication mechanism.

This architecture keeps the initial application relatively straightforward while providing a foundation for future enhancements.

## Getting Started

### Prerequisites

Before setting up the project, ensure that the following tools are available:

- [Node.js](https://nodejs.org/)
- npm, which is included with Node.js
- [MongoDB](https://www.mongodb.com/) or an accessible MongoDB deployment
- Git, if cloning the project from a repository

### Installation

#### 1. Clone the repository

Replace the placeholder URL with your actual repository URL.

```bash
git clone https://github.com/Echo-Nexus/swiftbasket.git
```

#### 2. Navigate to the project directory

```bash
cd SwiftBasket
```

Use the actual directory name if it differs.

#### 3. Install dependencies

```bash
npm install
```

#### 4. Configure environment variables

Create a `.env` file in the project root if your application uses environment variables. See the configuration section below.

#### 5. Start the application

Use the development or production command defined in your `package.json`. For example, if the corresponding scripts exist:

```bash
npm run dev
```

or:

```bash
npm start
```

These commands are examples, not confirmed scripts for the current codebase. Check `package.json` for the actual available commands.

#### 6. Open the application

Visit the local address and port configured by your application. The exact URL depends on your server configuration.

## Environment Configuration

The application may require environment variables for database connectivity, session management, and server configuration.

An illustrative `.env` file might look like this:

```env
PORT=3000
MONGODB_URI=mongodb://127.0.0.1:27017/swiftbasket
SESSION_SECRET=replace_with_a_long_random_secret
```

**Important:** These are example variable names and values, not verified names from the current implementation. Use the exact names expected by your application code and configuration.

### Environment Variable Guidelines

- Keep database connection strings out of source code.
- Use a strong, unpredictable session secret.
- Never commit your real `.env` file or production credentials.
- Add `.env` to `.gitignore`.
- Provide a sanitized `.env.example` file for other developers when appropriate.

Example `.gitignore` entries:

```gitignore
node_modules/
.env
```

Keep any existing project-specific ignore rules as well.

## Authentication

SwiftBasket V1 uses **email/password authentication with server-side sessions**.

The session-based approach allows the application to maintain authentication state across requests. This is the authentication strategy for the current release.

### Planned Authentication Improvements

SwiftBasket V2 is intended to introduce JWT-based authentication.

The migration should consider:

- Token generation and verification.
- Token expiration and refresh strategy, if required.
- Secure token storage and transmission.
- Authentication middleware and protected routes.
- Authorization and role checks.
- Logout and token invalidation behavior.

JWT is an authentication mechanism, not a complete replacement for every aspect of session management. The final implementation should be selected based on the application's security and deployment requirements.

## Admin Dashboard

The V1 application includes an admin dashboard and product management functionality.

These capabilities establish the administrative foundation of SwiftBasket. More advanced management tools and additional workflows can be introduced in future releases.

Administrative routes and operations should be protected by appropriate authorization checks to prevent unauthorized access.

## Current Limitations

SwiftBasket V1 is an MVP and does not yet include every feature expected from a complete online shopping platform.

The following functionality is planned rather than implemented:

- Shopping cart management.
- Complete checkout and purchasing workflows.
- User profile management.
- Online payment integration.
- JWT-based authentication.

The current version should therefore be understood as the foundation of the application rather than a fully featured commercial e-commerce platform.

## Roadmap

### V1 — Core MVP

- [x] Product listing and details.
- [x] Email/password authentication with sessions.
- [x] Responsive interface.
- [x] Product management.
- [x] Admin dashboard.

### V2 — E-commerce Expansion

- [ ] JWT authentication.
- [ ] Shopping cart.
- [ ] Buy and checkout workflow.
- [ ] User profile management.
- [ ] Payment integration.
- [ ] Additional e-commerce features.

The roadmap is a statement of intended development, not a guarantee that every feature will ship in the next release.

## Version History

### V1.0.0 — Initial MVP

The first version establishes the core SwiftBasket application, including product browsing, session-based authentication, responsive pages, product management, and an admin dashboard.

Future releases will build on this foundation by introducing more complete shopping and account-management workflows.

## Contributing

SwiftBasket is a portfolio and learning project. Suggestions, bug reports, and constructive feedback are welcome.

If you want to contribute:

1. Fork the repository.
2. Create a branch for your changes.
3. Implement and test your changes.
4. Submit a pull request with a clear description of the work.

Please ensure that credentials and other sensitive configuration values are not included in commits.

## License

No license has been specified for this project yet.

Until a license is added to the repository, do not assume that the source code is available for unrestricted reuse, modification, or redistribution.

---

**SwiftBasket V1** — A foundation for building a more complete e-commerce experience.
