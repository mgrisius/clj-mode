# clj-mode v 0.9

clj-mode - a 'bare metal' (old school) emacs major mode for the clojure language.

back from an unplanned  hiatus . . .

Provide basic syntax highlighting (font-lock), syntax formatting (indentation),
and navigation for clojure (http://clojure.org).

clj-mode is derived directly from the orginal version 1.0 'branch' of clojure-mode.el at:
http://www.emacswiki.org/emacs/clojure-mode.el

clj-mode is roughly 80% the same as original version 1.0. 14 forms are the same, 4 forms have
minor uopdates, 5 are re-written or split.

Preserve reference to original version 1.0 clojure-mode.el 2007/2008 'branch' before
all references to it disappear, and it slips into obscurity. 

clj-mode strategy: avoid version and package dependencies, simplify inferior-lisp-mode set up
and use analogous to traditional ('old school') lisp and scheme modes, e.g. make it
'self contained'.

## Steps:

* rename to clj-mode.
* update to clojure 1.5.1. (needs further updates clojure 1.11.n)
* add updated imenu interface function.
* simplify/fix/add a few minor things.
* delete old Auto Complete clj-mode dict file, use 'modern' ac dictionary and rename clj-mode

## imenu

clojure-match-next-def d/n work correctly, using `clojure-1.4.0/src/clj/clojure/core.clj'
as a test use case over 20 of 571 defs or ~4% were missing from index, plus erroneous
entries were added too!

m-x imenu now works with clj-mode-next-def, or try out
(add-hook 'clj-mode-hook 'imenu-add-menubar-index), very useful on large files
like core.clj with over 500 definitions.

## Delete Auto Complete Mode dict, use 'modern' ac dict file

copy ac 'clojure-mode' to 'clj-mode' in 'dict' dir. 

## License

Source Copyright (c) 2007-2008/2013 Jeffrey Chu & Lennart Staflin, (c) 2013-2019 Matthew A. Grisius

Distributed under the GNU General Public License

## Keywords

keywords: clj-mode, clojure-mode, lisp, clojure, clj
