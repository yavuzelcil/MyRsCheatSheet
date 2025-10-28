# MyRs Cheat Sheet 🤗

A comprehensive Rust programming language cheat sheet in LaTeX format, designed as a compact two-column reference guide.

## 📋 Contents

- **Basics**: Variables, types, mutability, shadowing
- **Macros**: Declarative and procedural macros with examples
- **Ownership & Borrowing**: Core Rust concepts
- **Generics**: Functions, structs, and enums
- **Traits**: Definitions, implementations, and trait bounds
- **Lifetimes**: Annotations, elision rules, and static lifetimes
- **Smart Pointers**: Box, Rc, and more
- **Error Handling**: Result types and custom errors
- **Cargo Commands**: Quick reference for common operations

## 🚀 Quick Start

### Building the PDF

In the `MyRsCheatSheet` directory:

```bash
make pdf          # Generates cheatsheet.pdf (two-column, single-page layout)
make pdf-2up      # Generates two-up.pdf (page 1 on left, page 2 on right)
make clean        # Remove auxiliary files
```

### Requirements

- **Recommended**: `latexmk` + `xelatex`
- **Alternatives**: `pdflatex` or `tectonic`

The build system automatically detects available LaTeX compilers.

## 📐 Layout Details

- **Format**: Two-column A4 (`extarticle[8pt, a4paper, twocolumn]`)
- **Font**: 8pt for maximum information density
- **Margins**: Narrow margins optimized for reference sheets
- **Code Blocks**: Automatic line breaking with `listings` package
- **No Split**: Code examples stay together (won't break across columns/pages)

## ✏️ How to Edit

1. Edit content directly in `cheatsheet.tex`
2. Keep section titles and lists short and dense
3. Use the `Code` environment for code examples:

```latex
\begin{Code}
// Your Rust code here
fn main() {
    println!("Hello, world!");
}
\end{Code}
```

## 🎨 Features

- ✅ **Auto-build on save** (with LaTeX Workshop in VS Code)
- ✅ **SyncTeX support** (PDF ↔ code synchronization)
- ✅ **Syntax highlighting** for Rust code
- ✅ **Custom emojis** (TikZ-based hugging face 🤗)
- ✅ **File naming conventions** with visual indicators (✓/✗)

## 📄 Two-Up Layout

The `two-up.pdf` displays pages side-by-side:
- Perfect for printing as a booklet
- Page 1 on left, Page 2 on right
- Ideal for double-sided reference sheets

## 🛠️ Project Structure

```
MyRsCheatSheet/
├── cheatsheet.tex      # Main LaTeX source
├── Makefile           # Build automation
├── .latexmkrc         # LaTeX build configuration
├── .gitignore         # Git ignore rules
├── README.md          # This file
└── cheatsheet.pdf     # Generated output
```

## 📦 Dependencies

LaTeX packages used:
- `geometry` - Page layout
- `listings` - Code syntax highlighting
- `xcolor` - Colors for code
- `tikz` - Custom graphics (emoji)
- `hyperref` - PDF links
- `pifont` - Special symbols (✓/✗)

## 🤝 Contributing

Feel free to:
- Report issues
- Submit pull requests
- Suggest new content
- Improve existing examples

## 📝 License

This project is open source. Feel free to use, modify, and distribute.

## 🎯 Tips

- Use `Cmd/Ctrl + Click` in PDF to jump to source code (SyncTeX)
- Use `Cmd/Ctrl + Alt + J` to jump from code to PDF location
- Auto-build triggers on every save in VS Code
- Keep code examples concise for better readability

---

**Author**: Yavuz Elcil  
**Built with**: LaTeX, TikZ, and ❤️ for Rust
