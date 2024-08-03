.\" darkmode.rm - Documentation for the darkmode.sty LaTeX package
.\" 
.\" Usage: man ./darkmode.rm
.\"
.TH DARKMODE 1 "August 2024" "darkmode.sty" "LaTeX Packages"
.SH NAME
darkmode.sty \- LaTeX package for dark mode appearance with colored boxes
.SH SYNOPSIS
.B \usepackage{darkmode}
.SH DESCRIPTION
The
.B darkmode.sty
package provides a LaTeX setup for creating documents with a dark mode appearance. This package includes pre-defined styles for different types of mathematical and logical content, all styled to be visually accessible on a dark background. The package features custom environments for definitions, theorems, axioms, proofs, and examples, each with distinct color settings.

.SH FEATURES
.PP
- Dark Mode Background: The background of the document is set to a dark color with light-colored text.
- Colored Boxes: Custom colored boxes for various content types, with colors applied to the borders and backgrounds.
- Pre-defined Environments:
  .TP
  .B mytheorem
  For theorems
  .TP
  .B myproof
  For proofs
  .TP
  .B myaxiom
  For axioms
  .TP
  .B mydefinition
  For definitions
  .TP
  .B myexample
  For examples

.SH USAGE
To use the
.B darkmode.sty
package in your LaTeX document, follow these steps:

.PP
1. Include the Package: Add the following line to the preamble of your LaTeX document:
.PP
.B \usepackage{darkmode}
.PP
2. Use the Environments: You can use the following custom environments to format your content:

.TP
.B mytheorem
.TS
center;
l l.
\begin{mytheorem}[optional settings]{Title}
Your theorem content here.
\end{mytheorem}
.TE

.TP
.B myproof
.TS
center;
l.
\begin{myproof}[optional settings]
Your proof content here.
\end{myproof}
.TE

.TP
.B myaxiom
.TS
center;
l l.
\begin{myaxiom}[optional settings]{Title}
Your axiom content here.
\end{myaxiom}
.TE

.TP
.B mydefinition
.TS
center;
l l.
\begin{mydefinition}[optional settings]{Title}
Your definition content here.
\end{mydefinition}
.TE

.TP
.B myexample
.TS
center;
l l.
\begin{myexample}[optional settings]{Title}
Your example content here.
\end{myexample}
.TE

.SH COLOR SETTINGS
The colors used in the
.B darkmode.sty
package are designed to work well with a dark background. Here are the color settings used:

.TP
- Background Color: Dark grey (#1E1E1E)
- Text Color: Light grey (#C0C0C0)
- Box Border Colors:
  .TP
  Theorem: Tomato (#FF6347)
  .TP
  Proof: Light Sea Green (#20B2AA)
  .TP
  Axiom: Steel Blue (#4682B4)
  .TP
  Definition: Gold (#FFD700)
  .TP
  Example: Blue Violet (#8A2BE2)
- Box Background Colors: Each box type has a background color with 10% opacity based on the border color.

.SH EXAMPLE DOCUMENT
Here is a basic example of how to use the
.B darkmode.sty
package in a LaTeX document:

.TS
center;
l l.
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
.TE

.SH SEE ALSO
The LaTeX documentation for the `tcolorbox` package for more advanced box customization.

.SH AUTHOR
This manual page was written for the `darkmode.sty` LaTeX package.

