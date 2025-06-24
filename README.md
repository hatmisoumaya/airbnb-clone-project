### Team Roles
🧑‍💻 Team Roles
This project is developed collaboratively by a cross-functional team, where each member contributes through a defined role. Below are the key roles and their responsibilities:

Frontend Developer
Responsibility: Designs and implements the user interface (UI) of the application using technologies like React.js or Next.js.

Key Tasks: Responsive layouts, integrating with backend APIs, ensuring accessibility and user experience.

Backend Developer
Responsibility: Builds and maintains the server-side logic, APIs, and handles business logic.

Key Tasks: API development, authentication, server-side rendering, performance optimization.

Database Administrator (DBA)
Responsibility: Designs, implements, and manages the database systems.

Key Tasks: Data modeling, indexing, optimization, backup, and recovery plans.

DevOps Engineer
Responsibility: Manages deployment pipelines, infrastructure, and CI/CD automation.

Key Tasks: Dockerization, server setup, version control, monitoring, and logging.

UI/UX Designer
Responsibility: Ensures the interface is user-friendly, intuitive, and visually appealing.

Key Tasks: Wireframes, prototypes, style guides, usability testing.

Project Manager (PM)
Responsibility: Oversees the project’s scope, timeline, and communication among team members.

Key Tasks: Planning sprints, tracking progress, managing risks, and coordinating tasks.

Quality Assurance (QA) Engineer
Responsibility: Verifies that the application is reliable and free of bugs.

Key Tasks: Writing and executing test cases, bug tracking, automated testing, and regression testing.

Security Specialist
Responsibility: Ensures the application is protected against threats and vulnerabilities.

Key Tasks: Threat modeling, penetration testing, secure coding practices.
### Technology Stack
This project uses a modern, scalable technology stack to replicate core functionalities of Airbnb. Below is a list of technologies used and their purposes:

Next.js
Purpose: A React framework used for building server-rendered and statically generated web applications. Enables performance optimizations, routing, and full-stack capabilities.

Tailwind CSS
Purpose: A utility-first CSS framework for rapidly building custom user interfaces with minimal CSS code.

TypeScript
Purpose: A strongly-typed language that builds on JavaScript, improving code quality and maintainability through static type checking.

Prisma
Purpose: A modern ORM (Object-Relational Mapping) tool for interacting with the PostgreSQL database in a type-safe and efficient manner.

PostgreSQL
Purpose: A powerful, open-source relational database system used to store application data like user accounts, listings, reservations, etc.

NextAuth.js
Purpose: A complete authentication solution for Next.js apps. Handles secure login, session management, and OAuth providers.

Cloudinary / UploadThing (or similar)
Purpose: Handles image uploads and media management for listing photos, user avatars, etc.

Zustand / Redux (optional)
Purpose: Lightweight state management libraries used to handle global application state like modals, filters, and user sessions.

React Hook Form + Zod
Purpose: Used together to manage complex forms (like listing creation) with validation and improved UX.

Vercel
Purpose: Cloud platform for hosting and deploying the Next.js frontend with fast global delivery.

### Database Design
The database schema is designed to capture the core functionality of an Airbnb-like platform. Below are the key entities, their important fields, and relationships:

User
Represents guests or hosts using the platform.

id – Unique identifier (UUID)

name – Full name of the user

email – User’s email (unique)

role – Indicates if the user is a host or guest

createdAt – Date of registration

🔗 Relationships:

A user can own many properties.

A user can make many bookings.

A user can write many reviews.

Property
Represents a place listed by a host.

id – Unique identifier

title – Name or title of the property

description – Details about the property

location – Address or coordinates

pricePerNight – Cost per night

🔗 Relationships:

A property is owned by one user.

A property can have many bookings.

A property can have many reviews.

Booking
Represents a reservation made by a guest.

id – Unique identifier

userId – The guest who made the booking

propertyId – The property being booked

startDate – Check-in date

endDate – Check-out date

🔗 Relationships:

A booking belongs to one user (guest).

A booking belongs to one property.

Review
Represents feedback left by a guest after a stay.

id – Unique identifier

rating – Numeric rating (e.g., 1–5 stars)

comment – Optional text review

userId – Reviewer

propertyId – Reviewed property

🔗 Relationships:

A review is written by one user.

A review is about one property.

Payment
Represents a payment made for a booking.

id – Unique identifier

bookingId – Linked booking

amount – Total amount paid

paymentMethod – e.g., card, PayPal

status – e.g., completed, pending

🔗 Relationships:

A payment belongs to one booking.

