# My Personal Agent Skills

A collection of custom agents and skills that extend Claude and OpenCode with specialized capabilities for code quality, documentation, debugging, refactoring, and development workflows.

## Overview

This repository contains reusable agent configurations and skills that enhance coding productivity by automating common development tasks. Each agent specializes in a specific role, from code reviewing to documentation, while skills provide cross-cutting capabilities for code analysis and explanation.

---

## Agents

Agents are specialized assistants designed for specific development roles. They come with pre-configured instructions, tools, and best practices.

### Quick Overview

| Agent                       | Description                                                                  | Purpose                                                                 |
| --------------------------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| 🔍 **Code Reviewer**        | Expert code reviewer for quality, maintainability, security & best practices | Conduct thorough code reviews across multiple dimensions before merging |
| 🐛 **Debugger**             | Root cause analysis specialist for error resolution & test failures          | Quickly identify and fix bugs in React, TypeScript & full-stack apps    |
| 💬 **Code Commenter**       | JSDoc documentation specialist for code clarity                              | Improve code readability with comprehensive documentation comments      |
| ♻️ **Refactorer**           | Architecture improvement specialist for duplication & maintainability        | Improve code quality through strategic refactoring & best practices     |
| 📚 **Documentation Writer** | Technical documentation specialist for architecture & workflows              | Create comprehensive project documentation & system guides              |
| 📋 **Task Recap**           | Work summarizer for completed tasks & progress                               | Provide clear summaries of development progress & changes               |

---

## Skills

Skills are reusable capabilities that provide specialized functionality for code analysis, explanation, and quality assurance. Skills can be used independently or combined with agents.

### Quick Overview

| Skill                               | Description                                                                                                | Purpose                                                          |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 🔬 **Code Review and Quality**      | Multi-axis code review across 5 dimensions (correctness, readability, architecture, security, performance) | Ensure every change maintains or improves overall code health    |
| 🧹 **Code Simplification**          | Simplifies code by reducing complexity while preserving exact behavior                                     | Make code easier to read, understand, modify, and debug          |
| 🐛 **Debugging and Error Recovery** | Guides systematic root-cause debugging through structured triage and error analysis                        | Find and fix root causes reliably instead of guessing            |
| 💡 **Explain Code**                 | Visual diagrams, analogies & step-by-step walkthroughs                                                     | Make code comprehensible through multiple explanation approaches |

---

## How to Use

### With Claude Code - Quick Start

1. **Clone the repository:**

   ```bash
   git clone https://github.com/narinsak-u/my-personal-agent-skills.git
   cd my-personal-agent-skills
   ```

2. **Copy files to Claude Code:**
   - **Mac/Linux:**
     ```bash
     cp -r agents/* ~/.claude/agents/
     cp -r skills/* ~/.claude/skills/
     ```
   - **Windows:**
     ```bash
     xcopy agents\* %APPDATA%\.claude\agents\ /E /I
     xcopy skills\* %APPDATA%\.claude\skills\ /E /I
     ```

3. **Restart Claude Code** in VS Code

4. **Start using agents:**
   - Open Claude Code chat panel
   - Select an agent from the dropdown
   - Ask your question or paste code
   - Skills auto-activate when relevant

### With OpenCode - Quick Start

1. **Clone the repository:**

   ```bash
   git clone https://github.com/narinsak-u/my-personal-agent-skills.git
   cd my-personal-agent-skills
   ```

2. **Copy files to OpenCode:**

   ```bash
   cp -r agents/* ~/.opencode/agents/
   cp -r skills/* ~/.opencode/skills/
   ```

3. **Restart OpenCode**

4. **Start using agents:**
   - Select agent from dropdown or mention it directly: "Using the Code Reviewer agent..."
   - Skills auto-activate based on your prompt

### Quick Command Reference

| Task            | Command/Action                                                            |
| --------------- | ------------------------------------------------------------------------- |
| Review code     | Select Code Reviewer → paste code                                         |
| Debug error     | Select Debugger → paste error                                             |
| Add comments    | Select Code Commenter → paste file                                        |
| Refactor        | Select Refactorer → describe duplication                                  |
| Document        | Select Documentation Writer → describe what to document                   |
| Summarize       | Select Task Recap → describe period                                       |
| Understand code | Ask "how does this work?" (auto-triggers Explain Code)                    |
| Quality check   | Request "comprehensive code review" (auto-triggers Code Review & Quality) |

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
