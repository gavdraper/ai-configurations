
# Coding Behaviors

As a coding agent you should think thoughly, it's ok for this to take some time. Avoid unnecessary repetition.

ALWAYS exhibit the following behaviors
* write clean code that complies with SOLID principles
* write tests at the most appropriate level adhering where possible to the test pyramid
* NEVER remove a failing test just because you can't make it pass
* if you need to delete a test because its no longer relevant ask me first and tell me the reasons
* create classes in their own files
* If you get stuck please let me know, give me options and ask for my thoughts
* before bringing in a new library ask me first
* If asked to commit ALWAYS do it on a feature branch
* code should be self documenting, comments should not be required

After completing a task ALWAYS do the following
* run a clean build and check it passes, if it doesn't then fix any issues
* run ALL tests not just the ones close to the changes, check they ALL pass and fix any that fail
* run a security review of changes - then fix issues
* run a code review on changes - then fix issues
* run a review of the changes against the task and make sure they cover everything asked

The following tools are available for you to use
* GitHub CLI - Viewing/Creating Issues, Creating PRs
* Curl - Quick testing of endpoints, these are throw away tests and should be created as automated tests in our testing framework where they are something worth keeping

# Workflow
When asked to start a new piece of work that has no plan, if the work has more than a couple of steps then ALWAUS ask if I'd like the initiate the plan workflow, if I say yes then do the following

* Create a unique file in the folder agent-tmp
* In that file breakdown all the steps of your plan and store them as a checklist
* Ask me if I'm happy with the plan

Once the plan is complete if I ask you to start work or continue take the first incomplete item in the plan and start work. As soon as an item is completed mark it as complete in the plan md file. As soon as a phase is completed stop work and ask if I'd like to resume.

Once the work is complete and meets all the requirements of the Behavior section above you may mark the step as complete in the markdown file and stop. 

## Project Overview

Tweeter is a Twitter-like social media application built as a demonstration/learning project. The app uses ASP.NET Core (.NET 9) with Entity Framework Core and SQLite for the backend, and vanilla JavaScript for the frontend.

## Architecture

- **Backend**: ASP.NET Core MVC with Web API controllers
- **Database**: SQLite with Entity Framework Core (Code First approach)
- **Frontend**: Vanilla JavaScript SPA with server-rendered HTML shell
- **Data Models**: User, Post, PostRepost, TrendingTag with EF navigation properties

### Key Components

- `TweeterContext` - EF DbContext with models and relationships
- API Controllers in `Controllers/Api/` - RESTful endpoints for posts, users, trending
- Models with DTOs for clean API responses
- Frontend state management and DOM rendering in `wwwroot/js/app.js`

## Commands

- **Build**: `dotnet build`
- **Clean**: `dotnet clean`
- **Run**: `dotnet run` (starts on https://localhost:5001)
- **Test**: `dotnet test`

## Database

- Uses SQLite (`tweeter.db`) with automatic database creation and seeding
- No migrations - uses `EnsureCreatedAsync()` for demo purposes
- Seed data includes demo users and initial posts

## Development Guidelines

From the GitHub Copilot instructions:

### Coding Standards
- Write clean code following SOLID principles
- Create classes in their own files
- Code should be self-documenting without excessive comments
- Always use feature branches for commits
- Ask before introducing new libraries

### Testing & Quality
- Write tests at appropriate levels following the test pyramid
- Never remove failing tests - fix them or ask first
- Run full test suite after changes
- Perform security and code reviews of changes

### Workflow
For complex tasks (3+ steps):
1. Create plan file in `agent-tmp/` folder with checklist
2. Get approval before starting work
3. Complete tasks incrementally
4. Mark completed items in the plan

### Post-Task Requirements
After completing any task:
1. Run clean build and fix any issues
2. Run ALL tests and fix failures
3. Security review of changes
4. Code review of changes
5. Verify all task requirements are met

## Available Tools
- GitHub CLI for issues and PRs
- cURL for endpoint testing (create proper automated tests for anything worth keeping)