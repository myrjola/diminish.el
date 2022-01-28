[![GNU ELPA](https://elpa.gnu.org/packages/diminish.svg)](https://elpa.gnu.org/packages/diminish.html)
[![GNU-devel ELPA](https://elpa.gnu.org/devel/diminish.svg)](https://elpa.gnu.org/devel/diminish.html)
[![MELPA](https://melpa.org/packages/diminish-badge.svg)](https://melpa.org/#/diminish)
[![MELPA Stable](http://stable.melpa.org/packages/diminish-badge.svg)](http://stable.melpa.org/#/diminish)

# diminish.el

Introduction
============

> When we diminish a mode, we are saying we want it to continue doing its
> work for us, but we no longer want to be reminded of it.  It becomes a
> night worker, like a janitor; it becomes an invisible man; it remains a
> component, perhaps an important one, sometimes an indispensable one, of
> the mechanism that maintains the day-people's world, but its place in
> their thoughts is diminished, usually to nothing.  As we grow old we
> diminish more and more such thoughts, such people, usually to nothing.
>  -- Will Mengarini

This package implements hiding or abbreviation of the mode line displays
(lighters) of minor-modes.

Quick start
===========

```emacs-lisp
(require 'diminish)

(diminish 'rainbow-mode)                                       ; Hide lighter from mode-line
(diminish 'rainbow-mode " Rbow")                               ; Replace rainbow-mode lighter with " Rbow"
(diminish 'rainbow-mode 'rainbow-mode-lighter)                 ; Use raingow-mode-lighter variable value
(diminish 'rainbow-mode '(" " "R-" "bow"))                     ; Replace rainbow-mode lighter with " R-bow"
(diminish 'rainbow-mode '((" " "R") "/" "bow"))                ; Replace rainbow-mode lighter with " R/bow"
(diminish 'rainbow-mode '(:eval (format " Rbow/%s" (+ 2 3))))  ; Replace rainbow-mode lighter with " Rbow/5"
(diminish 'rainbow-mode                                        ; Replace rainbow-mode lighter with greened " Rbow"
  '(:propertize " Rbow" face '(:foreground "green")))
(diminish 'rainbow-mode                                        ; If rainbow-mode-mode-linep is non-nil " Rbow/t"
  '(rainbow-mode-mode-linep " Rbow/t" " Rbow/nil"))
(diminish 'rainbow-mode '(3 " Rbow" "/" "s"))                  ; Replace rainbow-mode lighter with " Rb"
```

Ref: [Emacs manual - The Data Structure of the Mode Line](https://www.gnu.org/software/emacs/manual/html_node/elisp/Mode-Line-Data.html).

John Wiegley's
[use-package](https://github.com/jwiegley/use-package#diminishing-and-delighting-minor-modes)
macro also has support for diminish.el.

Copyright Assignment
====================

Diminish is subject to the same [copyright assignment](https://www.fsf.org/licensing/contributor-faq) policy as GNU Emacs.

Any [legally significant](https://www.gnu.org/prep/maintain/html_node/Legally-Significant.html#Legally-Significant) contributions can only be merged after the author has completed their paperwork. Please ask for the request form, and we'll send it to you.

Acknowledgments
===============

diminish.el was created by Will Mengarini on 19th of February 1998 and is now
maintained by [Martin Yrjölä](https://github.com/myrjola).
