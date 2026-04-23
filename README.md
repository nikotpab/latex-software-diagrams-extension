# SoftDiagrams: Unified Software Diagramming for LaTeX

`SoftDiagrams` is a comprehensive LaTeX package designed for software engineers, architects, and researchers to create high-quality, professional UML 2.5 diagrams directly within their LaTeX documents. Leveraging the power of TikZ, it provides a clean and expressive syntax for structural, behavioral, and interaction diagrams.

## Key Features

- **Full UML 2.5 Support**: Implement all 14 standard UML diagrams including Class, Object, Component, Package, Activity, State Machine, Use Case, and more.
- **Modern Aesthetics**: Built-in professional styling with subtle shadows, customizable colors, and clean typography.
- **Easy-to-use Macros**: Simplified commands for complex structures like multi-part class boxes, folder-style packages, and 3D-effect deployment nodes.
- **Highly Customizable**: Full access to underlying TikZ styles and `pgfkeys` for fine-grained control over appearance.
- **Relationship Management**: Predefined styles for associations, generalizations, dependencies, compositions, and aggregations.

## Supported Diagram Types

1.  **Composite Structure** (`\sdPart`, `\sdPort`)
2.  **Deployment** (`\sdNode`)
3.  **Packages** (`\sdPackage`)
4.  **Profile** (`sd profile` style)
5.  **Objects** (`\sdObject`)
6.  **Classes** (`\sdClass`)
7.  **Components** (`\sdComponent`)
8.  **State Machine** (`\sdState`)
9.  **Communication** (`\sdCommNode`, `\sdCommMessage`)
10. **Use Cases** (`\sdActor`, `\sdUseCase`)
11. **Activities** (`\sdActivity`, `\sdDecision`)
12. **Sequence** (`\sdLifeline`, `\sdMessage`)
13. **Timing (Synchronization)** (`\sdTimingLine`)
14. **Interaction Overview** (`\sdFrame`)

## Quick Start

### Installation
Copy `softdiagrams.sty` to your project directory or your local `texmf` folder.

### Basic Usage
Include the package in your preamble:
```latex
\usepackage{softdiagrams}
```

Example Class Diagram:
```latex
\begin{tikzpicture}
    \sdClass{Vehicle}{Vehicle}{Model}{+ start(): void}
    \sdClass[right=2cm of Vehicle]{Car}{Car}{Seats}{+ drive(): void}
    \draw[sd gen] (Car) -- (Vehicle);
\end{tikzpicture}
```

## Contributing
Contributions are welcome! Please feel free to submit pull requests or open issues for feature requests and bug reports.

## License
Distributed under the LaTeX Project Public License (LPPL) 1.3c or later.
