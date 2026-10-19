# Project Scope and Objectives

## Scope

Build an individual OpenAI agent that helps a student retrieve assignment information, search approved course policies, and calculate grades. The first version is a command-line application with local course data and controlled function tools.

## Objectives

- Reduce the time required to locate routine course information.
- Return answers based on approved data rather than model memory.
- Demonstrate tool routing with at least three distinct tools.
- Protect credentials and student information.
- Provide repeatable tests and version-controlled documentation.

## Deliverables

- Working Python agent using the OpenAI Agents SDK.
- Three tools: assignment lookup, policy search, and calculator.
- Input validation and a basic security guardrail.
- Automated unit tests.
- README with setup and usage instructions.
- Git repository with a documented initial commit.
- Word report with screenshots and implementation evidence.

## Individual roles and responsibilities

Ibrahim Khatib is responsible for project planning, development, tool integration, testing, security review, repository maintenance, and documentation. Because this is an individual assignment, no access coordination between team members is required.

## Out of scope

- Access to a live learning-management system.
- Storage of private student records.
- Automatic grade changes or assignment submissions.
- Production deployment.

## Success criteria

- All three tools return correct results for valid inputs.
- Invalid or unsafe inputs fail safely.
- The agent selects an appropriate tool for the required sample prompts.
- The repository contains no API credentials.

