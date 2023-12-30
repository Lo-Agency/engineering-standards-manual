# Application Development Standards

## Coding Conventions

We follow consistent conventions to enhance code clarity and readability across all projects:

### Pascal Case Naming 

All variables, functions, files, components, folders etc. should use **PascalCase**. This capitalizes the first letter of each word (e.g. `AppComponent`, `GetCustomers()`).

Using PascalCase improves scanability of code and keeps file/folder names readable.

### Atomic Design

We structure our React and React Native applications using the **Atomic Design** methodology. This divides components into atoms (basic building blocks), molecules (combing atoms), organisms (combining molecules), templates, and pages.

Organizing code this way keeps components and features modular, reusable, and easier to maintain.

## Code Quality Processes

To guarantee excellent code quality, all pull requests must go through peer **code reviews** before being merged, regardless of the experience level of the engineer. 

Code reviews enable knowledge sharing, better architectural patterns, and error catching before changes impact other developers.

For more complex features, we also utilize **pair programming** - two developers coding together at one workstation. This enables real-time feedback and faster solutions to problems.

## Documentation Requirements

We emphasize writing clean, self-documenting code using best practices and semantic naming. However, additional documentation is required in certain cases:

### Complex Functions/Components

Any highly complex logic should include inline comments explaining the intention and conceptual flow to aid future maintainers.

### Project README

All projects must include a thorough README file covering:

- Local development environment setup
- Description of technologies/services used
- Deployment instructions
- Configuration of any API keys, environment variables, etc.

The goal is to enable anyone to smoothly install, run, and deploy the software by following the outlined steps.