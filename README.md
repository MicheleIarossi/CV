# One page CV in LaTeX

This is a LaTeX template for generating a one page CV.

One of the main benefits of LaTeX is its capability of producing extremely neat and tidy typeset documents.

The template `cv.tex` that you can download here is based on the one page resume provided by Gayle Laakmann McDowell on her website https://www.careercup.com/resume. I have kept the same layout but reimplemented commands and enviroments on my own with much simpler
LaTeX definitions and without recurring to `\vspace` commands all the time. The final result is more or less the same.

Hope you like the template and find it easy to use!

## Prerequisites

Since the CV template is provided as a LaTeX file, you need to:

- Install the latest MacTex distribution from https://www.tug.org/mactex/
- Install the Calibri font on your Mac
- Use XeLaTeX in TeXShop for typesetting the CV

Concerning the Calibri font, if you have MS Office installed on your Mac, you can copy the required font files (`cp Calibri*.ttf`) from this folder:
`/Applications/Microsoft Word.app/Contents/Resources/DFonts` to this one in your home directory `~/Library/Fonts`, from where the font will be automatically added to your font library and made available for MacTeX to use.

## Usage

The template defines the following new commands and environments:
- `\cvheaderline`
- `\cvtitle`
- `\cvsection`
- `\cvlist`

# CV header line

The command:

`\cvheaderline{<left aligned text>}{<center aligned text>}{<right aligned text>}`

 aligns your text keywords to the left/center/right in the same line. I use it in the Employment and Education sections.

# CV title

The command:

`\cvtitle{\small <left aligned text in small font>}{<center aligned text in large and bold font>}{<right aligned text in small font>}`

is the same as `\cvheaderline` but the left and right aligned text are typeset in a `\small` font, whereas the center text is typeset in `\Large` and bold. I use it for generating the CV title at the top with my name at the center.

# CV section

The command:

`\cvsection{<section name>}`

introduces a section of your CV, such as Employment or Skills, by typesetting the section name left aligned and in bold font with a horizontal line underneath.

# CV list

The environment:

`\begin{cvlist}[optional <label>]`

`\item <your description>`

`\end{cvlist}`

produces a compact list of items which are typeset without any of the extra spacing characterising the conventional list. The default label is $\cdot$ but you can change it with the optional label parameter if you want. I use this environment for providing any type of text such as job descriptions or skills.

# Separating your sections

You might be tempted of using `\vspace` for separating your sections vertically but there is actually no need to use it. 

You can use LaTeX `\smallskip`, `\medskip` or `\bigskip` to introduce proper vertical spacing as needed.


