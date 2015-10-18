# tango-colors

Tango colors definition for use with python, latex and other ...

## LaTeX

If you want to use these tango colors in you latex document put `tango.sty` somewhere
latex will find it. For example, in the texmf directory.

## Python

You have two ways to use the colors. If you only need the HTML model you can 
import `TANGO_HTML_COLORS` which is a dictionary of tango colors.

```python
    >>> from tango_colors import TANGO_HTML_COLORS as tango
    >>> print(tango["butter1"])
    #fce94f
```

You can also make an instance of the `Tango` class. This allow you to choose
several color models :

```python
    >>> from tango_colors import Tango
    >>> Tango.available_models
    ('HTML', 'RGB', 'rgb', 'HSV', 'hsv')
    >>> tango = Tango()
    >>> tango.skyblue1
    #729fcf
    >>> tango = Tango("RGB")
    >>> tango.skyblue1
    (114, 159, 207)
```

## Grace

If you are using [(xm)grace](http://plasma-gate.weizmann.ac.il/Grace/)
the file `Default.agr` is a template which will allow you to have the tango
colors available into xmgrace.

You have to put it in your `$HOME` directory in `.grace/templates/`.

The template does not define only colors. If you only want the colors, just
copy the lines such as :

    @map color 16 to (138, 226,  52), "Chameleon 1"
    


    
