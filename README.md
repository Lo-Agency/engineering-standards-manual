# Engineering Standards Manual
Version: 0.1

Last modified: Dec 11, 2023

## Chapters
- [Introduction](introduction.md)


## Introduction
Welcome to the Software Development & Technology Handbook for our engineering team. The purpose of this handbook is to outline the standards, policies, processes, and guidelines followed across all software projects in our organization.

Having clear, well-documented development practices is essential for building high-quality products efficiently at scale. This handbook establishes these common methodologies for our technology teams to promote consistency and best practices in our approach to software engineering.

The contents covered in this guide include:

- Technology Stack Overviews: Approved languages, frameworks, databases, and other technologies organized by project type
- Application Development Standards: Coding conventions, code quality processes, documentation requirements, and architecture guidelines
- Engineering Team Policies: Issue tracking protocols, code review procedures, build & testing rules, and other operational standards
- Technical Best Practices: Security, performance, modularity and other coding best practices for efficient, sustainable software
- Development Processes & Tools: Step-by-step implementation guidelines for our software development life cycle, version control system, CI/CD tools, and other key platforms

This handbook is intended to codify the practices we employ to deliver secure, scalable, and reliable products. It defines what technologies to use when, how to write high-quality code at scale, what procedures to follow during development, and overarching best practices to work efficiently as a team.

Adhering to these documented standards will enable us to collaborate smoothly, maintain cleaner systems long-term, improve consistency across our engineering division. We look forward to collaborating successfully on impactful projects using the guidelines contained in this handbook.

Please direct any questions or comments to [hi@lo.agency](mailto:hi@lo.agency) as we continue improving our practices. Thank you in advance for following these methodologies in your valuable work!

## Technology Stack Overviews

### Websites

- Front-End
    - React
    - Next.js
    - Vanilla JavaScript 
- Animations & Interactivity 
    - GSAP
    - Three.js
- Focus
    - Creative, animation/interaction-heavy sites

### Web Applications

- Front-End
    - React
        - Create-React-App (CSR)
        - Next.js (CSR/SSR)
    - Tailwind or UI Kits (Ant Design)
    - State Management
        - Context API, Zustand (Small/Medium Apps) 
        - Redux (Complex Apps)
    - API Client
        - TanStack React Query and Apollo Client
- Back-End
    - NestJS
    - PostgreSQL
    - REST APIs
    - GraphQL APIs
    - Docker 
    - Prisma/TypeORM
    - JWT Authentication

### Mobile Applications 

- Front-End
    - React Native
- Back-End
    - Same as Web Applications

## Application Development Standards

### Coding Conventions

We follow consistent conventions to enhance code clarity and readability across all projects:

#### Pascal Case Naming 

All variables, functions, files, components, folders etc. should use **PascalCase**. This capitalizes the first letter of each word (e.g. `AppComponent`, `GetCustomers()`).

Using PascalCase improves scanability of code and keeps file/folder names readable.

#### Atomic Design

We structure our React and React Native applications using the **Atomic Design** methodology. This divides components into atoms (basic building blocks), molecules (combing atoms), organisms (combining molecules), templates, and pages.

Organizing code this way keeps components and features modular, reusable, and easier to maintain.

### Code Quality Processes

To guarantee excellent code quality, all pull requests must go through peer **code reviews** before being merged, regardless of the experience level of the engineer. 

Code reviews enable knowledge sharing, better architectural patterns, and error catching before changes impact other developers.

For more complex features, we also utilize **pair programming** - two developers coding together at one workstation. This enables real-time feedback and faster solutions to problems.

### Documentation Requirements

We emphasize writing clean, self-documenting code using best practices and semantic naming. However, additional documentation is required in certain cases:

#### Complex Functions/Components

Any highly complex logic should include inline comments explaining the intention and conceptual flow to aid future maintainers.

#### Project README

All projects must include a thorough README file covering:

- Local development environment setup
- Description of technologies/services used
- Deployment instructions
- Configuration of any API keys, environment variables, etc.

The goal is to enable anyone to smoothly install, run, and deploy the software by following the outlined steps.


## Engineering Team Policies

### Issue Tracking Protocols 

We standardize issue/task tracking in Linear using preset templates. Here are two example of them:

- **🐛 Bug Reports** - For software defects
- **🏖️ New Features** - For enhancement requests 

Engineers can self-assign tasks or add them to the backlog for later prioritization. We assign issues collaboratively during daily/weekly syncs.

*For a detailed overview of our entire task management process, please refer to the Task Management Guidelines section.*

Having centralized issue tracking maintains visibility and aligns priorities across teams.

### Code Review Procedures

The code review process for pull requests (PRs) is:

1. Engineer submits PR when task complete 
2. Engineer adds 1+ teammates as reviewers
3. Teammates review code changes within a few hours
4. Once approved, engineer merges PR
5. If waiting on reviews, engineer switches to another task

Reviews ensure changes meet standards before impacting other developers.

### Testing Rules 

Testing boosts our code coverage and regression testing:

- Unit testing with Jest is mandatory for web applications
- Additional plugins used for improved testing ergonomics 
- Website testing is encouraged but not required 
- Aim for test coverage between 70-90%


## Technical Best Practices 

### Security

We actively maintain secure development standards including:

- Encryption of sensitive data
- Input validation and sanitization 
- Use of content security policies  
- Regular dependency audits
- Static analysis testing
- Confidential data handling procedures

*This section will expand as new applicable standards emerge.*

### Performance

Common web performance metrics we optimize for:

- Page Load Time
- First Contentful Paint 
- Time to Interactive
- First Meaningful Paint
- Speed Index
- Time to First Byte
- Render Blocking Resources
- Network Requests 
- File Size/Compression
- Mobile Performance

We continually evaluate and enhance performance using Lighthouse audits, performance budgets, and tree shaking unused code.

*This section will expand as new applicable standards emerge.*

### Modularity

To maintain legible and maintainable code: 

- Components are kept small and single-purpose
- Strict separation of concerns is followed
- DRY (Don't Repeat Yourself) principles applied
- Loose coupling between modules
- High cohesion inside modules

This enhances readability, reusability and reduces bugs.


*This section will expand as new applicable standards emerge.*

## Development Processes & Tools

### Software Development Life Cycle Overview

#### Summary of Main Phases

Our development process depends on the project type:

**Websites**

We follow a linear Waterfall model with these phases:   

1. Requirements Gathering: Compile all features, content, and desired functionality
2. Design: Create wireframes and UI/UX specifications  
3. Development: Engineer site based on specifications
4. Testing: Perform quality assurance testing, fix defects
5. Maintenance: Provide ongoing site support and enhancements

**Applications** 

We use Agile frameworks like Kanban or Scrum:

1. Product Backlog: Prioritized list of required features  
2. Sprints: Fixed cycles to complete backlog items
3. Review Meetings: Demo functionality, gather feedback
4. Potentially Releasable: Each sprint completion  
5. Retrospectives: Review processes post-sprint  

Activities in each phase align to standard Agile ceremonies.
 
#### Issue/Task Tracking Guidelines

We will cover the detailed guidelines, best practices, and step-by-step instructions for managing issues and tasks using Linear in the dedicated Task Management section.


### Source Control Procedures 

We utilize Git for version control and source code management. Our branch methodology enables organized collaboration.  

#### Commit Conventions

Commits follow the [Angular Commit Message Conventions](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#commit) consisting of a type, short scope description, and issue reference:

```
feat(auth): add local authentication flow #145
``` 

**Atomic commits keep changes small so they are easily revertible.**

#### Feature Branching 

For every feature or bug fix item:

1. Checkout a new branch from `next` 
2. Prefix branch name with your Linear username, task id, and task slug: `bardiya/eng-1227-creating-our-standard-documents-v01`
3. Develop the item and commit changes
4. Open pull request targeting `next` when complete
5. Branch is merged after approval  

This keeps `next` integratable with the latest changes.

#### Mainline Branches

- `main`: Production branch, always deployable
- `uat`: Pre-production for user testing  
- `next`: Development branch integrating branches

Code moves from `next` to `uat` to `main` through pull requests, automating builds and tests.

### Continuous Integration & Delivery

Continuous Integration and Delivery (CI/CD) automates building, testing and deployment of applications.

#### Build Automation

Configuring CI/CD pipelines enables:  

- Automatic version control triggers
- Running test suites
- Building deployment artifacts
- Consistent environments
- Rapid delivery and reduced risk  

#### Our Implementation

Our CI/CD process depends on the project architecture:

**Dynamic Web Apps**

- Docker containers used for services
- Hosted on cloud platforms (AWS, GCP)
- Automated deployments from git branches 

**Static Sites** 

- No-code services like Netlify
- Merges to `main` auto-build and deploy
- Support global CDNs

We utilize [Chabokan](https://chabokan.net) for most full-stack deployment automation.

### Documentation Standards

We maintain up-to-date documentation covering tools, APIs, and code.

#### README Files

READMEs follow Markdown formatting with:

- **Overview**: High-level project description
- **Installation**: Dependency setup steps  
- **Usage**: Code examples and running instructions
- **Contributing**: Guidelines to contribute  
- **License**: Open source licensing 

#### API Documentation 

Our API docs use JSDoc syntax:

- **Method-level** docs: 
    - Description
    - Parameters 
    - Returns
    - Throws
    - Examples

- Generated documentation site

#### Inline Comments

Code includes inline comments for:

- **Line comments**: Specific implementation details 
- **Docblocks**: Overall method/class explanations
- **Links**: Related code sections
- **Deprecation**: Explanations on outdated code

We emphasize keeping documentation **consistent**, **concise**, and **up-to-date**.
