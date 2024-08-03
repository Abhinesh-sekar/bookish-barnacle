# darkmode.sty

`darkmode.sty` is a LaTeX package designed to provide a dark mode appearance with colored boxes for different types of mathematical and logical content. This package includes custom environments for definitions, theorems, axioms, proofs, and examples, each with distinct color settings.

## Features

- **Dark Mode Background**: The background of the document is set to a dark color with light-colored text.
- **Colored Boxes**: Custom colored boxes for various content types, with colors applied to the borders and backgrounds.
- **Pre-defined Environments**:
  - `mytheorem`: For theorems
  - `myproof`: For proofs
  - `myaxiom`: For axioms
  - `mydefinition`: For definitions
  - `myexample`: For examples

## Installation
Save this file in the same directory of the LaTeX document you are going to create 
To use the `darkmode.sty` package in your LaTeX document, include the following line in the preamble of your document:


```latex
\usepackage{darkmode}
```
## Usage
You can use the following custom environments to format your content:
### Theorem
```latex
\begin{mytheorem}[optional settings]{Title}
Your theorem content here.
\end{mytheorem}
```
### Proof 
```latex
\begin{myproof}[optional settings]
Your proof content here.
\end{myproof}
```
### Axiom
```latex
\begin{myaxiom}[optional settings]{Title}
Your axiom content here.
\end{myaxiom}
```
### Definition
```latex
\begin{mydefinition}[optional settings]{Title}
Your definition content here.
\end{mydefinition}
```
### Example 
```latex
\begin{myexample}[optional settings]{Title}
Your example content here.
\end{myexample}
```

## Color Settings
The colors used in the `darkmode.sty` package are designed to work well with a dark background. Here are the color settings used:
- Background Color: Dark grey (#1E1E1E)
- Text Color: Light grey (#C0C0C0)
- Box Border Colors:
  - Theorem: Tomato (#FF6347)
  - Proof: Light Sea Green (#20B2AA)
  - Axiom: Steel Blue (#4682B4)
  - Definition: Gold (#FFD700)
  - Example: Blue Violet (#8A2BE2)
- Box Background Colors: Each box type has a background color with 10% opacity based on the border color.

## Example Document:
Here is a basic example of how to use the darkmode.sty package in a LaTeX document:
```latex
\documentclass{article}
\usepackage{darkmode}

\title{Math Course Notes}
\author{Your Name}
\date{\today}

\begin{document}

\maketitle

\section*{Real Analysis}
\subsection*{Limits and Continuity}
\begin{mydefinition}{Definition}
A function \( f: \R \to \R \) is said to be \textit{continuous} at a point \( c \in \R \) if for every \( \epsilon > 0 \), there exists \( \delta > 0 \) such that whenever \( |x - c| < \delta \), it follows that \( |f(x) - f(c)| < \epsilon \).
\end{mydefinition}

\subsection*{Differentiation}
\begin{mytheorem}{Theorem}
If \( f \) is differentiable at \( c \in \R \), then \( f \) is continuous at \( c \).
\end{mytheorem}
\begin{myproof}
Let \( \epsilon > 0 \) be given. Since \( f \) is differentiable at \( c \), there exists \( \delta > 0 \) such that for all \( x \) with \( 0 < |x - c| < \delta \), we have
\[
\left| \frac{f(x) - f(c)}{x - c} - f'(c) \right| < \frac{\epsilon}{|x - c|}
\]
Thus,
\[
|f(x) - f(c)| < \epsilon
\]
which shows that \( f \) is continuous at \( c \).
\end{myproof}

\subsection*{Examples}
\begin{myexample}{Example 1}
Consider the function \( f(x) = x^2 \). This function is continuous at every point \( c \in \R \). To see this, note that
\[
|f(x) - f(c)| = |x^2 - c^2| = |x - c||x + c|
\]
Since \( |x + c| \) is bounded near \( c \), \( |f(x) - f(c)| \) can be made arbitrarily small by choosing \( x \) sufficiently close to \( c \).
\end{myexample}

\end{document}
```
# Thank you :>
