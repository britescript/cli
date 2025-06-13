# @britescript/cli

The official command-line interface for Britescript.

## Installation

```bash
# Install globally
bun install -g @britescript/cli

# Or use via package manager
bun add -D @britescript/cli
```

## Usage

```bash
# Get help
brite --help

# Create new project
brite init my-project

# Build entire project (NEW!)
brite build

# Compile individual .bs files
brite compile file.bs

# Run .bs files directly
brite run file.bs

# Interactive REPL
brite repl

# Show version
brite --version
```

## Commands

### `brite init`
Create a new Britescript project with example files and configuration.

```bash
brite init my-project
cd my-project
```

### `brite build` ⭐ **NEW**
Build entire Britescript projects professionally with configuration support.

```bash
# Build project (replaces custom build scripts!)
brite build

# Build and watch for changes
brite build --watch

# Use custom config file
brite build --config custom.toml
```

**Configuration** in `bunfig.toml`:
```toml
[britescript]
srcDir = "src"      # Source directory (default: "src")
outDir = "build"    # Output directory (default: "build")
target = "bun"      # Target runtime (default: "bun")
minify = false      # Minify output (default: false)
```

### `brite compile`
Compile individual Britescript (.bs) files to TypeScript.

```bash
# Compile to TypeScript
brite compile file.bs

# Custom output file
brite compile file.bs -o output.ts

# Watch for changes
brite compile file.bs --watch
```

### `brite run`
Execute Britescript files directly without manual compilation.

```bash
# Run once
brite run file.bs

# Watch and re-run on changes
brite run file.bs --watch

# Silent mode
brite run file.bs --silent

# Debug mode
brite run file.bs --debug
```

### `brite repl`
Start an interactive Britescript REPL (Read-Eval-Print Loop).

```bash
# Start REPL
brite repl

# Show TypeScript compilation
brite repl --typescript
```

REPL commands:
- `.help` - Show help
- `.exit` - Exit REPL
- `.clear` - Clear screen
- `.ts` - Toggle TypeScript output
- `.version` - Show version

## Features

- 🚀 **Zero Setup** - No configuration required
- 📦 **Project Templates** - Quick project initialization
- 🔄 **File Watching** - Auto-compilation and execution
- 🛠 **Interactive REPL** - Test code snippets quickly
- 🎯 **TypeScript Output** - Clean, readable compiled code
- 📱 **Cross Platform** - Works on macOS, Linux, and Windows

## Development

```bash
# Clone the repository
git clone https://github.com/britescript/cli.git
cd cli

# Install dependencies
bun install

# Run in development mode
bun run dev

# Build for production
bun run build

# Run tests
bun test
```

## Requirements

- **Bun** >= 1.0.0
- **britescript** package (automatically installed)

## Related Repositories

- [`britescript`](https://github.com/britescript/britescript) - Core compiler and runtime

## License

MIT License - see [LICENSE](LICENSE) file for details.