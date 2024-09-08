# Library Management System

## Overview

The Library Management System is a comprehensive web application built with Next.js for the frontend and Flask for the backend. It offers a user-friendly interface for managing a collection of books, featuring functionalities such as adding, editing, deleting, and searching for books. This system is designed to streamline library operations and enhance the user experience for both librarians and patrons.

## Features

- **Book Management:**
  - View a list of all books in the library
  - Add new books to the collection
  - Edit existing book information
  - Delete books from the library
- **Search and Filter:**
  - Search for books by title or author
  - Filter books by genre and availability
- **User-friendly Interface:** Responsive design for seamless use on desktop and mobile devices
- **RESTful API:** Well-structured API for easy integration and extensibility

## Technology Stack

- **Frontend:**
  - Next.js 13+ (React)
  - TypeScript
  - Tailwind CSS
  - shadcn/ui components
- **Backend:**
  - Flask (Python)
  - SQLite
- **API:** RESTful architecture

## Prerequisites

- Python 3.7+
- Node.js 14+
- npm or yarn

## Project Structure

```
library-management-system/
├── backend/
│   ├── app.py              # Main Flask application
│   ├── models.py           # Database models
│   ├── routes/             # API route handlers
│   ├── services/           # Business logic
│   ├── tests/              # Backend unit tests
│   └── requirements.txt    # Python dependencies
└── frontend/
    ├── src/
    │   ├── app/            # Next.js app directory
    │   ├── components/     # React components
    │   ├── lib/            # Utility functions
    │   └── types/          # TypeScript type definitions
    ├── public/             # Static assets
    ├── tests/              # Frontend unit and integration tests
    ├── .env.local          # Environment variables
    └── package.json        # Node.js dependencies
```

## Setup and Installation

### Backend Setup

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/library-management-system.git
   cd library-management-system
   ```

2. Set up the backend:
   ```
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```
   cd ../frontend
   ```

2. Install Next.js and its dependencies:
   ```
   npx create-next-app@latest .
   ```
   Choose the following options when prompted:
   - Would you like to use TypeScript? Yes
   - Would you like to use ESLint? Yes
   - Would you like to use Tailwind CSS? Yes
   - Would you like to use `src/` directory? Yes
   - Would you like to use App Router? Yes
   - Would you like to customize the default import alias? No

3. Install additional dependencies:
   ```
   npm install axios react-query
   ```

4. Install and set up shadcn/ui:
   ```
   npx shadcn-ui@latest init
   ```
   Choose the following options:
   - Would you like to use TypeScript (recommended)? Yes
   - Which style would you like to use? › Default
   - Which color would you like to use as base color? › Slate
   - Where is your global CSS file? › › src/app/globals.css
   - Do you want to use CSS variables for colors? › Yes
   - Where is your tailwind.config.js located? › tailwind.config.js
   - Configure the import alias for components: › @/components
   - Configure the import alias for utils: › @/lib/utils
   - Are you using React Server Components? › Yes
   - Write configuration to components.json. Proceed? › Yes

5. Install specific shadcn/ui components as needed:
   ```
   npx shadcn-ui@latest add button
   npx shadcn-ui@latest add input
   npx shadcn-ui@latest add table
   ```

6. Configure environment variables:
   - Copy `.env.example` to `.env.local` in the frontend directory
   - Update the variables as needed, especially the API_URL

## Running the Application

1. Start the backend server:
   ```
   cd backend
   flask run
   ```

2. In a new terminal, start the frontend development server:
   ```
   cd frontend
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:3000`

## API Endpoints

- `GET /api/books`: Fetch all books
- `POST /api/books`: Add a new book
- `GET /api/books/<id>`: Fetch a specific book
- `PUT /api/books/<id>`: Update a book
- `DELETE /api/books/<id>`: Delete a book
- `GET /api/books/search`: Search and filter books

For detailed API documentation, refer to the [API Documentation](API_DOCS.md) file.

## Testing

- Run backend tests:
  ```
  cd backend
  pytest
  ```
- Run frontend tests:
  ```
  cd frontend
  npm run test
  ```

## Contributing

We welcome contributions to improve the Library Management System! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

Please ensure your code adheres to our coding standards and includes appropriate tests.

## Troubleshooting

If you encounter any issues:

1. Ensure both backend and frontend servers are running
2. Check console logs for any error messages
3. Verify that the API URL in `.env.local` matches your backend server address
4. Clear browser cache and restart the application
5. If problems persist, please open an issue with detailed information about the error and steps to reproduce

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgements

- [Next.js Documentation](https://nextjs.org/docs)
- [Flask Documentation](https://flask.palletsprojects.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [shadcn/ui](https://ui.shadcn.com/)
- [SQLite](https://www.sqlite.org/index.html)

For any additional questions or support, please open an issue or contact the maintainers.