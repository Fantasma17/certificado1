# Quality Assurance & Testing with Chai

## Overview
This is a Quality Assurance and Testing application built with Node.js, Express.js, and Chai. The project is a learning platform for practicing automated testing techniques including unit tests, functional tests with chai-http, and browser-based tests with Zombie.js.

**Purpose**: Educational project for learning testing frameworks and methodologies
**Current State**: Fully configured and running in Replit environment
**Last Updated**: September 25, 2025

## Recent Changes
- **Server Configuration**: Updated server.js to bind to 0.0.0.0:5000 for Replit compatibility
- **Bug Fix**: Fixed client.js AJAX function where `params` was undefined (changed to `options.data`)
- **Workflow Setup**: Created Express server workflow on port 5000
- **Deployment**: Configured autoscale deployment target with npm start command

## Project Architecture
```
├── server.js           # Main Express server
├── package.json        # Dependencies and scripts
├── test-runner.js      # Mocha test runner with custom reporting
├── assertion-analyser.js # Test assertion analysis utility
├── views/
│   └── index.html     # Frontend HTML page
├── public/
│   ├── client.js      # Frontend JavaScript with AJAX utilities
│   └── style.css      # Styles
└── tests/
    ├── 1_unit-tests.js      # Chai unit tests (intentionally failing)
    └── 2_functional-tests.js # Chai-http and Zombie.js tests (intentionally failing)
```

## Key Features
- **Express.js API**: REST endpoints for testing (`/hello`, `/travellers`)
- **Frontend Form**: Interactive form for testing Italian explorers data
- **Test Suite**: Comprehensive test coverage with unit and functional tests
- **Real-time Testing**: Tests run automatically when server starts
- **API Testing**: chai-http integration for HTTP endpoint testing
- **Browser Testing**: Zombie.js for headless browser testing

## API Endpoints
- `GET /` - Serves the main HTML page
- `GET /hello?name=<name>` - Returns greeting message
- `PUT /travellers` - Accepts JSON with surname, returns explorer data
- `GET /_api/get-tests` - Returns test results in JSON format

## Development Setup
- **Server**: Runs on port 5000, bound to 0.0.0.0
- **Dependencies**: All installed via npm
- **Workflow**: "Server" workflow runs `npm start`
- **Testing**: Tests run automatically 1.5 seconds after server start

## Test Structure
The tests are intentionally failing as this is an educational project where students learn to fix them:
- Unit tests cover Chai assertion methods (isNull, equal, deepEqual, etc.)
- Functional tests cover HTTP requests and browser interactions
- 25 total tests designed for learning different testing patterns

## Deployment
- **Target**: Autoscale (suitable for stateless web applications)
- **Command**: `npm start` 
- **Port**: 5000 (required for Replit)