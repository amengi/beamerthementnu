# beamerthementnu
A LaTeX beamer theme for NTNU presentation templates.

Mattia Veroni (IMF, IE) has taken over as maintainer for the project. 
Future directions, including where it's hosted, rests with him. Stay tuned!


## Overview

This beamer theme implements the [NTNU PowerPoint templates](https://innsida.ntnu.no/wiki/-/wiki/Norsk/Lage+presentasjon) 
for LaTeX beamer. See usage example below.

The single theme can produce all the different templates, both in 4:3
and 16:9 format. Starting from the 2017 edition, the theme also includes
campus dependent versions of of all the variants.

If you have technical questions, please contact [Martin Strand](https://www.ntnu.edu/employees/martin.strand). 
Do not send such questions to the NTNU Communications Division.


## Usage

The basic usage is the command

```latex
\usetheme[style=ntnu|simple|vertical|horizontal, language=bm|nn|en, smalltitle, city=all|trondheim|alesund|gjovik]{ntnu2017}
```

All options are optional. The defaults are `ntnu`, `bm` and no cities.

A minimal working example

```latex
\documentclass[screen, aspectratio=43]{beamer}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}

% Use the NTNU-temaet for beamer 
% \usetheme[style=ntnu|simple|vertical|horizontal, 
%     language=bm|nn|en, 
%     smalltitle, 
%     city=all|trondheim|alesund|gjovik]{ntnu2017}
\usetheme[style=ntnu,language=en]{ntnu2017}

\usepackage[english]{babel}

\title[Short title]{The full and long title of the presentation}
\subtitle{Subtitle if you want}
\author[O. Nordmann]{Ola Nordmann}
\institute[NTNU]{Department of \LaTeX-ical sciences, NTNU}
\date{1 January 1970}
%\date{} % To have an empty date

\begin{document}

\begin{frame}
  \titlepage
\end{frame}

% Alternatively, special title page command to get a different background
% \ntnutitlepage

\begin{frame}
  \frametitle{Main theorem}
  \begin{theorem}
    {\LaTeX} makes things easier.
  \end{theorem}
  \begin{proof}
    For details, see Flynn.
  \end{proof}
\end{frame}

\end{document}
```


## Installation

Simply copy the folder `beamerthementnu2017` into your `texmf/tex/latex` folder. 
The precise location varies on different operating systems. 

TeX Live specific: A user have suggested that one can run `texhash` after 
installing the files if LaTeX is unable to find the new theme.


## Known issues

 - The theme doesn't work with `eps` only presentations. This can be changed if there is a demand for it.

## Changes from the 2015 edition

 - The code is completely rewritten, based on a skeleton by [Claudio Fiandrino](https://tex.stackexchange.com/questions/146529/design-a-custom-beamer-theme-from-scratch)
 - All templates are localized
 - Full support for biblatex
 - There is now an option to show which city you belong to, in those rare cases that is important
 - The overall size is reduced, due to fewer and smaller pictures
 - Generating the title page is fully flexible, and it can be used everywhere in the presentation
 - Margins and sizes are adjusted to bring it closer to the PowerPoint templates
 - The title font is greatly increased in size; if your presentation has a long title, use the `smalltitle` option
 - Frames can now have subtitles
 
As a principle, the code is as lightweight as practically possible, and
only using packages when really necessary. For example, while some of
the graphics could have been generated by TikZ, an image is included
instead.


## Contributions and license

The code was originally based on [Håvard Berland's work in 2005](http://www.pvv.ntnu.no/~berland/ntnubeamer/). In private conversation
in December 2015, Berland licensed his code under a [Creative Commons 
Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/), and so naturally goes 
for all code in this repository.

However, the design is owned by NTNU, and should not be altered 
substantially without checking it with the [Communication Division](https://www.ntnu.no/adm/komm).

Any contribution to improve the code is very welcome.

This theme also includes code from the following sources and contributors:
 - [Detect aspect ratio](http://tex.stackexchange.com/questions/123106/detect-aspect-ratio-in-beamer), by StackExchange user egreg
 - anates
 - dvolgyes
