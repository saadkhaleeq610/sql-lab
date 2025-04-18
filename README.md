# SQL Interpreter

A full-stack application that allows users to write SQL queries, execute them against a Supabase PostgreSQL database, and view the results in a user-friendly interface.

![SQL Interpreter Screenshot](path/to/screenshot.png)

## Features

- **Interactive SQL Editor**: Write and execute SQL queries directly from the browser
- **Database Schema Browser**: View tables and columns in the sidebar for easy reference
- **Real-time Query Execution**: Send queries to a PostgreSQL database and view results instantly
- **Query History**: Keep track of past queries and their execution status
- **Query Validation**: Validate SQL syntax before execution
- **Beautiful Table Display**: View results in a well-formatted table with proper typing

## Tech Stack

### Frontend
- React.js with TypeScript
- CSS for styling

### Backend
- Go (Golang)
- Gin web framework
- Supabase for PostgreSQL database

## Installation

### Prerequisites
- Node.js and npm for frontend
- Go 1.19+ for backend
- Supabase account and project

### Frontend Setup

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/sql-interpreter.git
   cd sql-interpreter/frontend
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Run the development server
   ```bash
   npm run dev
   ```

### Backend Setup

1. Navigate to the backend directory
   ```bash
   cd ../backend
   ```

2. Create a `.env` file in the backend directory with your Supabase credentials:
   ```
   # Supabase Configuration
   SUPABASE_URL=your_supabase_url
   SUPABASE_KEY=your_supabase_anon_key

   # Server Configuration
   PORT=8080
   ```

3. Set up the required PostgreSQL functions in your Supabase project:
   - See the [Backend README](backend/README.md) for the SQL definitions of required functions

4. Install Go dependencies
   ```bash
   go mod download
   ```

5. Run the backend server
   ```bash
   go run main.go
   ```

## Usage

1. Open your browser and navigate to `http://localhost:5173` (or the port specified by Vite)
2. The left sidebar displays your database schema (tables and columns)
3. Write SQL queries in the editor in the main panel
4. Click "Execute" or press Ctrl+Enter to run your query
5. View the results in the table below the editor

## Project Structure

```
/
├── frontend/                # React frontend application
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── App.tsx          # Main application component
│   │   └── ...
│   ├── package.json         # Frontend dependencies
│   └── ...
│
└── backend/                 # Go backend application
    ├── handlers/            # HTTP request handlers
    ├── models/              # Data models
    ├── services/            # Business logic services
    ├── main.go              # Application entry point
    └── ...
```

## API Endpoints

The backend exposes the following API endpoints:

- `POST /api/query/execute` - Execute an SQL query
- `GET /api/query/schema` - Get database schema information
- `POST /api/query/validate` - Validate an SQL query
- `GET /api/query/history` - Get query execution history

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Supabase](https://supabase.io/) for the PostgreSQL database
- [Gin](https://github.com/gin-gonic/gin) for the Go web framework
- [React](https://reactjs.org/) for the frontend library
