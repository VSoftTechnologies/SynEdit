<div align="center">
  <img src="Art/SynEditLogo.svg" alt="SynEdit" width="96" />

  # SynEdit

  A fast, syntax-highlighting source code editor control for Delphi.

  [![Delphi: 10.4+](https://img.shields.io/badge/Delphi-10.4%2B-red.svg)](https://www.embarcadero.com/products/delphi)
  [![Platform: Windows](https://img.shields.io/badge/platform-Win32%20%7C%20Win64%20%7C%20ARM64EC-blue.svg)](#requirements)
  [![License: MPL 1.1](https://img.shields.io/badge/license-MPL%201.1%20%2F%20LGPL-lightgrey.svg)](LICENSE)
  [![DPM](https://img.shields.io/badge/DPM-VSoft.SynEdit-green.svg)](https://delphi.dev)
</div>

> This is a fork of the [PyScripter](https://github.com/pyscripter/SynEdit) version of SynEdit. Following the passing of Kiriakos Vlahos, we decided to maintain our own fork so that the control continues to evolve and stay supported. 

---

## Table of contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Requirements](#requirements)
4. [Installation](#installation)
5. [Package names](#package-names)
6. [Demos](#demos)
7. [Documentation](#documentation)
8. [Highlighters](#highlighters)
9. [Contributing](#contributing)
10. [License](#license)
11. [Acknowledgements](#acknowledgements)

---

## Introduction

SynEdit is a syntax-highlighting edit control that is **not** based on the Windows common controls — it is a fully custom-drawn editor written in Object Pascal. It powers editors such as [PyScripter](https://github.com/pyscripter/pyscripter) and many other Delphi applications that need a capable code editing surface.

SynEdit is compatible with both Delphi and C++ Builder; however, this fork is currently developed and tested with **Delphi only**.

## Features

- **Syntax highlighting** — [60+ built-in highlighters](#highlighters) covering most popular languages, plus a multi-highlighter for mixed content (e.g. HTML with embedded scripts).
- **Code folding** — fast, lag-free folding for files with tens of thousands of lines. See [Doc/CodeFolding.md](Doc/CodeFolding.md).
- **Multiple cursors & selections** — VS Code–style multi-caret editing and column/block selection. See [Doc/Multi-caret.md](Doc/Multi-caret.md).
- **Code completion** — completion proposal and parameter hint popups (`SynCompletionProposal`).
- **Search & replace** — incremental search, regular expressions, and scope-aware replace across multiple selections.
- **Spell checking** — built-in `SynSpellCheck` component.
- **Auto-correct** — configurable text replacement as you type (`SynAutoCorrect`).
- **Modern rendering** — DirectWrite-based text rendering (`SynDWrite`) for crisp fonts and high-DPI displays.
- **Word wrap**, **bookmarks**, **line indicators**, a customizable **gutter** with line numbers, and **drag & drop** support.
- **Printing & print preview** with configurable headers, footers and margins.
- **Export** to HTML, RTF and TeX.
- **Data-aware editing** via `SynDBEdit`.

## Requirements

- **RAD Studio / Delphi 10.4 Sydney** or later (tested through **Delphi 13.0**).
- **Platforms:** Win32, Win64, and Win ARM64EC (Delphi 13).

> Code folding and multi-caret editing rely on generic collections and therefore require Delphi 2009 or later. The current packages target 10.4+.

## Installation

### Using [DPM](https://delphi.dev) (recommended)

In your project folder:

```
dpm install VSoft.SynEdit
```

Or install it via the DPM IDE plugin. This adds the `VSoft.SynEdit` package to your project search path. The design-time components are loaded automatically when you open your project in the IDE.

### Manually

1. Add the **Source** and **Source\Highlighters** directories to the IDE's library path or to your project's search path.
2. Open and install the design-time package for your IDE version from the matching folder under [Packages/](Packages/). The IDE will notify you once the components are installed.

## Package names

SynEdit packages follow this naming convention:

| Package          | Description          |
| ---------------- | -------------------- |
| `SynEditDR.bpl`  | Delphi Runtime       |
| `SynEditDD.bpl`  | Delphi Design-time   |

Packages for each supported IDE version live under [Packages/](Packages/) (e.g. `RAD Studio 12.0`, `RAD Studio 13.0`).

## Demos

The [Demos/](Demos/) folder contains sample projects that showcase the main features:

| Demo                       | Demonstrates                                            |
| -------------------------- | ------------------------------------------------------ |
| `EditAppDemos`             | SDI, MDI and workbook-style editor applications        |
| `SimpleIDEDemo`            | A minimal IDE-like editor                              |
| `HighlighterDemo`          | Switching between the built-in highlighters            |
| `Folding`                  | Code folding with JScript, Python and C++ files        |
| `CompletionProposalDemo`   | Code and parameter completion popups                   |
| `SearchReplaceDemo`        | Search & replace, including multiple selections        |
| `SpellCheck`               | The `SynSpellCheck` component                          |
| `PrintDemo`                | Printing and print preview                             |
| `MarkdownViewer`           | Rendering Markdown using SynEdit                       |

## Documentation

- [Code folding](Doc/CodeFolding.md) — adding and using folding support.
- [Multi-caret editing](Doc/Multi-caret.md) — internals, new commands, and compatibility notes.

## Highlighters

SynEdit ships with highlighters for a wide range of languages and file formats, including:

> Pascal/Delphi, C/C++, C#, Java, JavaScript, JSON, Python, Ruby, Perl, PHP, HTML, XML, CSS, SQL, YAML, INI, Batch, Bash/Shell, VB/VBScript, Fortran, Cobol, Haskell, Assembler, TeX, Inno Setup, DOT, LLVM, WebIDL — and many more.

The full set of highlighters lives in [Source/Highlighters/](Source/Highlighters/). You can also combine highlighters with `SynHighlighterMulti` for files that mix languages.

## Contributing

Contributions are welcome! Please open an issue to discuss significant changes before submitting a pull request. Bug reports and feature requests can be filed on the [issue tracker](https://github.com/VSoftTechnologies/SynEdit/issues).

## License

SynEdit is distributed under the **Mozilla Public License 1.1 (MPL 1.1)**. Alternatively, you may use and redistribute it under the terms of the **GNU Lesser General Public License (LGPL) 2.1** or later. See [LICENSE](LICENSE) for details.

## Acknowledgements

SynEdit has a long history and is the work of many contributors over many years. This fork builds directly on the excellent [PyScripter fork](https://github.com/pyscripter/SynEdit) by the late **Kiriakos Vlahos**, whose work advanced this control what it is today.
