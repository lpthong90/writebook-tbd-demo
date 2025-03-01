# Writebook

Writebook is a Rails application for creating and managing digital books. It provides a platform for collaborative book writing, editing, and publishing.

## Features

- Book creation and management
- Collaborative editing
- Markdown support with Redcarpet
- Syntax highlighting with Rouge
- Image processing capabilities
- QR code generation
- User authentication with BCrypt
- Real-time updates with Turbo

## Requirements

- Ruby 3.3.1
- Redis
- SQLite3
- Node.js

## Setup

1. Clone the repository

2. Install dependencies:
```bash
bin/setup
```

This will:
- Install Ruby gems
- Set up the database
- Clear logs and temporary files
- Configure puma-dev for local development

## Development

### Starting the Application

```bash
bin/rails server
```

### Background Jobs

The application uses Resque for background job processing. Start the workers with:

```bash
resque-pool
```

### Code Quality

The project uses several tools to maintain code quality:

- Rubocop for code style checking:
```bash
bin/rubocop
```

- Brakeman for security analysis:
```bash
bin/brakeman
```

### Testing

Run the test suite with:

```bash
bin/rails test
bin/rails test:system
```

## Deployment

The application includes a Docker configuration for production deployment:

1. Build the Docker image:
```bash
docker build -t writebook .
```

2. Run the container:
```bash
docker run -p 3000:3000 writebook
```

## License

This project is proprietary software.

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request