# Introduction
This repository is for documenting about Metatron Discovery Install.

# How to build and update the contents
* Requirements
  * Python 3 + [pip](https://pypi.org/project/pip/)
  
* Clone this repository
  ```sh
     git clone https://github.com/AnnieHwang/metatron-doc-install.git
  ```
* Install packages
  ```sh
    pip install -r requirements.txt
  ```
* Edit the contents
   * Every document is written in **rst file**. Follow the reStructedText syntax.
   * Location for all the image files is `/_static/img/part00`
  
* Build documents using [Sphinx](http://sphinx-doc.org/)
  ```sh
    make html
  ```
* HTML files are located in `_build/html/`.
* Copy built files to `docs/` for publishing [GitHub Pages](https://pages.github.com/)
  ```sh
    cp -r _build/html/* docs/
  ```
* Refactory
  ```sh
    rm -f docs/static
    rm -f docs/image
    refactor > rename (by intelliJ) : _static => static, _image => image
    cp -r docs/static/* docs/_static
  ```
* Update
  ```sh
    git add .
    git commit -m "commit message"
    git pull
    git push
  ```

# References
* [Sphinx Documents](http://www.sphinx-doc.org/en/master/contents.html)
* [reStructuredText Quick Reference](http://docutils.sourceforge.net/docs/user/rst/quickref.html)
