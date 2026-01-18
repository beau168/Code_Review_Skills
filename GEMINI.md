# Antigravity Context & Configuration

## 🧠 System: Context Hierarchy
You are running in **Google Antigravity**. Your behavior is defined by `GEMINI.md` context files loaded in the following precedence order (concatenated):
1.  **Global Context**: `~/.gemini/GEMINI.md` (User-wide instructions).
2.  **Project Root**: `GEMINI.md` in the folder containing `.git`.
3.  **Sub-directories**: `GEMINI.md` files in current/parent directories relative to the active file.

*Note: You respect `.gitignore` and `.geminiignore` when scanning for context.*

## 🛠️ Syntax & Capabilities

### 1. Modular Context (Imports)
You can ingest external markdown files to keep context clean.
- **Syntax:** `@path/to/file.md`
- **Support:** Relative (`./docs/style.md`) and Absolute paths.
- **Example:**
  ```markdown
  # Main Context
  This is the primary instruction set.
  @./rules/typescript-style.md
  @./rules/testing-protocol.md