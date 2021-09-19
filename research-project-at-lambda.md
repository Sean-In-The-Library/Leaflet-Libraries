# Notes on research projects at Lambda-Lab

## Setup

- Create an Overleaf project, use *X-Y* as project title (replace `X` by `msc-thesis` or `bep` or your overarching research topic; replace `Y` by the specific topic of the paper/report) and invite me to it.
  - Every section/chapter gets at least two rounds of comments.
- Use GitHub to keep track of your project and add me to your project.
  - Add a `README.md` where you keep track of the meetings we had and what we discussed (action points to take).
  - Add a folder `papers` where you keep track of all the papers you read for your project.
  - Add a folder `code` to keep track of all your code. 
  - When you run any experiments, keep track of which code version you ran (use hash commits or tag the repo).
- For MSc thesis students only: make sure to submit the two required forms on time (one to form the thesis committee and one to fix the defense date).
- If several people work together on the project and aim for 1+ publications, settle on the order of authors at the start of the project. Note: it is possible to have several first authors on a paper with footnote such as *Equal contribution*.


## Material to read in preparation of your project
- [Differences between undergraduate work and graduate research](https://twitter.com/cesifoti/status/1437043299852996608)
- [How to get unstuck in your research](https://twitter.com/jbhuang0604/status/1419880122006519809)
- [How to avoid machine learning pitfalls: a guide for academic researchers](https://arxiv.org/abs/2108.02497)
- [IR anthology](https://ir.webis.de/anthology/): an overview of recent IR conference proceedings.
- [How to approach an applied ML project](https://elvissaravia.substack.com/p/getting-started-with-applied-ml-research)
- [Book on Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/)
- [Book on Search User Interfaces](http://searchuserinterfaces.com): very good starting point for those wanting to dive deeper into search engine interfaces
- [Methods for Evaluating Interactive Information Retrieval Systems with Users](https://ils.unc.edu/courses/2017_fall/inls509_002/papers/FnTIR-Press-Kelly.pdf): a must-read book for those interested in designing interactive IR studies
- [An opinionated guide to ML research](http://joschu.net/blog/opinionated-guide-ml-research.html)
- [How to write code for NLP research](https://github.com/allenai/writing-code-for-nlp-research-emnlp2018)
- [How to come up with research questions](http://pgbovine.net/research-design-patterns.htm)!
- [Which papers can I read to catch up on the latest trends in NLP?](https://medium.com/huggingface/the-best-and-most-current-of-modern-natural-language-processing-5055f409a1d1)
- [Troubleshooting neural nets](http://josh-tobin.com/troubleshooting-deep-neural-networks.html): a handy guide if you find yourself in neural IR land and need to debug your models!
- [NLP recipes in Jupyter notebook form](https://github.com/microsoft/nlp-recipes)
- [Developing a research taste](http://colah.github.io/notes/taste/)

## A few useful DL resources
- Attention/transformer blog posts: [1](https://lilianweng.github.io/lil-log/2018/06/24/attention-attention.html) and [2](https://lilianweng.github.io/lil-log/2020/04/07/the-transformer-family.html)
- [Dive into Deep Learning](https://d2l.ai/index.html)
- [fastai courses](https://www.fast.ai/)
- [Embeddings in NLP](http://josecamachocollados.com/book_embNLP_draft.pdf)
- [Made with ML](https://madewithml.com/)
- [Papers with Code](https://paperswithcode.com/)
- [Overview of lots of useful ML toolkits](https://github.com/EthicalML/awesome-production-machine-learning)

## Checklists
- For machine learning oriented projects: [ML code completeness checklist](https://medium.com/paperswithcode/ml-code-completeness-checklist-e9127b168501)
- For interactive IR projects: [Elements of IIR studies](http://toinebogers.com/biirrr2019/proceedings/biirrr2019-petras-1.pdf)
- [Behavioral Testing of NLP Models with CheckList](https://homes.cs.washington.edu/~marcotcr/acl20_checklist.pdf)
- [Paper writing checklist](https://t.co/BVgVagDQCt)

## Presenting your work
- To a Twitter audience via [Twitter posters](https://twitter.com/mikemorrison/status/1242445150619607040)
- Once you are ready to make slides or a poster, I suggest to use Google Slides as this makes collaboration/commenting easy. You do not have to invent a template from scratch, [Slides Carneval](https://www.slidescarnival.com) has plenty of free templates to choose from (consider the *formal* and *simple* categories). If you want to go down your own route, head to [Adobe Color](https://color.adobe.com/explore) to find a color scheme you like. [Paul Tol's notes](https://personal.sron.nl/~pault/) on color schemes suitable for different types of plots with color blindness issues in mind are also useful.

## Organizing your thoughts/ideas
- [Obsidian](https://obsidian.md)
  - In combination with Obsidian, [espanso](https://espanso.org/) will be useful (e.g. to write `/today` instead of writing out today's date).
  - Watch [this YouTube video](https://www.youtube.com/watch?v=X61wRmfZU8Y) to learn about useful plugins for Obsidian.
  - Learn how to create a [Zettelkasten](https://forum.obsidian.md/t/simple-zettelkasten-guide/3054) in Obsidian.
- [Roam Research](https://roamresearch.com/) (costs money, in contrast to Obsidian)
  - Learn how to create a [Zettelkasten in Roam](https://www.roambrain.com/implementing-zettelkasten-in-roam).
- [Gitbook](https://www.gitbook.com/)
- [Miro](https://miro.com), an online whiteboard for visual collaboration.
- Productivity during the pandemic: https://www.youtube.com/watch?v=snAhsXyO3Ck.
- [Foam, similar to Obsidian and Roam inside of Visual Studio Code](https://foambubble.github.io/foam/).

## Useful LaTeX snippets

### Introductory LaTeX guide

The [Overleaf documentation](https://www.overleaf.com/learn) is quite handy to get started with LaTeX. 

### Which report template?

In information retrieval most conferences use the 2-column ACM format. Luckily, [Overleaf](https://www.overleaf.com/latex/templates/association-for-computing-machinery-acm-sig-proceedings-template/bmvfhcdnxfty) has this available as already. [Overleaf](https://www.overleaf.com) is a collaborative cloud-based LaTeX editor for which all TU Delft students and staff [have a professional account](https://www.overleaf.com/edu/tudelft).

### Paper structure

Every area of computer science has their own ideas of how to structure scientific contributions. 

In Information Retrieval a common structure for an interactive IR paper is the following:

```latex
\section{Introduction}

\section{Related Work}
\subsection{First Related Area}
\subsection{Second Related Area}
\subsection{Third Related Area}

\section{SearchX} %or any other big software contribution needed for this study
\subsection{Search Interface}
\subsection{Special Component Implemented for this Study}
\subsection{Data Collection and Retrieval}

\section{Experimental Design}
\subsection{Experimental Conditions}
\subsection{Search Tasks}
\subsection{Experimental Procedure}
\subsection{Questionnnaires}
\subsection{Study Participants}
\subsection{Evaluation Metrics}

\section{Results}
\subsection{RQ1}
\subsection{RQ2}
\subsection{RQ3}

\section{Conclusions}
```

A system-oriented IR paper often looks as follows:

```latex
\section{Introduction}

\section{Related Work}
\subsection{First Related Area}
\subsection{Second Related Area}
\subsection{Third Related Area}

\section{Algorithm to be Investigated} 
\subsection{Base algorithm}
\subsection{Improvement 1}
\subsection{Improvement 2}

\section{Experimental Setup}
\subsection{Datasets}
\subsection{Baselines}
\subsection{Model Variations}
\subsection{Evaluation Metrics}

\section{Results}
\subsection{RQ1}
\subsection{RQ2}
\subsection{RQ3}

\section{Conclusions}
```

### LaTeX packages

Right after `\documentclass` add the following list of packages to use (some of these are already present in templates, others need to be added by hand):

```latex
\usepackage[normalem]{ulem}
\usepackage{array,booktabs,ragged2e} % For formal tables
\usepackage{enumitem} % Better enumeration
\usepackage{xcolor} % better colors
\usepackage{tabularx}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{hyperref}
\hypersetup{
    colorlinks=true
}
\usepackage{multirow}
\usepackage{graphicx}
\usepackage{tikz}
\usepackage{fontawesome}
\usepackage{tikzsymbols}
\usepackage{adjustbox}
\usepackage{subcaption}
\usepackage[skip=1pt]{caption}
```

### LaTeX commands
Defining LaTeX commands is useful for a few things. We use it mostly to signal todos and to avoid the typing out of commonly used phrases, names and concepts. Here are a few LaTeX commands commonly found in our papers (they are all added right before `\begin{document}`) and how they are used in the text:

```latex
%% allows us to write ... bla bla \todo{This still needs to be done.}
\newcommand{\todo}[1]{ {\color{magenta} $\blacktriangleright$ #1 $\blacktriangleleft$ } }

%% experimental conditions can then be referenced as ... We first discuss \control{} and then \upperRight{}.
\newcommand{\control}{\texttt{CONTROL}}
\newcommand{\upperRight}{\texttt{UPPER-RIGHT}}

%% mathematical notation that is repetitive ... Set \cqb{} contains elements ...
\newcommand{\cqb}{$C^{\mathcal{QB}}$}

%% when discussing elements of a screenshot, we can annotate the screenshot with "enumerated balls". 
%% To also use these "enumerated balls" throughout the text ... Component \circled{2} shows of the chat window ... 
\newcommand*\circled[1]{\tikz[baseline=(char.base)]{\node[shape=circle,fill=black,inner sep=1pt] (char) {\textcolor{white}{#1}};} }
```

### Emphasizing text

Important concepts should be emphasized when they are first introduced, either via `\textit{..}`, `\emph{..}` (*italics*), `\textbf{..}` (**bold**), or `\underline{..}` (underlined text).

### Citing

Avoid the manual typing out of author names at all costs. Depending on the template, the writer can enforce the use of a certain citation style, e.g. either numerical mode (often via `~\cite{REF}`) or author names mode (via `~\citet{REF}`). 

The [natbib](https://www.overleaf.com/learn/latex/Natbib_citation_styles) package is usually recommended. It contains many different citation options. For us though and the templates we encounter at IR/NLP conferences, the mentioned `\cite` and `\citet` get us all the way. The `~` ensures that there is a whitespace before the reference. 

In most templates, several references can be included in a single command: `~\cite{REF1,REF2,REF3}`.

### Splitting up files
When collaborating on a LaTeX document it helps to not keep the entire report in one file but instead to split it up into `1_introduction.tex`, `2_related.tex` and so on. We generally use one file per section. Large tables should be saved in their own separate files. To include these separate files (here we assume we have 7 files) into the main LaTeX file, use (we here assume the files are stored in a folder named `sections`):

```latex
\input{sections/1_introduction}
\input{sections/2_related}
\input{sections/3_approach}
\input{sections/4_hypotheses}
\input{sections/5_experiment}
\input{sections/6_discussion}
\input{sections/7_conclusions}
```

### Tables and figures spread across both columns

If you are working with a 2-column template layout, you sometimes may need to use figures and tables that cover both columns. This is easy to achieve by using the `*` characer:

```latex
%figure is intended to be as large as a single column
\begin{figure}
\includegraphics[width=\linewidth]{figures/architecture.pdf}
\centering
\caption{My caption.}
\label{fig:architecture}
\end{figure}

%figure covers both columns
\begin{figure*}[t!]
\includegraphics[width=\textwidth]{figures/architecture.pdf}
\centering
\caption{My caption.}
\label{fig:architecture}
\end{figure*}

%single column table
\begin{table}
...
\end{table}

%2-column table
\begin{table*}
...
\end{table*}
```

### Explaining mathematical concepts

Take a look [here](https://betterexplained.com/articles/colorized-math-equations/) for an idea of how to use colors to make explanations of formulas more clear.

### Spreadsheet table to LaTeX table

If you have a spreadsheet (e.g. to keep track of results), porting it to LaTeX is easy and requires very little work from your side; various online converters exist, e.g. https://www.tablesgenerator.com/.

### Content in boxes


<img align="right" width="350px" src="https://github.com/chauff/chauff.github.io/blob/master/img/latex-rendering.png" />


Sometimes it makes sense to visually distinguish a piece of text from the rest by drawing a box around it and giving this box a background color. For instance, when putting the search task description into a paper:

```latex
\begin{mdframed}[backgroundcolor=black!7]
Imagine that you are taking an introductory \underline{Physics} course this term. 
For your term paper, you have decided to write about \underline{Radioactivity}. 
You also would like to write about how \underline{Radioactivity} happens and what 
\underline{types of Radioactivity} exist.
\end{mdframed}
```

### Text with a background color

Instead of putting an entire paragraph in a box, we can also just give one or more terms a different background/font color:
```latex
In the \colorbox{magenta}{\textcolor{white}{\textbf{Review}}} condition ...
```

### Icons

The [fontawesome5](https://www.ctan.org/pkg/fontawesome5) package makes it easy to also include icons in a piece of text:

```latex
We report aggregate search and review behaviours over a group \faUsers{} and individually \faUser{}.
```

### Table styling
Use the `booktabs` package to create good looking tables:

```latex
\begin{table}[!t]
    \centering
    \caption{Lots of text to explain what we see in the table.}
    \label{tab:chess} %a label allows us to refer back to the table ... As seen in Table~\ref{tab:chess}.
    \begin{tabular}{lrrr}
        \toprule
        \textbf{Search Engine} & \textbf{Placement} & \textbf{\#Columns} & \textbf{\#Entries} \\
        \midrule
        \texttt{bing.com} & Bottom left & 1 & 8\\
        \texttt{google.com} & Bottom left & 2 & 8\\
        \bottomrule
    \end{tabular}
\end{table}
```

### Large tables

Large tables (many rows and many columns) can be tricky to work with when it comes to the discussion section. To help yourself, provide an ID (Roman numbers) as first cell of each table row. In the text, you can then use `In Table~\ref{tab:results}, row X ... `.

### Table, figure and section referencing

Instead of manually typing out references to tables (which is error-prone and leads to extra work when a new table/figure is added in the middle of the report), figures or sections (e.g. `As seen in Table 3 ... `), it is better to label each of these items with a unique string as seen in the LaTeX table snippet above where `\label{tab:chess}` is used. Here, `tab:chess` is the unique string that we can use to refer to this table later via the `\ref{}` command: `As seen in Table~\ref{tab:chess}`. The same principle holds for sections:

```latex
\section{Methodology}\label{sec:methodology}
blah
As seen in Section~\ref{sec:methodology} ...
```

and figures:

```latex
\begin{figure}[t!]
\includegraphics[width=\linewidth]{images/image1.png}
\centering
\caption{Overview of something.}
\label{fig:plot1}
\end{figure}
blah
As seen in Figure~\ref{fig:plot1} ...
```

### Enumerating questions, hypothes, features
Research questions should be visually different from the rest of the text and enumerated (often in the introduction or methodology section). In addition, once research questions are enumerated, we can refer back to them as `RQ1`, `RQ2` and so on throughout the text: 

```latex
\begin{description}
    \item[\textbf{RQ1}]{\textit{This is the first research question.}}
    \item[\textbf{RQ2}]{\textit{This is the second research question.}}
    \item[\textbf{RQ3}]{\textit{This is the third research question.}}
\end{description}
```
The enumeration of research questions above can also be used to enumerate and label hypotheses and to enumerate and label features when in a setup where a lot of feature engineering is taking place. 



