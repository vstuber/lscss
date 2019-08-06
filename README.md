# Leading Systems LSCSS

## Getting started
After installing LSCSS, the less framework is located in assets/lscss. The files in this directory may not be modified.

Instead, you create your own custom less file, include the LSCSS framework and do all your work here.

The custom less file should be created in **files/styles** or **files/lscss** (whatever you like best) and, in order to make
the purpose of the file obvious, it should be named **lscss-project.less**

In Contao, load the stylesheet by selecting it as an external stylesheet in the layout record. Make sure to select the
compiled CSS file and not the LESS file. Contao could compile the LESS file but the way Contao handles paths (e.g. font
paths) can cause trouble.

The lscss-project.less file should only contain a few imports:


```
@import "../../assets/lscss/lscss.less";

@import "_variables.less";

@import "_fonts.less";

@import "_custom.less";
```

The first import loads the lscss framework itself. The other imports are project specific files which technically are
not mandatory but of course it makes sense to use them. Therefore, create the files "_variables.less", "_fonts.less"
and "_custom.less" inside the same directory where lscss-project.less is located as well.

`_variables.less` is the file in which you override variables defined in the LSCSS framework if necessary. Of course,
you can also define new variables.

`_fonts.less` contains the @font-face rules for loading fonts

`_custom.less` contains all the project specific styles, probably divided in multiple imports.