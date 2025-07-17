# GEMINI.md

- **MUST use Context7 MCP tool to check documentation before any code-related work**
  - **Always resolve library IDs first** using `mcp__context7__resolve-library-id` before fetching docs
  - **Focus on relevant topics** when using `mcp__context7__get-library-docs` to optimize token usage
  - This ensures access to current documentation beyond Claude's knowledge cutoff
  - This applies to ALL coding tasks: frameworks, APIs, libraries, patterns, and language features
- **MUST use Sequential Thinking MCP tool for complex problem-solving**
  - Use `mcp__sequential-thinking__sequentialthinking` for multi-step analysis, debugging, implementation planning, or any task requiring structured problem-solving
  - Break down complex problems into logical thinking steps
  - Use when uncertain about approach or when multiple solutions exist
