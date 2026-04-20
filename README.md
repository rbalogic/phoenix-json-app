# Phoenix JSON App

A full-stack web application demonstrating seamless integration between a **Phoenix** (Elixir) backend and a **React** frontend, communicating via JSON APIs.

## Overview

This project showcases modern full-stack web development practices by combining the robustness of Phoenix with the interactivity of React. The application features a RESTful JSON API backend built with Phoenix that serves a dynamic React frontend.

## Features

- 🎯 RESTful JSON API built with Phoenix
- ⚛️ React frontend with component-based architecture
- 🔄 Seamless client-server communication
- 📦 Modular and maintainable code structure
- 🚀 Production-ready setup

## Tech Stack

### Backend
- **Elixir** - Functional programming language
- **Phoenix** - Web framework
- **JSON API** - RESTful endpoint specification

### Frontend
- **React** - UI library
- **JavaScript (ES6+)** - Programming language
- **HTML5** - Markup

## Project Structure

```
.
├── lib/
│   ├── phoenix_json_app/           # Business logic
│   └── phoenix_json_app_web/       # Web layer
│       ├── controllers/            # API endpoints
│       ├── views/                  # JSON serializers
│       └── router.ex              # Route definitions
├── assets/
│   └── js/
│       └── src/
│           ├── components/         # React components
│           ├── pages/             # Page components
│           └── App.js             # Main app component
├── priv/
│   └── repo/                      # Database migrations
└── mix.exs                        # Elixir dependencies
```

## Installation

### Prerequisites
- [Elixir](https://elixir-lang.org/install.html) (v1.10+)
- [Phoenix](https://hexdocs.pm/phoenix/installation.html)
- [Node.js](https://nodejs.org/) (v14+)
- [PostgreSQL](https://www.postgresql.org/) (optional, for database)

### Setup

```bash
# Clone the repository
git clone https://github.com/rbalogic/phoenix-json-app.git

# Navigate to the project
cd phoenix-json-app

# Install Elixir dependencies
mix deps.get

# Install Node.js dependencies
cd assets
npm install
cd ..

# Set up the database (if using)
mix ecto.create
mix ecto.migrate

# Start the Phoenix server
mix phx.server
```

The application will run on `http://localhost:4000`

## API Endpoints

The backend provides JSON API endpoints at `/api/*`:

```
GET    /api/items           # List all items
GET    /api/items/:id       # Get specific item
POST   /api/items           # Create new item
PUT    /api/items/:id       # Update item
DELETE /api/items/:id       # Delete item
```

## Running the Application

### Development Mode

```bash
# Terminal 1: Start Phoenix server
mix phx.server

# Terminal 2 (optional): Watch for asset changes
cd assets && npm start
```

Visit `http://localhost:4000` in your browser.

### Building for Production

```bash
# Build assets
cd assets
npm run build
cd ..

# Create production release
mix release
```

## Architecture

### Backend (Phoenix)
- Handles business logic and data persistence
- Serves RESTful JSON API endpoints
- Manages database operations with Ecto ORM
- Provides request validation and error handling

### Frontend (React)
- Consumes JSON API from Phoenix backend
- Manages UI state and user interactions
- Provides responsive, component-based interface
- Handles client-side routing (if applicable)

## Key Dependencies

### Elixir
```elixir
{:phoenix, "~> 1.x"}
{:phoenix_html, "~> 3.x"}
{:plug_cowboy, "~> 2.x"}
```

### JavaScript
```json
{
  "react": "^18.x",
  "react-dom": "^18.x"
}
```

## Development Workflow

1. **Start the server** - `mix phx.server`
2. **Make code changes** - Edit files in `lib/` or `assets/js/src/`
3. **Hot reloading** - Changes reflect automatically in browser
4. **Test changes** - Visit API endpoints or interact with React frontend

## Best Practices Demonstrated

- ✅ Separation of concerns (backend/frontend)
- ✅ RESTful API design
- ✅ Component-based architecture
- ✅ Proper error handling
- ✅ Clean code structure
- ✅ Modular dependencies

## Resources

- [Phoenix Documentation](https://hexdocs.pm/phoenix/overview.html)
- [Elixir Documentation](https://elixir-lang.org/docs.html)
- [React Documentation](https://react.dev)
- [JSON:API Specification](https://jsonapi.org/)
- [Phoenix JSON API Guide](https://hexdocs.pm/phoenix/json_api.html)

## Learning Outcomes

By building this project, I gained experience with:
- Full-stack web development
- Elixir and functional programming patterns
- Phoenix framework best practices
- React component architecture
- Client-server communication
- API design and implementation

## Future Enhancements

- [ ] Add authentication and authorization
- [ ] Implement WebSocket real-time updates
- [ ] Add comprehensive test suite
- [ ] Improve error handling and validation
- [ ] Add API documentation with Swagger
- [ ] Implement caching strategies

## Contributing

Contributions are welcome! Feel free to fork the repository and submit pull requests for improvements.

## License

This project is open source and available under the MIT License.

---

**Note:** This is a minimal demonstration project showcasing Phoenix and React integration. It serves as a foundation for building more complex full-stack applications.
