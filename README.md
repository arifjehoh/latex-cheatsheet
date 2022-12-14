# latex-cheatsheet
My LaTeX cheatsheet 

## Latex base document
```latex
\documentclass[a4paper,11pt]{article}
\usepackage[utf8]{inputenc}
\begin{document}

\title{
    \textbf{Title name}
}
\author{Arif Jehda-Oh}
\date{\today}

\maketitle

\end{document}
```
## Code snippets
```latex
\usepackage{minted}
\begin{minted}{<language>}
<code>
\end{minted}
```
## Images
```latex
\usepackage{graphicx}
\graphicspath{ {./images/} }

\includegraphics[width=\textwidth]{<name>.png}
```
## Table
```latex
\begin{table}[H]
\centering
\begin{tabular}{l|c|r}
Column 1 & Column 2 & Colum 3 \\ \hline
a & b & c \\
1 & 2 & 3 
\end{tabular}
\caption{Some caption}
\end{table}
```

## Mathematical expression
```latex
\[ <expression> \]
```

## Plotting Graph
```latex
\usepackage{pgfplots}
\pgfplotsset{width=\textwidth, compat=1.8}

\begin{tikzpicture}
  \begin{axis}[
    title={<title of graph>},
    xmin={0}, xmax={MAX_WIDTH}, xlabel={AXIS_X},
    ymin={0}, ymax={MAX_HEIGHT}, ylabel={AXIS_Y},
    grid={both},
    major grid style={lightgray},
    minor grid style={lightgray},
    height={\textwidth * 0.75},
    legend cell align={left},
    legend pos={north west},
  ],
  \addplot[
    color={blue},
    mark={square}
  ]
  coordinates {
    (0.4, 10)
    (3.2, 100)
    (15, 1000)
  };
  \legend{
    {dataset 1}
  }
  \end{axis}
\end{tikzpicture}

```

## Bullet points
```latex
% Create unordered list in LaTeX
\begin{itemize}
  \item The first item of the list.
  \item The second item of the list.
  \item An item with an \textsc{equation}:
    \[ \sum_{n=1}^{\infty} \frac{1}{n^2}=\frac{\pi^2}{6}\]
\end{itemize}
```
