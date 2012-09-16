Hunspell Dictionaries
=====================

This repository provides dictionary data for the spell checker *Hunspell*. Each language is separated into its own branch, where each is directly based on the `anchor` branch, plus they are all merged together in `master`. The spell checker itself is *not* included, but available at http://hunspell.sourceforge.net.

If you would like to add another dictionary for e.g. a *new* language `zz` and country `ZZ`, then apply:

    $ git checkout anchor
    $ git checkout -b zz
    $ git add zz_ZZ.aff
    $ git add zz_ZZ.dic
    $ git commit -m "New dictionary: zz"
    $ git checkout master
    $ git merge zz

Otherwise, if the language branch `zz` already exists, then:

    $ git checkout zz
    $ git add zz_ZZ.aff
    $ git add zz_ZZ.dic
    $ git commit -m "New dictionary: zz"
    $ git checkout master
    $ git merge zz

This sequence of commands will make sure, that the history of the repository remains clean, and it enables access to each dictionary separately. Consider a *pull request* if you think your dictionary data is of high quality and might be of use for others.

All files should contain a header w.r.t. a license; otherwise GPL can be assumed. Nevertheless, if the original author did not include such a header, then please make the effort the clarify. Original authors responsible for such omissions can contact the maintainer of this repository and ask to include the corresponding licensing information.
