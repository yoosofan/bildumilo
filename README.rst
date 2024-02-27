Bildumilo
=========
Bildumilo is a tool to make impress.js_ presentations from
reStructuredText. For a quick explanation, see the demo_.

Based on `Hovercraft! <https://github.com/regebro/hovercraft>`_

Features
--------
* Write your presentations in a text markup language. No slow, limiting GUI, no annoying HTML!
* Pan, rotate and zoom in 3D, with automatic repositioning of slides!
* A presenter console with notes and slide previews!
* Support for showing mathematical formulas.
* Styling is easy with CSS.
* The slide show generated is in HTML, so you only need a web browser to show it.
* Easy sharing, as it can be put up on a website for anyone to see!

Full documentation of Hovercraft is available at readthedocs.org_, and also in the
documentation subdirectory.

Installation
------------
Bildumilo requires Python 3 and can be installed like any Python package.

It is better to use virtual environment::

    $ cd /destination/directory/
    $ python -m venv myvenv
    $ source myvenv/bin/activate

Download the code in a directory let's name it `src_dir/path/`
The easiest way is to install pip_, and then run::

    $ pip install ~/path/bildumilo/
    
    or
    
    $ python3 -m pip install ~/path/bildumilo/

Use bildumilo

Then you can deactivate virtual environment::

    $ deactivate

Juan Bondi has made videos of how to install Hovercraft:

* Installation on Ubuntu and Debian based computers: https://www.youtube.com/watch?v=tHSJLF9OnKQ
* Installation on Windows: https://www.youtube.com/watch?v=I63I8Az24d8

Chromium-chromedriver is needed to generate PDF from RST presentations files (You can only Install Chrome Browser)

Hovercraft is untested on Windows, but there is no reason it shouldn't work, at least in theory.

TODO
----
* Remove extra files:
    * Prevent making extra grap_ii.png for changing yographviz
        * G.draw("test.svg", prog= 'dot', format='svg:cairo') 
        * https://stackoverflow.com/a/72152677/886607
        * https://github.com/liuyug/python-docutils-graphviz/tree/master
        * https://github.com/liuyug/python-docutils-graphviz/blob/master/docutils_graphviz.py
        * https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Adding_vector_graphics_to_the_Web
        * https://docutils-ext.readthedocs.io/en/latest/svgt.html
* Add an option to run a new instance of web browser
* Replace `pyhtml2pdf` by `selenium` because of the following vulnerability:
    * https://security.snyk.io/vuln/SNYK-PYTHON-PYHTML2PDF-6254644
    * https://vuldb.com/?id.254137
    * https://vulners.com/github/GHSA-P3RV-QJ56-2FQX
    * https://www.cvedetails.com/cve/CVE-2024-1647/
    * https://cert.ir/node/6248
    * https://nvd.nist.gov/vuln/detail/CVE-2024-1647
    
    * https://github.com/xhtml2pdf/xhtml2pdf
    * https://github.com/CourtBouillon/weasyprint-samples/tree/master
    * https://github.com/Kozea/WeasyPrint/tree/main
    
    
    * https://github.com/plotly/plotly.py
    * https://plotly.com/python/static-image-export/
    * https://plotly.com/python/bar-charts/
    
    * return [nodes.raw('', parsed, format='html')]   # https://snyk.io/advisor/python/docutils/functions/docutils.parsers.rst.directives.register_directive
    * https://github.com/renatopp/pyramid-blog/blob/7dba5a948af8a61e00fea303367be12e5de6f788/blog/blog/libs/rest/reSTpygments.py#L73
    * https://github.com/renatopp/pyramid-blog/tree/master/blog/blog/libs/rest
    * https://github.com/renatopp/pyramid-blog/blob/master/blog/blog/libs/rest/reSTpygments.py
    * https://github.com/renatopp/pyramid-blog/blob/4cc950d6a82eeaa912c9e1111fe25a8cb836d660/blog/blog/libs/rest/reSTpygments.py#L73

    * https://pygraphviz.github.io/documentation/stable/install.html
    
.. _impress.js: http://github.com/bartaz/impress.js
.. _demo: https://regebro.github.io/hovercraft
.. _readthedocs.org: https://hovercraft.readthedocs.io/
.. _pip: http://www.pip-installer.org/en/latest/
