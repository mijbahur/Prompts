# Claude Code Master Handbook

### Complete Full-Stack Development Workflow

| | |
|---|---|
| **Environment** | Windows + VS Code + Claude Code |
| **Project** | Frontend + Backend + Database |
| **Account** | Multiple Gmail accounts |
| **Total** | 70 reusable prompts |

> **How to use:** Every prompt is inside its own code block. Click the copy button (or select the block) and paste it straight into Claude Code. Replace any `[PLACEHOLDER]` text before sending.

---

## Table of Contents

- [Part 01 — Installation & Initial Setup](#part-01--installation--initial-setup)
- [Part 02 — Account Switching & Session Recovery](#part-02--account-switching--session-recovery)
- [Part 03 — Project Understanding](#part-03--project-understanding)
- [Part 04 — Documentation & Project Memory](#part-04--documentation--project-memory)
- [Part 05 — Architecture Analysis](#part-05--architecture-analysis)
- [Part 06 — Bug Detection & Debugging](#part-06--bug-detection--debugging)
- [Part 07 — Feature Development](#part-07--feature-development)
- [Part 08 — Frontend UI/UX](#part-08--frontend-uiux)
- [Part 09 — Backend & API](#part-09--backend--api)
- [Part 10 — Database Management](#part-10--database-management)
- [Part 11 — Security](#part-11--security)
- [Part 12 — Performance](#part-12--performance)
- [Part 13 — Testing & QA](#part-13--testing--qa)
- [Part 14 — Git & Code Management](#part-14--git--code-management)
- [Part 15 — Production & Deployment](#part-15--production--deployment)
- [Part 16 — Final Review & Maintenance](#part-16--final-review--maintenance)
- [Quick Reference — Account Switching](#quick-reference--account-switching)
- [Project Root File Structure](#project-root-file-structure)
- [Daily Development Workflow](#daily-development-workflow)
- [Important Development Rules](#important-development-rules)

---

# PART 01 — Installation & Initial Setup

## Toggle 01 — Install Claude Code

```text
I want to set up Claude Code on my Windows computer.

Guide me through the installation and configuration.

Requirements:
1. Check whether Claude Code is already installed.
2. Check the installed version.
3. Explain any missing prerequisites.
4. Install Claude Code using the recommended official method.
5. Verify that the installation works.
6. Explain how to launch Claude Code from PowerShell and VS Code.

Do not modify any of my project files during installation.

Provide commands one by one and explain what each command does.
```

## Toggle 02 — First-Time Authentication

```text
Help me authenticate Claude Code using my primary Gmail account.

Requirements:
1. Explain the available authentication methods.
2. Guide me through browser-based authentication.
3. Verify that authentication is successful.
4. Explain how to check my active account.
5. Explain how to check usage limits.
6. Explain how to log out safely.

Do not ask me to share passwords, verification codes, or API keys.
```

## Toggle 03 — Open Complete Full-Stack Project

```text
Help me open my complete full-stack project in Claude Code.

My project may contain:
- client/ or frontend/
- server/ or backend/
- shared/
- database/
- configuration files
- package.json

Requirements:
1. Identify the common parent directory.
2. Verify that both frontend and backend are inside the accessible project directory.
3. Explain how to open the parent folder in VS Code.
4. Explain how to launch Claude Code from the correct directory.
5. Verify that both client-side and server-side folders are accessible.

Do not modify any files.

Do not access directories outside the project unless I explicitly authorize it.
```

## Toggle 04 — Verify Project Access

```text
Verify that you can access my complete project.

Check:
1. Frontend directory.
2. Backend directory.
3. Shared directories.
4. Main configuration files.
5. Documentation files.
6. Git repository status.

Identify any folders that cannot be accessed.

Do not modify, create, or delete files.

Report the accessible project structure and any permission limitations.
```

---

# PART 02 — Account Switching & Session Recovery

## Toggle 05 — Before Switching Gmail

```text
I am about to switch from my current Claude account to another Gmail account because I have reached my usage limit.

Before switching:

1. Summarize the current development task.
2. Explain what has been completed.
3. Explain what remains unfinished.
4. Identify all files modified during this session.
5. Identify any pending changes that have not been verified.
6. List the commands and tests already executed.
7. Explain the exact next steps.
8. Identify important technical decisions and constraints.

Create a concise account-switch handoff document named ACCOUNT_HANDOFF.md in the project root.

Do not include API keys, passwords, tokens, or other secrets.

Do not overwrite an existing handoff document without asking me.

Do not make unrelated code changes.
```

## Toggle 06 — Switch Gmail Account

```text
I want to switch my Claude Code authentication to another Gmail account.

Guide me through the process.

Requirements:
1. Explain how to safely end the current Claude Code session.
2. Explain how to log out.
3. Explain how to authenticate with the second Gmail account.
4. Verify the active account using the appropriate status command.
5. Explain how to reopen my existing project.
6. Verify that both frontend and backend folders remain accessible.

Important:
- Do not delete or modify project files.
- Do not reset Git.
- Do not remove project dependencies.
- Do not overwrite account-specific settings.
- Do not assume that switching accounts transfers conversation history.

Give me commands one at a time.
```

## Toggle 07 — Continue After Switching Gmail

```text
I have switched to a different Claude account.

Continue working on the same full-stack project.

First:

1. Read CLAUDE.md if it exists.
2. Read ACCOUNT_HANDOFF.md if it exists.
3. Inspect the current Git status.
4. Inspect the files related to the unfinished task.
5. Verify the current implementation instead of assuming the previous account's work was completed.
6. Identify the exact point where development should continue.

Then summarize:
- Previous progress
- Current project status
- Pending tasks
- Relevant files
- Next recommended action

Do not repeat completed work unnecessarily.

Do not revert existing changes.

Ask me before making significant architectural changes.
```

## Toggle 08 — Restore Previous Development Context

```text
Reconstruct the development context of this project using its existing documentation and files.

Check:
- CLAUDE.md
- ACCOUNT_HANDOFF.md
- README.md
- Git commit history
- Current Git changes
- Relevant source code
- Existing TODO comments

Do not assume you have access to previous Claude conversations.

Produce a clear summary of the project's current state and identify the next unfinished development task.

Do not modify any files.
```

---

# PART 03 — Project Understanding

## Toggle 09 — Understand Entire Project

```text
Analyze my entire full-stack project.

I want you to understand the complete application before making any changes.

Analyze:

1. Complete folder and file structure.
2. Frontend technologies and architecture.
3. Backend technologies and architecture.
4. Database structure and relationships.
5. Authentication and authorization.
6. API endpoints and integrations.
7. Environment variables and configurations.
8. State management.
9. Routing and navigation.
10. Build and deployment configuration.

For each important file, explain its responsibility.

Identify how the frontend communicates with the backend and how data flows through the application.

Important:
- Do not modify any files.
- Do not delete anything.
- Do not expose secrets.
- Do not guess when you can inspect the source code.

At the end, provide a complete technical overview of the application.
```

## Toggle 10 — Understand Frontend/Backend Communication

```text
Analyze how my frontend and backend communicate.

Trace the complete application workflow:

1. User interaction in the frontend.
2. Form submission or button actions.
3. Frontend validation.
4. API request creation.
5. Backend route handling.
6. Middleware execution.
7. Controller or service execution.
8. Database operations.
9. Backend response.
10. Frontend response handling.
11. UI updates and error messages.

Create a list of API endpoints with:
- HTTP method
- Endpoint URL
- Backend file location
- Frontend file that uses it
- Request structure
- Response structure
- Authentication requirements

Identify mismatches between frontend and backend.

Do not modify any files.
```

## Toggle 11 — Understand Existing Features

```text
Create a complete inventory of my application's existing features.

Explore both frontend and backend.

For every feature, document:

1. Feature name.
2. Purpose.
3. Related frontend components.
4. Related backend routes.
5. Database dependencies.
6. Authentication requirements.
7. Current implementation status.
8. Potential problems.

Separate features into:
- Fully implemented
- Partially implemented
- Not implemented
- Broken or potentially unreliable

Do not assume a feature works just because its UI exists.

Do not modify any files.
```

---

# PART 04 — Documentation & Project Memory

## Toggle 12 — Create CLAUDE.md

```text
Create a comprehensive CLAUDE.md file in the root directory of my full-stack project.

The document must guide future Claude Code sessions.

Include:

1. Project overview.
2. Technology stack.
3. Frontend architecture.
4. Backend architecture.
5. Database structure.
6. Folder structure.
7. API conventions.
8. Coding standards.
9. Naming conventions.
10. Error-handling rules.
11. Authentication and security guidelines.
12. Testing instructions.
13. Build commands.
14. Development commands.
15. Deployment instructions.
16. Important project restrictions.

Important:
- Base everything on the actual source code.
- Do not invent technologies or commands.
- Keep instructions concise and useful.
- Never include passwords, tokens, or secret values.
- Preserve existing application code.

This document should help a new Claude Code session understand the project quickly.
```

## Toggle 13 — Keep Documentation Updated

```text
Review my existing project documentation.

Update CLAUDE.md and other relevant documentation when necessary.

Whenever the project architecture, APIs, dependencies, or development workflow changes:

1. Identify outdated documentation.
2. Compare documentation against actual source code.
3. Update incorrect information.
4. Document important new features.
5. Update development and testing commands.
6. Keep account-independent project instructions in CLAUDE.md.

Do not include temporary conversation history in permanent project documentation.

Do not include secrets.

Do not overwrite useful documentation unnecessarily.

Report all documentation changes.
```

## Toggle 14 — Create Development Handoff

```text
Create or update a development handoff document for this project.

The document should contain:

1. Current development status.
2. Recently completed tasks.
3. Current unfinished task.
4. Modified files.
5. Known bugs.
6. Pending decisions.
7. Test results.
8. Next development steps.
9. Relevant commands.
10. Important implementation details.

Use the filename ACCOUNT_HANDOFF.md.

Keep it concise and easy to understand.

Do not include credentials or secrets.

Do not overwrite an existing handoff without checking its contents first.

This document must allow another Claude account to continue development without depending on the previous conversation history.
```

---

# PART 05 — Architecture Analysis

## Toggle 15 — Full Architecture Audit

```text
Perform a complete architecture audit of my full-stack application.

Analyze both frontend and backend.

Frontend:
- Component organization
- Routing
- State management
- API integration
- Reusable components
- Error handling
- UI architecture

Backend:
- Route organization
- Controllers
- Services
- Middleware
- Database access
- Authentication
- Validation
- Error handling

Full-stack integration:
- API contracts
- Request and response consistency
- Authentication flow
- Data synchronization
- Shared types
- Error propagation

Identify:
1. Architectural weaknesses.
2. Unnecessary complexity.
3. Duplicate implementations.
4. Poor separation of responsibilities.
5. Scalability concerns.
6. Maintainability problems.

Provide a prioritized improvement plan.

Do not modify files during the initial audit.
```

## Toggle 16 — Architecture Improvement

```text
Based on the architecture audit, propose improvements to my application.

My goals are:
- Maintainable code.
- Reusable components.
- Clean architecture.
- Clear frontend/backend separation.
- Scalable APIs.
- Reliable database operations.
- Consistent error handling.

Before implementing:

1. Explain the proposed architecture.
2. Identify affected files.
3. Explain possible breaking changes.
4. Identify migration requirements.
5. Explain how existing functionality will be preserved.

Wait for my approval before major architectural changes.

Implement approved improvements in small steps.

Run relevant tests after each step.
```

---

# PART 06 — Bug Detection & Debugging

## Toggle 17 — Find All Bugs

```text
Perform a comprehensive bug investigation across my entire application.

Check both frontend and backend.

Look for:

1. Runtime errors.
2. Console errors.
3. API failures.
4. Incorrect API responses.
5. Broken routes.
6. Form validation problems.
7. Authentication issues.
8. Database errors.
9. State management bugs.
10. UI interaction problems.
11. Loading-state problems.
12. Error-handling issues.
13. Responsive layout problems.
14. Unexpected edge cases.

For each confirmed bug, report:
- Description
- Reproduction steps
- Affected files
- Root cause
- Severity
- Recommended fix

Do not modify any files during the investigation.

Do not report guesses as confirmed bugs.
```

## Toggle 18 — Fix Bugs One by One

```text
Fix the confirmed bugs in my project one by one.

For each bug:

1. Understand the root cause.
2. Identify the smallest safe solution.
3. Check related frontend and backend code.
4. Implement the fix.
5. Run relevant tests.
6. Verify that existing functionality still works.

Important:
- Do not rewrite unrelated code.
- Do not introduce unnecessary dependencies.
- Preserve existing architecture.
- Avoid changing API contracts unless necessary.
- Do not remove existing features.

After every important fix, explain:
- What was wrong.
- What you changed.
- Which files were modified.
- How you verified the fix.

If a fix could cause breaking changes, ask for approval first.
```

## Toggle 19 — Debug an Error

> Replace the two placeholders before sending.

```text
Help me investigate and fix the following error.

ERROR:
[PASTE ERROR MESSAGE HERE]

CONTEXT:
[EXPLAIN WHAT I WAS DOING WHEN THE ERROR OCCURRED]

Requirements:

1. Locate the source of the error.
2. Inspect related frontend and backend files.
3. Trace the complete execution flow.
4. Identify the actual root cause.
5. Explain why the error occurs.
6. Propose the safest solution.
7. Implement the fix after explaining the approach.
8. Run relevant tests.
9. Verify the error is resolved.

Do not hide errors using empty catch blocks or unnecessary fallback logic.

Do not modify unrelated functionality.
```

## Toggle 20 — Fix Frontend/Backend Integration Bugs

```text
Investigate integration problems between my frontend and backend.

Check:

1. Incorrect API URLs.
2. HTTP method mismatches.
3. Request body mismatches.
4. Response structure mismatches.
5. Missing headers.
6. Authentication token problems.
7. CORS configuration.
8. Incorrect status-code handling.
9. Data validation mismatches.
10. Loading and error states.

Trace each issue from frontend request to backend response.

Fix confirmed integration bugs while preserving existing functionality.

Run relevant frontend and backend tests after the changes.
```

---

# PART 07 — Feature Development

## Toggle 21 — Plan a New Feature

> Replace the two placeholders before sending.

```text
I want to add a new feature to my existing application.

FEATURE NAME:
[ENTER FEATURE NAME]

FEATURE DESCRIPTION:
[EXPLAIN WHAT THE FEATURE SHOULD DO]

Before writing code:

1. Understand the existing application architecture.
2. Identify related frontend components.
3. Identify related backend routes and services.
4. Identify database changes, if necessary.
5. Identify required API endpoints.
6. Identify authentication and authorization requirements.
7. Identify validation and error-handling requirements.
8. Identify possible conflicts with existing features.

Provide:
- Implementation plan
- Required files
- API design
- Database changes
- User workflow
- Testing strategy
- Potential risks

Do not write or modify code until I approve the implementation plan.
```

## Toggle 22 — Implement a Complete Full-Stack Feature

> Replace the two placeholders before sending.

```text
Implement the following feature in my full-stack application.

FEATURE:
[ENTER FEATURE NAME]

REQUIREMENTS:
[ENTER FEATURE REQUIREMENTS]

Implement the complete feature across frontend and backend.

Frontend:
- Create or update necessary UI components.
- Implement user interactions.
- Add form validation.
- Integrate the required APIs.
- Handle loading, success, and error states.
- Ensure responsive design.

Backend:
- Implement required API routes.
- Add controllers and services where appropriate.
- Validate incoming data.
- Apply authentication and authorization.
- Implement database operations.
- Handle errors securely.

Integration:
- Keep frontend and backend API contracts consistent.
- Use appropriate HTTP status codes.
- Handle unexpected responses.
- Avoid duplicated logic.

Testing:
- Test the complete feature workflow.
- Verify edge cases.
- Ensure existing features still work.

Follow the existing project architecture and coding conventions.

Do not introduce unnecessary dependencies.

Summarize all modified files and test results.
```

## Toggle 23 — Add Features Without Breaking Existing Features

```text
I want to add new functionality without breaking existing application features.

Before implementing:

1. Identify all components affected by the new feature.
2. Identify dependencies on existing APIs.
3. Identify shared database models.
4. Check authentication and authorization.
5. Identify possible side effects.

Implement the feature using the smallest safe changes.

Requirements:
- Preserve existing behavior.
- Avoid unnecessary refactoring.
- Maintain backward compatibility where possible.
- Reuse existing components and services.
- Add appropriate tests.
- Verify related existing workflows.

If a breaking change is unavoidable, explain it and wait for approval.
```

## Toggle 24 — Refactor Existing Code

```text
Review the codebase and identify opportunities for safe refactoring.

Focus on:

1. Duplicate code.
2. Large components.
3. Complex functions.
4. Repeated API logic.
5. Unnecessary dependencies.
6. Poor naming.
7. Unclear responsibilities.
8. Difficult-to-maintain code.

For every proposed refactoring:
- Explain the current problem.
- Explain the proposed improvement.
- Identify affected files.
- Explain potential risks.

Do not change application behavior.

Refactor only after approval.

Run appropriate tests and compare behavior before and after refactoring.
```

## Toggle 25 — Implement a Complete User Workflow

> Replace the placeholder before sending.

```text
Analyze and implement a complete user workflow for the following functionality.

WORKFLOW:
[DESCRIBE USER WORKFLOW]

Consider every stage:

1. Initial user interaction.
2. Input collection.
3. Frontend validation.
4. API request.
5. Backend processing.
6. Database operations.
7. Response handling.
8. Success feedback.
9. Failure handling.
10. Loading states.
11. Edge cases.
12. Authorization.

Ensure the workflow works from beginning to end.

Do not implement only the frontend UI while leaving the backend incomplete.

Verify the complete workflow using appropriate tests.
```

---

# PART 08 — Frontend UI/UX

## Toggle 26 — Complete UI/UX Audit

```text
Perform a complete UI/UX audit of my frontend application.

Review:

1. Overall visual consistency.
2. Typography.
3. Color system.
4. Spacing and alignment.
5. Navigation.
6. Buttons and interactive elements.
7. Forms and validation.
8. Cards and tables.
9. Modals and dialogs.
10. Loading states.
11. Empty states.
12. Error messages.
13. Mobile responsiveness.
14. Accessibility.

Check every important page and identify inconsistent components.

Provide a prioritized improvement plan.

Do not modify any files yet.

Preserve the application's existing brand identity unless I request a redesign.
```

## Toggle 27 — Modern Professional UI

```text
Improve my application's frontend design to a modern, professional, production-quality standard.

Design goals:

- Clean and minimal interface.
- Consistent typography.
- Balanced spacing.
- Clear visual hierarchy.
- Professional color palette.
- Reusable UI components.
- Consistent buttons and forms.
- Smooth but subtle interactions.
- Responsive layouts.
- Accessible components.

Requirements:

1. Inspect the existing design system.
2. Reuse existing components where possible.
3. Maintain existing functionality.
4. Avoid unnecessary animation.
5. Avoid inconsistent styles.
6. Avoid unnecessary dependencies.
7. Verify desktop, tablet, and mobile layouts.

Do not redesign the application randomly.

Maintain a consistent design language across all pages.
```

## Toggle 28 — Responsive Design

```text
Audit and improve responsive design across my entire frontend.

Check layouts at:

- Small mobile screens.
- Standard mobile screens.
- Tablets.
- Laptops.
- Large desktop screens.

Check:

1. Navigation menus.
2. Sidebars.
3. Tables.
4. Forms.
5. Cards.
6. Modals.
7. Images.
8. Buttons.
9. Typography.
10. Horizontal overflow.

Fix layout problems without removing features.

Use the existing CSS framework and styling conventions.

Verify that the application remains usable on all target screen sizes.
```

## Toggle 29 — Dark Mode and Light Mode

```text
Analyze my application's existing theme implementation.

I want a consistent light mode and dark mode.

Requirements:

1. Use centralized design tokens or CSS variables.
2. Apply consistent background and foreground colors.
3. Ensure cards and dialogs support both themes.
4. Update forms and input fields.
5. Maintain readable text contrast.
6. Support navigation and sidebars.
7. Ensure icons and borders remain visible.
8. Preserve user theme preferences using the existing project approach.
9. Avoid flashing or incorrect theme initialization where possible.

Do not introduce a second conflicting theme system.

Verify both themes across all important pages.
```

## Toggle 30 — Accessibility

```text
Perform an accessibility review of my frontend.

Check:

1. Semantic HTML.
2. Keyboard navigation.
3. Focus visibility.
4. Screen reader labels.
5. Image alternative text.
6. Color contrast.
7. Form labels.
8. Accessible dialogs.
9. Button and link semantics.
10. Responsive text sizing.

Implement appropriate accessibility improvements.

Preserve the existing design and functionality.

Report any remaining accessibility limitations.
```

---

# PART 09 — Backend & API

## Toggle 31 — Backend Architecture Audit

```text
Perform a detailed audit of my backend application.

Analyze:

1. Server initialization.
2. Route structure.
3. Controllers.
4. Services.
5. Middleware.
6. Database access.
7. Authentication.
8. Authorization.
9. Input validation.
10. Error handling.
11. Logging.
12. Configuration.
13. External integrations.

Identify duplicated logic, security weaknesses, and scalability issues.

Recommend improvements based on the current technology stack.

Do not modify files during the audit.
```

## Toggle 32 — API Documentation

```text
Generate complete API documentation for my existing backend.

For every endpoint, document:

1. Endpoint name.
2. HTTP method.
3. URL.
4. Purpose.
5. Authentication requirements.
6. Authorization requirements.
7. Request headers.
8. Request parameters.
9. Request body.
10. Response structure.
11. HTTP status codes.
12. Error responses.
13. Validation rules.

Verify each endpoint against the actual backend implementation.

Do not invent endpoints.

Use the documentation format already present in the project if one exists.

Do not expose secret values.
```

## Toggle 33 — API Error Handling

```text
Review and improve error handling across my backend APIs.

Requirements:

1. Use consistent error response structures.
2. Apply appropriate HTTP status codes.
3. Validate incoming requests.
4. Handle missing resources.
5. Handle authentication failures.
6. Handle authorization failures.
7. Handle database errors.
8. Handle unexpected server errors.
9. Avoid exposing internal stack traces in production.
10. Add appropriate logging.

Ensure frontend clients can understand and display API errors correctly.

Preserve existing API behavior where possible.

Update tests for the modified endpoints.
```

## Toggle 34 — API Integration and Validation

```text
Review all frontend-to-backend API integrations.

Check:

1. API base URLs.
2. HTTP methods.
3. Request headers.
4. Request payloads.
5. Response structures.
6. Validation rules.
7. Authentication tokens.
8. Error handling.
9. Timeout handling.
10. Loading states.

Identify inconsistent API contracts.

Where appropriate, use shared types or schemas to reduce frontend/backend mismatches.

Implement approved improvements and verify all affected endpoints.
```

## Toggle 35 — Authentication Review

```text
Audit my existing authentication and authorization implementation.

Analyze:

1. User registration.
2. User login.
3. Password hashing.
4. Session or token management.
5. Token expiration.
6. Refresh token handling, if implemented.
7. Logout.
8. Protected routes.
9. Role-based access control.
10. Password reset.
11. Account verification.
12. Rate limiting.

Identify security weaknesses and recommend fixes.

Do not expose passwords, tokens, or secret values.

Do not weaken existing security controls.

Wait for approval before implementing major authentication changes.
```

---

# PART 10 — Database Management

## Toggle 36 — Understand Database Structure

```text
Analyze the complete database structure of my application.

Identify:

1. Database technology.
2. Database connection configuration.
3. All tables or collections.
4. Models and schemas.
5. Relationships.
6. Primary and foreign keys.
7. Indexes.
8. Constraints.
9. Data validation.
10. Database access patterns.

Explain how frontend operations eventually interact with the database through the backend.

Identify redundant or inefficient structures.

Do not modify database schemas or data.

Never display database passwords or connection secrets.
```

## Toggle 37 — Database Optimization

```text
Analyze my database performance and identify optimization opportunities.

Check:

1. Slow queries.
2. Missing indexes.
3. Unnecessary database calls.
4. N+1 query problems.
5. Inefficient joins.
6. Pagination.
7. Large data retrieval.
8. Duplicate data.
9. Connection management.
10. Transaction handling.

Recommend improvements based on the actual database technology.

Do not change production data.

Do not execute destructive migrations.

Explain the expected benefits and risks before implementing changes.
```

## Toggle 38 — Database Migration Review

```text
Review the existing database migration system.

Analyze:

1. Existing migrations.
2. Current schema.
3. Migration ordering.
4. Schema consistency.
5. Rollback support.
6. Potential data loss.
7. Compatibility with existing application code.

If a schema change is needed:

- Explain the required migration.
- Identify affected models and endpoints.
- Explain data migration requirements.
- Provide a rollback strategy.
- Wait for approval before execution.

Never drop tables, delete production records, or reset the database without explicit authorization.
```

## Toggle 39 — Database Backup and Recovery

```text
Create a database backup and recovery strategy for my application.

Analyze the database technology and hosting environment.

Prepare recommendations for:

1. Full backups.
2. Incremental backups where supported.
3. Backup frequency.
4. Backup storage.
5. Encryption.
6. Retention policy.
7. Recovery procedures.
8. Backup verification.
9. Disaster recovery.
10. Recovery testing.

Do not execute backup or restoration commands without my approval.

Never overwrite existing backups.
```

---

# PART 11 — Security

## Toggle 40 — Complete Security Audit

```text
Perform a complete security audit of my full-stack application.

Frontend security:
- Sensitive data exposure.
- Unsafe rendering.
- XSS risks.
- Token storage.
- Insecure API usage.
- Client-side access-control assumptions.

Backend security:
- Authentication vulnerabilities.
- Authorization weaknesses.
- SQL/NoSQL injection.
- Input validation.
- Rate limiting.
- CORS configuration.
- Security headers.
- File upload security.
- Session management.

Infrastructure:
- Exposed environment variables.
- API key handling.
- Dependency vulnerabilities.
- Production configuration.
- Logging of sensitive information.

For each confirmed finding, provide:
- Severity.
- Affected file.
- Root cause.
- Potential impact.
- Recommended remediation.

Do not print secret values.

Do not modify files during the initial audit.
```

## Toggle 41 — Environment Variable Security

```text
Review how my application manages environment variables and secrets.

Check:

1. Frontend environment variables.
2. Backend environment variables.
3. Database credentials.
4. API keys.
5. Authentication secrets.
6. Deployment configuration.
7. Git tracking of environment files.
8. Secret exposure through frontend builds.

Ensure private secrets are only used on the server side.

Identify any exposed credentials without printing their values.

Recommend secure configuration changes.

Do not modify production secrets or environment settings without my approval.
```

## Toggle 42 — Dependency Security

```text
Audit all project dependencies for security and maintenance issues.

Check both frontend and backend dependency files.

Identify:
- Known vulnerabilities.
- Outdated dependencies.
- Deprecated packages.
- Unmaintained packages.
- Unnecessary dependencies.
- Version conflicts.

For each issue, recommend a safe update strategy.

Do not blindly upgrade every package.

Before making updates, explain breaking-change risks.

After approved updates, run tests and verify the production build.
```

## Toggle 43 — Authorization and Access Control

```text
Audit authorization and access control across my application.

Verify:

1. Users can only access authorized resources.
2. Protected API routes enforce permissions server-side.
3. Role-based permissions are consistent.
4. Resource ownership is validated.
5. Admin-only functionality is protected.
6. Frontend restrictions are not treated as security boundaries.
7. Unauthorized requests return appropriate responses.

Identify insecure direct object reference risks and privilege-escalation possibilities.

Do not change user permissions or production data.

Wait for approval before implementing major security changes.
```

---

# PART 12 — Performance

## Toggle 44 — Complete Performance Audit

```text
Perform a performance audit of my entire application.

Frontend:
- Initial page load.
- JavaScript bundle size.
- Component rendering.
- Unnecessary re-renders.
- Image loading.
- Lazy loading.
- Code splitting.
- Network requests.

Backend:
- API response times.
- Database query performance.
- Memory usage.
- CPU usage.
- Caching opportunities.
- Request processing.

Full-stack:
- Data transfer size.
- API communication.
- Pagination.
- Duplicate requests.
- Slow workflows.

Identify measurable performance problems.

Provide a prioritized optimization plan.

Do not modify any files during the initial audit.
```

## Toggle 45 — Frontend Optimization

```text
Optimize the frontend for speed and responsiveness.

Analyze:

1. Component rendering.
2. Unnecessary re-renders.
3. Bundle size.
4. Lazy loading.
5. Code splitting.
6. Image optimization.
7. Font loading.
8. Asset loading.
9. API request duplication.
10. State management efficiency.

Implement only improvements that provide a meaningful benefit.

Preserve existing behavior and UI design.

Run the production build and relevant tests.

Report measurable improvements where available.
```

## Toggle 46 — Backend Optimization

```text
Optimize my backend for better performance.

Analyze:

1. API response time.
2. Database queries.
3. Connection pooling.
4. Middleware overhead.
5. Synchronous blocking operations.
6. Caching.
7. Pagination.
8. Large payloads.
9. Memory usage.
10. Error-handling overhead.

Implement safe optimizations based on actual bottlenecks.

Avoid unnecessary complexity.

Preserve existing API contracts wherever possible.

Run relevant tests and report performance measurements.
```

## Toggle 47 — Caching Strategy

```text
Analyze caching opportunities across my full-stack application.

Consider:

1. Browser caching.
2. Static asset caching.
3. API response caching.
4. Database query caching.
5. Server-side caching.
6. Cache invalidation.
7. User-specific data isolation.
8. Stale data risks.

Recommend an appropriate caching strategy for my existing architecture.

Do not cache sensitive or user-specific information insecurely.

Explain the trade-offs before implementation.

Wait for approval before introducing caching infrastructure.
```

---

# PART 13 — Testing & QA

## Toggle 48 — Testing Audit

```text
Analyze the testing setup of my entire full-stack application.

Identify:

1. Unit tests.
2. Component tests.
3. Integration tests.
4. API tests.
5. Database tests.
6. Authentication tests.
7. End-to-end tests.
8. Regression tests.

Check:
- Existing testing frameworks.
- Test configuration.
- Test coverage.
- Missing test cases.
- Unreliable or duplicated tests.

Provide a testing improvement plan.

Do not modify any files during the initial audit.
```

## Toggle 49 — Unit Tests

```text
Create meaningful unit tests for my application.

First identify the existing testing framework and conventions.

Prioritize:
1. Utility functions.
2. Business logic.
3. Backend services.
4. Validation functions.
5. Frontend components.
6. State management logic.

Test:
- Normal cases.
- Edge cases.
- Invalid inputs.
- Expected errors.
- Boundary conditions.

Do not modify application behavior to make tests pass.

Run the tests and report the results.
```

## Toggle 50 — API Integration Tests

```text
Create and run integration tests for my backend APIs.

Verify:

1. Successful requests.
2. Invalid request bodies.
3. Missing required fields.
4. Authentication failures.
5. Authorization failures.
6. Missing resources.
7. Database errors.
8. Unexpected server errors.
9. Correct HTTP status codes.
10. Correct response structures.

Use the existing test framework.

Use a safe test environment and test database.

Never run destructive tests against production data.

Report all passed and failed tests.
```

## Toggle 51 — End-to-End Tests

```text
Create an end-to-end testing strategy for my application.

Identify the most important user workflows.

Test the complete journey:

1. Open application.
2. Navigate to relevant pages.
3. Submit forms.
4. Authenticate.
5. Perform user actions.
6. Send API requests.
7. Process backend operations.
8. Verify database results using a safe test environment.
9. Display correct UI responses.
10. Handle failures.

Use the existing testing tools where possible.

Do not use real customer accounts or production data.

Report failed workflows and their root causes.
```

## Toggle 52 — Regression Testing

```text
Perform regression testing after the latest code changes.

Identify all modified files and their dependencies.

Verify:

1. Existing features.
2. Related API endpoints.
3. Authentication.
4. Database interactions.
5. Forms and validation.
6. Navigation.
7. Responsive layouts.
8. Error handling.
9. Existing tests.
10. Production build.

Identify any functionality that has broken because of recent changes.

Do not make unrelated modifications.

Report the results clearly.
```

## Toggle 53 — Fix Failing Tests

```text
Investigate all failing tests in my application.

For each failure:

1. Identify the failing test.
2. Inspect the relevant implementation.
3. Determine whether the test or application is incorrect.
4. Find the root cause.
5. Recommend the smallest correct fix.
6. Implement the fix.
7. Rerun the affected test.
8. Run the complete relevant test suite.

Do not delete tests or weaken assertions just to achieve a passing result.

Report any remaining failures honestly.
```

---

# PART 14 — Git & Code Management

## Toggle 54 — Check Git Status

```text
Review my project's current Git status before making changes.

Check:

1. Current branch.
2. Modified files.
3. Untracked files.
4. Staged files.
5. Existing commits.
6. Merge conflicts.
7. Existing ignored files.

Identify whether there are uncommitted changes that must be preserved.

Do not reset, discard, overwrite, or commit anything.

Explain the current Git state and recommend a safe next step.
```

## Toggle 55 — Create Safe Backup

```text
Help me create a safe backup before making significant changes.

First inspect the Git status.

Check whether important files are already tracked.

Ensure environment variables, API keys, credentials, and private files are excluded.

If uncommitted changes exist, explain how they can be preserved.

Recommend a safe Git commit or backup strategy.

Do not discard existing changes.

Do not push anything to a remote repository without my approval.
```

## Toggle 56 — Review Changes

```text
Review all changes made during the current development session.

Analyze:

1. Modified files.
2. New files.
3. Deleted files.
4. Changed dependencies.
5. Configuration changes.
6. Potential security issues.
7. Unintended changes.
8. Test results.

Check whether the changes are complete and consistent.

Identify anything that should not be committed.

Do not commit automatically.

Present a concise review and wait for my approval.
```

## Toggle 57 — Create Git Commit

```text
Prepare a Git commit for the approved project changes.

Before committing:

1. Review Git status.
2. Review the staged changes.
3. Check for secrets.
4. Check for generated files that should not be committed.
5. Confirm tests and build status.
6. Verify the commit contains only intended changes.

Suggest a clear, meaningful commit message.

Wait for my approval before running git commit.

Do not push to a remote repository unless I explicitly authorize it.
```

## Toggle 58 — Resolve Git Conflicts

```text
Help me investigate and resolve the current Git merge conflict.

Requirements:

1. Identify all conflicted files.
2. Explain the conflicting changes.
3. Compare both versions.
4. Identify the intended functionality.
5. Recommend the safest resolution.
6. Preserve unrelated changes.
7. Run relevant tests after resolution.

Do not automatically choose one side of every conflict.

Do not run git reset --hard, force push, or destructive Git commands.

Wait for my approval before finalizing conflict resolution.
```

## Toggle 59 — Work Safely Across Two Accounts

```text
Help me maintain a safe development workflow when working on the same local project using different Claude accounts.

Requirements:

1. Both accounts must follow the same CLAUDE.md.
2. Keep project documentation independent of account history.
3. Use ACCOUNT_HANDOFF.md to transfer unfinished work.
4. Use Git to track changes.
5. Check Git status before starting work.
6. Avoid editing the same files simultaneously.
7. Review changes before switching accounts.
8. Preserve uncommitted changes.
9. Run relevant tests after continuing work.
10. Never assume previous conversation history is available.

Recommend a simple workflow to avoid conflicts and duplicated work.

Do not reset or discard project changes.
```

---

# PART 15 — Production & Deployment

## Toggle 60 — Production Readiness Audit

```text
Perform a complete production readiness audit of my full-stack application.

Review:

1. Frontend production build.
2. Backend production configuration.
3. Environment variables.
4. Database connectivity.
5. Authentication.
6. API configuration.
7. CORS settings.
8. Security headers.
9. Error handling.
10. Logging.
11. Performance.
12. Static assets.
13. Deployment configuration.
14. Domain and HTTPS requirements.
15. Health checks.

Identify everything that must be fixed before production deployment.

Do not deploy or modify production settings.

Provide a prioritized production readiness report.
```

## Toggle 61 — Prepare Vercel Deployment

```text
Analyze my project and prepare it for deployment on Vercel.

First determine whether my frontend and backend architecture is compatible with Vercel.

Review:

1. Framework detection.
2. Build commands.
3. Output directories.
4. API routes.
5. Serverless function compatibility.
6. Environment variables.
7. Routing configuration.
8. Static assets.
9. Build errors.
10. Deployment configuration.

Check whether frontend and backend should be deployed together or separately.

Do not assume the project structure.

Do not expose secrets.

First provide the required configuration changes and deployment steps.

Wait for approval before modifying deployment files.
```

## Toggle 62 — Environment Variables for Deployment

```text
Prepare my application for production environment configuration.

Identify all required environment variables across frontend and backend.

For each variable, document:
- Variable name.
- Purpose.
- Which side uses it.
- Whether it is public or private.
- Whether it is required in production.

Requirements:
1. Keep private API keys server-side.
2. Do not expose database credentials.
3. Do not hardcode secrets.
4. Do not print actual secret values.
5. Identify missing production configuration.
6. Explain how to configure variables on my hosting platform.

Do not modify real production environment variables.
```

## Toggle 63 — Build Verification

```text
Verify that my complete application can be built successfully for production.

Check both frontend and backend.

Requirements:

1. Inspect available build scripts.
2. Verify dependency installation status.
3. Run the appropriate production build commands.
4. Identify TypeScript errors, if applicable.
5. Identify compilation errors.
6. Identify missing dependencies.
7. Identify configuration problems.
8. Check build output.
9. Report warnings separately from errors.

Do not hide build errors.

Do not delete files or change dependencies unnecessarily.

Report the exact commands executed and their results.
```

## Toggle 64 — Deployment Checklist

```text
Create a complete deployment checklist for my application.

Include:

- Code review.
- Git backup.
- Frontend build.
- Backend build.
- Database configuration.
- Environment variables.
- Authentication configuration.
- API configuration.
- CORS.
- HTTPS.
- Security checks.
- Domain configuration.
- Deployment.
- Post-deployment testing.
- Error monitoring.
- Rollback strategy.

Adapt the checklist to my actual hosting platform and project architecture.

Do not deploy automatically.

Make the checklist actionable and sequential.
```

## Toggle 65 — Post-Deployment Verification

```text
Help me verify my application after production deployment.

Check:

1. Homepage availability.
2. Frontend routing.
3. Backend health.
4. API endpoints.
5. Authentication.
6. Database connectivity.
7. Form submissions.
8. Main user workflows.
9. Static assets.
10. Error handling.
11. Mobile responsiveness.
12. Security configuration.

Use safe, non-destructive checks.

Do not expose production secrets or modify production data.

Report any deployment problems and recommend fixes.
```

---

# PART 16 — Final Review & Maintenance

## Toggle 66 — Professional Code Review

```text
Act as a senior full-stack software engineer and perform a professional code review of my entire project.

Review both frontend and backend.

Evaluate:

1. Code quality.
2. Architecture.
3. Maintainability.
4. Security.
5. Performance.
6. API design.
7. Database design.
8. Error handling.
9. Testing.
10. Responsive design.
11. Accessibility.
12. Deployment readiness.

Identify:
- Critical issues.
- High-priority issues.
- Medium-priority issues.
- Low-priority improvements.

For each issue, explain the root cause and recommended solution.

Do not modify files during the initial review.

Provide an honest professional assessment.
```

## Toggle 67 — Remove Unnecessary Code

```text
Analyze my project for unnecessary or unused code.

Look for:

1. Unused imports.
2. Unused variables.
3. Unused components.
4. Unused functions.
5. Duplicate code.
6. Unused dependencies.
7. Dead code.
8. Obsolete configuration.
9. Unnecessary files.
10. Unused API endpoints.

Before removing anything:

- Verify that it is genuinely unused.
- Check dynamic imports and references.
- Check routes and external integrations.
- Check whether it is required by the build or deployment system.

Do not delete anything without presenting the proposed changes first.

Run tests after approved cleanup.
```

## Toggle 68 — Improve Maintainability

```text
Improve the long-term maintainability of my full-stack application.

Focus on:

1. Clear naming.
2. Consistent coding conventions.
3. Reusable components.
4. Modular backend services.
5. Clear API contracts.
6. Centralized error handling.
7. Consistent validation.
8. Useful documentation.
9. Appropriate testing.
10. Reduced duplication.

Avoid unnecessary architectural complexity.

Do not change application behavior.

Implement improvements incrementally and verify each change.
```

## Toggle 69 — Project Maintenance Plan

```text
Create a long-term maintenance plan for my application.

Analyze the current project and recommend a schedule for:

1. Dependency updates.
2. Security audits.
3. Database maintenance.
4. Performance checks.
5. Backup verification.
6. Test maintenance.
7. Documentation updates.
8. Error monitoring.
9. Code quality reviews.
10. Deployment verification.

Separate weekly, monthly, and quarterly maintenance activities.

Adapt the recommendations to the actual project architecture.

Do not make changes automatically.
```

## Toggle 70 — Final Project Health Report

```text
Prepare a final project health report for my full-stack application.

Evaluate:

1. Frontend quality.
2. Backend quality.
3. Database health.
4. API reliability.
5. Security.
6. Performance.
7. Testing.
8. Documentation.
9. Maintainability.
10. Deployment readiness.

For each category, provide:
- Current status.
- Verified findings.
- Remaining issues.
- Recommended next steps.

Provide an overall assessment of the project's technical health.

Do not invent test results or claim that unverified features work.

Do not make changes during this assessment.
```

---

# Quick Reference — Account Switching

When Account 1 reaches its usage limit:

**Step 1 — Prepare handoff**

Run [Toggle 05](#toggle-05--before-switching-gmail).

**Step 2 — Check project status**

```bash
git status
```

**Step 3 — Log out**

```text
/logout
```

**Step 4 — Log in to the second account**

```text
/login
```

**Step 5 — Verify account**

```text
/status
```

**Step 6 — Reopen project**

```powershell
cd D:\Projects\my-website
claude
```

**Step 7 — Restore context**

Run [Toggle 07](#toggle-07--continue-after-switching-gmail).

**Step 8 — Continue development**

Continue from the unfinished task.

**Important:**
- Both accounts can access the same local project folder.
- Account conversations are separate.
- Project files remain on your computer.
- Usage allowances remain account-specific.
- Multiple accounts do not guarantee unlimited usage; follow Anthropic's usage policies.

---

# Project Root File Structure

Recommended project structure:

```text
my-project/
│
├── client/
│   ├── src/
│   ├── public/
│   └── package.json
│
├── server/
│   ├── src/
│   ├── routes/
│   ├── controllers/
│   └── package.json
│
├── shared/
│
├── CLAUDE.md
├── ACCOUNT_HANDOFF.md
├── README.md
├── .gitignore
└── .env.example
```

Adapt this to the actual project. Do not create unnecessary folders.

---

# Daily Development Workflow

1. Check Git status.
2. Open the parent project folder.
3. Start Claude Code.
4. Ask Claude to inspect relevant files.
5. Plan the required changes.
6. Implement one feature at a time.
7. Run tests.
8. Review modified files.
9. Commit approved changes.
10. Update documentation.
11. Prepare account handoff before switching Gmail.

---

# Important Development Rules

1. Never share passwords, API keys, or authentication tokens.
2. Never run destructive database commands without explicit approval.
3. Never use `git reset --hard` to solve ordinary problems.
4. Always review changes before committing.
5. Never assume a test passes without running it.
6. Do not let Claude rewrite the entire project unnecessarily.
7. Keep frontend and backend API contracts synchronized.
8. Preserve existing functionality.
9. Maintain CLAUDE.md across accounts.
10. Maintain ACCOUNT_HANDOFF.md when switching accounts.
11. Use Git backups before significant changes.
12. Always verify production builds before deployment.

---

**End of Claude Code Master Handbook** — Version 1.0 · Windows + VS Code · Full-Stack Development · 70 prompts
