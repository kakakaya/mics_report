MICS Report Template
====================

# System requirements
* Ruby >= 1.9.3
* rake
* jlisting.sty

# Edit Title page
```
$ emacs config/title.yml
```

# Init workspace
```
$ rake init
```

# Create new page
```
$ rake create name=PAGE_NAME
```

# Compile TeX files
```
$ rake compile
```

or

```
$ rake
```

If stopped, try
```
$ rake --trace
```
and if it stopped while make_pdf, then try below.

# Debug TeX error
```
$ rake make_pdf_debug
```

# Add source codes to TeX file
* put source code in `src` directory
* inject `\lstinputlisting[caption=hoge,label=hoge]{filename}` into where you want to attach it


# Add .png files to TeX file
* put {*.png, *.jpg, *.eps} file in `images` directory
* inject `\includegraphics[width=5cm]{filename.png}` into where you want to attach it
