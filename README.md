# My Personal Agent Skills

A collection of custom agents and skills that extend Claude and OpenCode with specialized capabilities for code quality, documentation, debugging, refactoring, and development workflows.

## Overview

This repository contains reusable agent configurations and skills that enhance coding productivity by automating common development tasks. Each agent specializes in a specific role, from code reviewing to documentation, while skills provide cross-cutting capabilities for code analysis and explanation.

---

## Agents

Agents are specialized assistants designed for specific development roles. They come with pre-configured instructions, tools, and best practices.

### 🔍 Code Reviewer

**Description:** Expert code reviewer specializing in quality, maintainability, security, and best practices for React/TypeScript applications.

**Purpose:** Conduct thorough code reviews across multiple dimensions before merging changes to ensure high code quality standards.

**Capabilities:**

- Quality assessment (clarity, readability, error handling, test coverage)
- Maintainability review (component structure, TypeScript types, hooks, re-render optimization)
- Security analysis (XSS vulnerabilities, data exposure, authentication logic, input validation)
- Best practices compliance (TypeScript strict mode, React patterns, accessibility, styling consistency)

**Use When:** Code changes are submitted for review, pull requests need evaluation, or you need quality assessment before merging.

---

### 🐛 Debugger

**Description:** Expert debugging specialist for root cause analysis, error resolution, and test failures in React, TypeScript, and full-stack applications.

**Purpose:** Quickly identify and fix bugs while understanding their root causes and preventing future occurrences.

**Capabilities:**

- Runtime error resolution (stack traces, type errors, undefined references)
- Test failure debugging (unit/integration tests, assertion failures, mocking issues)
- State management troubleshooting (Redux state problems, stale data, mutations)
- API and integration debugging (network errors, auth failures, response mismatches)
- UI bug resolution (rendering issues, event handling, form validation)

**Use When:** You encounter errors, tests are failing, or need to trace and fix bugs in your codebase.

---

### 💬 Code Commenter

**Description:** Documentation specialist that adds comprehensive JSDoc-style comments to code for clarity and maintainability.

**Purpose:** Improve code readability and maintainability by adding clear, comprehensive documentation to all code elements.

**Capabilities:**

- Function & method documentation (purpose, parameters, return values, examples)
- React component documentation (rendering logic, props, behavior, usage)
- Custom hooks documentation (functionality, dependencies, return values)
- Utility & helper documentation (purpose, edge cases, parameters)
- Complex logic explanation (algorithms, business logic, non-obvious patterns)
- API service documentation (endpoints, request/response shapes, error handling)

**Use When:** You want to improve code documentation, add JSDoc comments, or make code more understandable for future developers.

---

### ♻️ Refactorer

**Description:** Code refactoring specialist focused on improving architecture, reducing duplication, and applying best practices to React/TypeScript codebases.

**Purpose:** Improve code quality through strategic refactoring while maintaining backward compatibility and respecting existing patterns.

**Capabilities:**

- Code duplication elimination (extract common patterns, consolidate repeated logic)
- Architectural improvements (separation of concerns, cleaner dependencies)
- Maintainability enhancement (naming, organization, extensibility)
- Best practices application (modern React patterns, TypeScript improvements)
- Code consistency enforcement (align with project conventions)
- Testability improvement (easier testing and mocking)

**Use When:** You need to clean up code structure, remove duplication, improve maintainability, or modernize existing code.

---

### 📚 Documentation Writer

**Description:** Technical documentation specialist that writes comprehensive project documentation including architecture, workflows, and system guides.

**Purpose:** Create clear, comprehensive documentation that helps developers understand and work with complex systems.

**Capabilities:**

- Project overview documentation (architecture, systems, tech stack)
- System and domain guides (detailed feature documentation)
- Data workflow documentation (how data flows through the application)
- Integration documentation (third-party services and APIs)
- API documentation (endpoints, request/response formats, authentication)
- Database schema documentation (data models and relationships)
- Setup and installation guides (development environment configuration)

**Use When:** You need to document a new project, system architecture, or create guides for other developers.

---

### 📋 Task Recap

**Description:** Work summarizer that recaps completed tasks, features, and progress through git history and code changes.

**Purpose:** Provide clear summaries of development progress, completed work, and changes made during a period.

**Capabilities:**

- Work completion recap (features, bug fixes, refactoring)
- Git history analysis (recent commits, branches, pull requests)
- Code change summary (files affected, scope of modifications)
- Progress tracking (accomplishments over time periods)
- Feature highlights (new capabilities and how they work)
- Release notes generation (summary suitable for changelogs)

**Use When:** You need to summarize work done, generate progress reports, or create release notes.

---

## Skills

Skills are reusable capabilities that provide specialized functionality for code analysis, explanation, and quality assurance. Skills can be used independently or combined with agents.

### 🔬 Code Review and Quality

**Description:** Conducts multi-axis code review across five critical dimensions: correctness, readability, architecture, security, and performance.

**Purpose:** Ensure every change maintains or improves overall code health before it enters the main branch.

**When to Use:**

- Before merging any PR or change
- After completing a feature implementation
- When evaluating code written by yourself or another agent
- When refactoring existing code
- After any bug fix (review the fix and regression test)

**Review Dimensions:**

1. **Correctness** - Does it do what it claims? Edge cases? Error handling?
2. **Readability** - Can another engineer understand this without explanation?
3. **Architecture** - Is it well-organized with proper separation of concerns?
4. **Security** - Are there vulnerabilities? Is data handled safely?
5. **Performance** - Are there efficiency issues or unnecessary operations?

---

### 💡 Explain Code

**Description:** Explains code through visual diagrams, analogies, and step-by-step walkthroughs to make complex logic understandable.

**Purpose:** Make code comprehensible through multiple explanation approaches for different learning styles.

**When to Use:**

- When explaining how code works
- Teaching about a codebase to new developers
- When the user asks "how does this work?"
- Making complex algorithms or patterns understandable
- Creating documentation for tricky logic

**Explanation Approach:**

1. Start with an everyday analogy
2. Draw ASCII art diagrams showing flow/structure
3. Walk through the code step-by-step
4. Highlight common gotchas and misconceptions

---

## How to Use with Claude Code

### Setup Instructions

1. **Install Claude Code Extension:**
   - Install the Claude Code extension for VS Code from the marketplace
   - Ensure you have access to Claude and valid API credentials configured

2. **Copy Agent Files:**

   ```bash
   # Copy agent files to Claude Code's agents directory
   cp -r agents/* ~/.claude/agents/

   # Or on Windows:
   # xcopy agents\* %APPDATA%\.claude\agents\ /E /I
   ```

3. **Copy Skill Files:**

   ```bash
   # Copy skill files to Claude Code's skills directory
   cp -r skills/* ~/.claude/skills/

   # Or on Windows:
   # xcopy skills\* %APPDATA%\.claude\skills\ /E /I
   ```

4. **Restart Claude Code:**
   - Reload the VS Code window or restart Claude Code
   - Custom agents and skills will now be available

### Using Custom Agents

1. **Access Agents:**
   - Open Claude Code chat panel
   - Look for your custom agents in the agent selector dropdown
   - Select the agent that matches your task

2. **Agent Usage Examples:**

   **Code Reviewer Agent:**

   ```
   In Claude Code: Review this code for quality and best practices
   ```

   Select the "Code Reviewer" agent from the dropdown.

   **Debugger Agent:**

   ```
   In Claude Code: I'm getting this error... [paste error]
   ```

   Select the "Debugger" agent to get focused debugging help.

   **Documentation Writer Agent:**

   ```
   In Claude Code: Write documentation for this feature
   ```

   Select the "Documentation Writer" agent.

   **Code Commenter Agent:**

   ```
   In Claude Code: Add JSDoc comments to this file
   ```

   Select the "Code Commenter" agent.

   **Refactorer Agent:**

   ```
   In Claude Code: Refactor this code to remove duplication
   ```

   Select the "Refactorer" agent.

   **Task Recap Agent:**

   ```
   In Claude Code: Summarize the work done in this PR
   ```

   Select the "Task Recap" agent.

3. **Using Skills:**
   - Skills are automatically applied when relevant to your request
   - Mention "code review" to trigger the Code Review and Quality skill
   - Ask "how does this work?" to trigger the Explain Code skill
   - Skills enhance agent capabilities and provide specialized analysis

### With OpenCode

#### Setup

1. **Configure OpenCode Integration:**
   - OpenCode uses the same agent/skill infrastructure as GitHub Copilot
   - Place agent files in your OpenCode configuration directory
   - Skills are loaded automatically when available

2. **Selecting Agents:**
   - Use the agent selector dropdown in OpenCode
   - Choose your custom agent before starting a conversation
   - Or mention the agent name directly: "Using the Code Reviewer agent..."

3. **Using Skills in Prompts:**

   ```
   "Please review this code for quality and security. Also look at performance."
   → Automatically triggers: Code Review and Quality skill

   "Explain how this authentication flow works"
   → Automatically triggers: Explain Code skill
   ```

#### Installation

```bash
# 1. Clone this repository
git clone https://github.com/narinsak-u/my-personal-agent-skills.git

# 2. Copy agents to your OpenCode config
cp -r agents/* ~/.opencode/agents/

# 3. Copy skills to your OpenCode config
cp -r skills/* ~/.opencode/skills/

# 4. Restart OpenCode or reload extensions
```

---

## Directory Structure

```
my-personal-agent-skills/
├── agents/                          # Custom agent configurations
│   ├── code-commenter.md           # JSDoc documentation specialist
│   ├── code-reviewer.md            # Multi-axis code quality reviewer
│   ├── debugger.md                 # Root cause analysis & bug fixing
│   ├── documentation-writer.md     # Technical documentation specialist
│   ├── refactorer.md               # Code refactoring & architecture
│   └── task-recap.md               # Work summarization & progress reporting
├── skills/                          # Reusable capabilities
│   ├── code-review-and-quality/    # Multi-dimensional code review
│   │   └── SKILL.md
│   └── explain-code/               # Code explanation with diagrams
│       └── SKILL.md
└── README.md                        # This file
```

---

## Quick Reference

| Need                       | Agent/Skill                 | Command                       |
| -------------------------- | --------------------------- | ----------------------------- |
| Review code before merge   | Code Reviewer               | Select agent, paste code      |
| Fix a bug                  | Debugger                    | Share error stack trace       |
| Add documentation comments | Code Commenter              | Select agent, paste file      |
| Refactor duplicated code   | Refactorer                  | Share duplicate sections      |
| Write architecture docs    | Documentation Writer        | Describe what to document     |
| Understand complex code    | Explain Code skill          | Ask "how does this work?"     |
| Summarize progress         | Task Recap                  | Select agent, describe period |
| Deep code quality review   | Code Review & Quality skill | Request comprehensive review  |

---

## Best Practices

1. **Use the Right Tool:** Match your task to the appropriate agent or skill for best results
2. **Provide Context:** Include file names, line numbers, and error messages for faster resolution
3. **Review Suggestions:** Always review AI-generated suggestions before applying them
4. **Iterate:** Multiple rounds of questioning often produce better results
5. **Combine Skills:** Use multiple agents or skills for comprehensive analysis (e.g., Code Reviewer + Code Review & Quality skill)

---

## Contributing

These are personal agents and skills tailored to specific development workflows. Feel free to fork and customize them for your own use.

---

## License

Personal use. Modify and adapt as needed for your projects.
