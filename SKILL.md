---
name: Industry Standard Humanized Coding
description: Forces the agent to write pure, professional, industry-standard code devoid of any AI-like narrative, enthusiasm, or verbosity.
---

# Industry Standard Humanized Coding

When writing, modifying, or generating code, you MUST strictly adhere to the following rules to ensure the codebase remains a pure, production-grade, human-engineered repository. 

Violating these rules breaks the illusion of human engineering and degrades the quality of the codebase.

## 1. Zero AI Narrative & Enthusiasm
- **BANNED WORDS in code/comments:** "ultra-fast", "massive", "commencing", "trivial", "successfully", "boom", "voila", "magic".
- Do NOT apologize, chatter, or explain your reasoning inside the code.
- Do NOT write enthusiastic docstrings. (e.g., *BAD:* `"""Ultra-fast generation loop!"""` *GOOD:* `"""Speculative generation loop."""`)

## 2. Silence is Golden (No Decorative Outputs)
- **NEVER** use `print()` for decorative banners, progress bars, or UI emulation.
- **BANNED:** `print("===========================")`
- **BANNED:** `print("[1] Building Architecture...")`
- **BANNED:** `print(" -> Architecture built successfully!")`
- If you need to log state, use the standard `logging` module (e.g., `logger.info()`, `logger.debug()`), and format the logs strictly like a production server.

## 3. Pure Functional Comments Only
- Code files are exclusively for code.
- Use simple `# ...` comments ONLY to describe *what* a complex line of code functionally does if it is not immediately obvious to a senior engineer.
- Do NOT explain *why* an architecture was chosen inside the code file. 

## 4. Offload Explanations to `papersdo/`
- If the user requests an explanation of a complex algorithm or architecture, **DO NOT** put the explanation in the code.
- Instead, create an `explanation.md` file inside a separate directory named `papersdo/` at the root of the project.
- Keep the theoretical math, justifications, and architectural diagrams entirely inside `papersdo/explanation.md`.

## 5. Professional Structure
- Write modular, DRY (Don't Repeat Yourself) code.
- Use standard naming conventions (e.g., `snake_case` for Python functions, `PascalCase` for classes).
- Emulate the clean, minimalist style of major open-source repositories (like Jax, Grok, or PyTorch core).
