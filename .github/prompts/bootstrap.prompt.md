---
mode: 'agent'
tools: ['codebase']
description: 'Bootstrap the repository with necessary copilot instructions and prompts.'
---
Your goal is to bootstrap the repository with necessary copilot instructions and prompts. You will need to create a `.github/copilot-instructions.md` file with the following content:

```markdown
# Copilot Instructions
```

You will also need to create a `.github/instructions/general-coding.instructions.md` file with the following content:

```markdown
---
applyTo: "**"
---
# Project general coding standards

## Naming Conventions
- Use PascalCase for component names, interfaces, and type aliases
- Use camelCase for variables, functions, and methods
- Prefix private class members with underscore (_)
- Use ALL_CAPS for constants

## Error Handling
- Use try/catch blocks for async operations
- Implement proper error boundaries in React components
- Always log errors with contextual information
```

You will also need to create a `.github/instructions/typescript-react.instructions.md` file with the following content:

```markdown
---
applyTo: "**/*.ts,**/*.tsx"
---
# Project coding standards for TypeScript and React

Apply the [general coding guidelines](./general-coding.instructions.md) to all code.

## TypeScript Guidelines
- Use TypeScript for all new code
- Follow functional programming principles where possible
- Use interfaces for data structures and type definitions
- Prefer immutable data (const, readonly)
- Use optional chaining (?.) and nullish coalescing (??) operators

## React Guidelines
- Use functional components with hooks
- Follow the React hooks rules (no conditional hooks)
- Use React.FC type for components with children
- Keep components small and focused
- Use CSS modules for component styling
```

You will also need to create a `.github/prompts/update.prompt.md` file with the following content:

```markdown
---
mode: 'agent'
tools: ['githubRepo', 'codebase']
description: 'Update the repository with necessary copilot instructions and prompts.'
---
Your goal is to update the repository with necessary copilot instructions and prompts. You will need to replace the content inside `.github` directory with content in `.github` directory in this repository `https://github.com/vu-bui/copilot-bootstrap` by simply running a terminal command to delete `.github` directory and shallow clone the `.github` directory in the repository.
```
