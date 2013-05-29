This is a Plone extension for the `plone.stringinterp`__ module.

__ https://pypi.python.org/pypi/plone.stringinterp

Adding this to your buildout and you will be able to add **full content text** in
your **contentrules** e-mail messages.

How to use
==========

When you are preparing e-mail action for your Plone Content Rules, you can use two new
marker in the text:

``${text}``
    The current document full text
``${indented_text}``
    Same as above, but right-indent the text using a tabular char before every line.

Text is transformed from HTML to plain text (as ussualy are Plone e-mail).

Getting text
------------

"Main text field" is an abstract entity.
This product try to guess text using adapters, so you can override or provide more specific
ones (see the code some example).

In general those kind of text is supported:

* ATContentTypes based content types with a *text* field
  (Event, News Item, Document)
* Comment from plone.app.discussion

Plus, a general adapter that simply try to read a "text" attribute is provided as fallback
(this will probably fix the use with Dexterity too).

Credits
=======

Developed with the support of `Regione Emilia Romagna`__;
Regione Emilia Romagna supports the `PloneGov initiative`__.

__ http://www.regione.emilia-romagna.it/
__ http://www.plonegov.it/

Authors
=======

This product was developed by RedTurtle Technology team.

.. image:: http://www.redturtle.it/redturtle_banner.png
   :alt: RedTurtle Technology Site
   :target: http://www.redturtle.it/

