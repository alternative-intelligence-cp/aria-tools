# Contributing to Aria Tools

Thank you for your interest in improving Aria's developer tooling!

## Repository Contents

- **aria-safety/** — Static safety audit tool (C)
- **aria-mcp/** — MCP server for AI-assisted Aria coding (Python)
- **vscode-aria/** — VS Code extension (TextMate grammar, JSON)
- **tree-sitter-aria/** — Tree-sitter grammar
- **emacs/** — Emacs major mode

## Getting Started

1. Fork the repository
2. Clone: `git clone https://github.com/<your-username>/aria-tools.git`
3. Create a branch: `git checkout -b feature/your-change`
4. Make your changes
5. Push and open a Pull Request

## VS Code Extension

The extension lives in `vscode-aria/`. To test changes:

1. Open `vscode-aria/` in VS Code
2. Press `F5` to launch the Extension Development Host
3. Open an `.aria` file to test syntax highlighting

The TextMate grammar is in `syntaxes/aria.tmLanguage.json`. Key scopes:
- Keywords: `func:`, `failsafe`, `pass()`, `fail()`, `till`, `use`
- Types: `int8`–`int128`, `flt32`/`flt64`, `str`, `bool`, `NIL`
- Preprocessor: `%define`, `%macro`, `%ifdef`, `%include`
- Compile-time: `comptime`, `inline`, `noinline`

## aria-safety (C)

```bash
cd aria-safety
make
./aria-safety ../path/to/file.aria
```

## aria-mcp (Python)

```bash
cd aria-mcp
pip install -r requirements.txt
python aria_mcp_server.py
```

## Commit Messages

Use conventional format:

```
type(scope): description

feat(vscode): add comptime keyword highlighting
fix(safety): handle nested borrow scopes
docs(mcp): update tool descriptions
```

## License

This project is licensed under AGPL-3.0. By contributing, you agree to license your contributions under the same terms.
