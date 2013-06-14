Prototype of the documentation for OpenPTV project
==================================================


This separate repository can be become http://github.com/openptv/docs. Such repository including the `gh-pages` branch would automatically allow us to create 

http://www.openptv.net/docs

using Sphinx http://sphinx-doc.org/index.html


How it works
------------

For the prototype, check http://alexlib.github.io/docs


The source files are simple ASCII files that one can edit offline or online using Github editor. The source files are in the software repository, i.e. http://github.com/alexlib/openptv-python for example. 

Therefore, in order to add a new page or a new documentation fix, one could fork the directory, add a page of fixs something and send pull request or a patch by mail. 

* What else do we get from Sphinx - automatic rendering our comments and docstrings from Python.
* How do we link C code references: we generate those using Doxygen and then link manually by copying into the docs/ folder


How to use it effectively
-------------------------


1. install Sphinx
2. clone two repositories: 
  * `openptv-python` from http://github.com/alexlib/openptv-python
  * `docs` from http://github.com/alexlib/docs
2. in the `openptv-python` folder, edit the reST files in `openptv-python/docs/source/` subfolder  
    
        $$ edit source/index.rst

3. in `openptv-python/docs` subfolder run   
  
        $$ make html

4. copy everything into the separate repository copy of the `docs` (check that it's under git branch `gh-pages`) 

        $$ cd /Users/alex/docs
        $$ git checkout gh-pages 
        $$ cp -rf /Users/alex/openptv-python/docs/build/html/* .
        $$ git add .
        $$ git commit -m "new html"
        $$ git push origin gh-pages



