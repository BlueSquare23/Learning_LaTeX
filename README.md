# Learning LaTeX

These are some note's I've taken while learning LaTex. I'm using [Luke Smiths
videos](https://youtu.be/NwnYHoNtfJ0) on the subject as my guide.

## A Tangent

Fun side fact about Luke Smith, I totally hacked his personal Email server one
time over telenet. I used some SMTP commands to send him messages from himself.
No spoofing either, legitimately to his address, from his address, using his
Email server. 

He just accidentally allowed unauthenticated sending to himself. Don't worry, I
sent him a message from my own Email later on and told him how I did it. He has
since fixed his [Postfix
configuration](https://github.com/LukeSmithxyz/emailwiz).

> Re: Your Mail Server Allows Unauthenticated Sending
> From: Luke Smith <luke@lukesmith.xyz>
> 
> Hey, thanks for bringing this to my attention.
> 
> I fooled around with some Postfix settings and it should reject all
> unauthenticated mail.
> 
> I tried sending via telnet now and was rejected at `rcpt`.

## Formatting Basics 

### Header & Title

There are several basic elements of a latex document. First is the
`\documentclass{}` function which specifies what type of tex document it is. In
the case below we'll use the article class.

After that comes the title block. This is composed of `\author{}` and
`\title{}` statements. Its closed off by a `\maketitle` function.

The content of a latex document lives within the `\begin{document}` and
`\end{document}` tags.

`latex.tex`

```
\documentclass{article}

\author{John Radford}
\title{My first {\LaTeX} Document}

\begin{document}

\maketitle

This is some text.

\end{document}
```

### LaTeX

The cool way of writing Latex in LaTeX is \`{\LaTeX}\`. Its the closest thing the
text formatting system community has to a "gang-sign." 

I wonder what Groff's gangsign would look like? 

HTML's is definitely `<HTML>`.

Markdown's gangsign would probably just be, `Markdown`.

### Sections

In Latex sections are defined by the `\section{}` tag.

`latex.tex`

```
\documentclass{article}

\author{John Radford}
\title{My first {\LaTeX} Document}

\begin{document}

\maketitle

\section{Introdution}

This is some text.

\section{Formatting}

\section{Numbering}

\subsection{Subsection}

\end{document}
```

You can see sections are numbered automatically. 


### Markup Basics

Latex has all the good old markup basics we know and love from html and
markdown, plus more.

We can use the make text italicised, bold, underlined, and emphatic. The
difference between emphatic and italics is that italics is for proper titles
and things like that whereas emphatic is just anything that need emphasis.

`latex.tex`

```
\section{Formatting}

\textbf{This is bold text.}

\textit{This is italic.}

\emph{This is emphatic!}

\underline{This text is under lined.}

This text is sad and normal and will be alone forever :(

"unambiguous quotes"

``real quotes''

`real single quotes'

```


