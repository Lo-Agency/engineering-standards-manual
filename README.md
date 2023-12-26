# Engineering Standards Manual
Version: 0.1

Last modified: Dec 11, 2023

## Chapters
- [Introduction](introduction.md)
- [Technology Stack Overviews](technology-stack-overviews.md)
- [Application Development Standards](application-development-standards.md)
- [Engineering Team Policies](engineering-team-policies.md)
- [Technical Best Practices](technical-best-practices.md)

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
