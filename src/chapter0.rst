Practical 0 - Installing R and R libraries
==========================================

How to check if R is installed on a Windows PC
----------------------------------------------

In these bioinformatics practicals, you will learn to use the R statistics package
(`www.r-project.org <http://www.r-project.org/>`_), a commonly used
free Statistics software. 

To use R, you first need to install the R program on your computer.

These instructions are for a Windows PC. If you want to install R on a computer that
has a non-Windows operating system (for example, a Macintosh or computer running Linux,
you should download the appropriate R installer for that operating system at 
`http://ftp.heanet.ie/mirrors/cran.r-project.org
<http://ftp.heanet.ie/mirrors/cran.r-project.org/>`_ and 
follow the R installation instructions for the appropriate operating system at 
`http://ftp.heanet.ie/mirrors/cran.r-project.org/doc/FAQ/R-FAQ.html#How-can-R-be-installed_003f 
<http://ftp.heanet.ie/mirrors/cran.r-project.org/doc/FAQ/R-FAQ.html#How-can-R-be-installed_003f>`_).

Before you install R on your computer, the first thing to do is to check whether
R is already installed on your computer (for example, by a previous user). To do this,
click on the "Start" menu at the bottom left of your Windows desktop, and then move your 
mouse over "All Programs" in the menu that pops up. See if "R" appears in the list
of programs that pops up. If it does, it means that R is already installed on your
computer, and you can start R by selecting "R"  (or R X.X.X, where X.X.X gives the version of R, 
eg. R 2.10.0) from the list.

|image1|

If there is an old version of R installed on the Windows PC that you are using,
it is worth installing the latest version of R, to make sure that you have all the
latest R functions available to you to use. 

Installing R on a Windows PC
----------------------------

To install R on your Windows computer, follow these steps:

1. Go to `http://ftp.heanet.ie/mirrors/cran.r-project.org <http://ftp.heanet.ie/mirrors/cran.r-project.org>`_.
2. Under "Download and Install R", click on the "Windows" link.
3. Under "Subdirectories", click on the "base" link.
4. On the next page, you should see a link saying something like "Download R 2.10.1 for Windows" (or R X.X.X, where X.X.X gives the version of R, eg. R 2.11.1). 
   Click on this link.
5. You may be asked if you want to save or run a file "R-2.10.1-win32.exe". Choose "Save" and
   save the file on the Desktop. Then double-click on the icon for the file to run it.
6. You will be asked what language to install it in - choose English.
7. The R Setup Wizard will appear in a window. Click "Next" at the bottom of the R Setup wizard 
   window.
8. The next page says "Information" at the top. Click "Next" again.
9. The next page says "Information" at the top. Click "Next" again.
10. The next page says "Select Destination Location" at the top. 
    By default, it will suggest to install R in "C:\\Program Files" on your computer. 
11. Click "Next" at the bottom of the R Setup wizard window.
12. The next page says "Select components" at the top. Click "Next" again.
13. The next page says "Startup options" at the top. Click "Next" again.
14. The next page says "Select start menu folder" at the top. Click "Next" again.
15. The next page says "Select additional tasks" at the top. Click "Next" again.
16. R should now be installed. This will take about a minute. When R has finished, you will 
    see "Completing the R for Windows Setup Wizard" appear. Click "Finish".
17. If you click on the "Start" button at the bottom left of your computer screen, and then 
    choose "All programs", you can start R by selecting "R"  (or R X.X.X, where 
    X.X.X gives the version of R, eg. R 2.10.0) from the menu of programs. 
    The R console (a rectangle) should pop up:

|image3|

How to install an R library
---------------------------

R comes with some standard libraries that are installed when you install R. However, in these 
practicals we will also use some additional R libraries for bioinformatics (eg. the "SeqinR" 
R library, the "graph" R library, the "igraph" R library, the "RBGL" R library, etc.), and 
these additional libraries do not come with the standard installation of R. 

Once you have installed R on a Windows computer (following the steps above), you can install 
an additional library by following the steps below:

1. Start R by clicking on the "Start" button at the bottom left of your computer screen, 
   choosing "All programs", and starting R by selecting "R" (or R X.X.X, where
   X.X.X gives the version of R, eg. R 2.10.0) from the menu of programs. 
   The R console (a rectangle) should pop up.
2. Once you have started R, you can now install an R library (eg. the SeqinR library) by 
   using the install.packages() R function. For example, to install the SeqinR library, type in
   the R console:

::

    > install.packages("seqinr")

3. This will ask you what website you want to download the package from, you should choose 
   "Ireland" (or another country, if you prefer). This will install the SeqinR package.
4. The SeqinR package is now installed. Whenever you want to use the SeqinR package after this, 
   after starting R, you first have to load the package by typing into the R console:

::

    > library("seqinr")

5. For these practicals, you will need to install the following R libraries using install.packages():
   SeqinR, graph, igraph, ape, RBGL, BoolNet, and LIM:

::

    > install.packages("graph")
    > install.packages("igraph")
    > install.packages("ape")
    > install.packages("RBGL")
    > install.packages("BoolNet")
    > install.packages("LIM")

Note that there are some additional R libraries for bioinformatics that are part of a special 
set of R libraries called Bioconductor (`www.bioconductor.org <http://www.bioconductor.org/>`_) 
such as the "yeastExpData" R library, the "Biostrings" R library, the "Rgraphviz" R library, etc.). 
These Bioconductor libraries need to be installed using a different, Bioconductor-specific procedure 
(see `How to install a Bioconductor R library`_ below).

Furthermore, there is one specific Bioconductor library, "Rgraphviz", which requires some special
installation steps of its own (see `How to install the Rgraphviz R library`_ below).

How to install a Bioconductor R library
---------------------------------------

The procedure above can be used to install the majority of R libraries. However, the
Bioconductor set of bioinformatics R libraries need to be installed by a special procedure.
Bioconductor is a group of R libraries that have been developed for bioinformatics. This includes 
some R libraries that you will be using, such as the "yeastExpData", "Biostrings", etc.


To install the Bioconductor libraries, follow these steps:


1. Start R by clicking on the "Start" button at the bottom left of your computer screen, 
   choosing "All programs", and starting R by selecting "R" (or R X.X.X, where
   X.X.X gives the version of R, eg. R 2.10.0) from the menu of programs. 
   The R console should pop up.
2. Once you have started R, now type in the R console:

::

    > source("http://bioconductor.org/biocLite.R")
    > biocLite()

3. This will install a core set of Bioconductor libraries ("affy", "affydata", "affyPLM", 
   "annaffy", "annotate", "Biobase", "Biostrings", "DynDoc", "gcrma", "genefilter", 
   "geneplotter", "hgu95av2.db", "limma", "marray", "matchprobes", "multtest", "ROC", 
   "vsn", "xtable", "affyQCReport").
   This takes a few minutes (eg. 10 minutes). 
4. At a later date, you may wish to install some extra Bioconductor libraries that do not belong 
   to the core set of Bioconductor libraries. For example, to install the Bioconductor library called 
   "yeastExpData", start R and type in the R console:

::

    > source("http://bioconductor.org/biocLite.R")
    > biocLite("yeastExpData")

5. For these practicals, you will need to install the following Bioconductor libraries that are not
   part of the core Bioconductor set: biomaRt, yeastExpData, and yeastCC:

::

    > biocLite("biomaRt")
    > biocLite("yeastCC")

6. Whenever you want to use a library after installing it, you need to load it into R by typing:

::

   > library("yeastExpData")


How to install the Rgraphviz R library
--------------------------------------

The Rgraphviz R library is part of Bioconductor. It requires some special steps in its 
installation. 

1. Firstly, you need to install the software called Graphviz, which is a software for Windows for 
   drawing graphs. To install Graphviz on your Windows computer, download the Graphviz installer 
   from `http://tinyurl.com/graphviz <http://tinyurl.com/graphviz>`_ (this is a link to 
   `http://www.graphviz.org/pub/graphviz/stable/windows/graphviz-2.20.3.1.msi 
   <http://www.graphviz.org/pub/graphviz/stable/windows/graphviz-2.20.3.1.msi>`_) into your 
   "My Documents" folder on your computer. Note that this is not the latest version of Graphviz 
   available. However, later versions of Graphviz do not work with R. 
2. To install Graphviz, double-click on the icon for the graphviz-2.20.3.1.msi file 
   (the installer file that you downloaded above). This will bring up some instructions on how 
   to install Graphviz. At some point in the instructions you will be asked where to install 
   Graphviz. You should choose to install it in your "My Documents" folder, for example, in 
   "C:\\Documents and Settings\\Joe Bloggs\\My Documents\\Graphviz".
   You need to keep pressing "OK" or "Next" until Graphviz is installed. 
   Note that at two points during the installation process, an error message may pop up, but you 
   should be able to continue installing Graphviz by pressing a button labelled "Continue". 
3. Once Graphviz is installed, you need to add the path (address) to Graphviz to the "PATH" variable on your computer. To do this:

   * Click on the "Start" menu at the bottom left of your Windows desktop, and choose "Control Panel".
   *  Double-click on the "System" icon.
   * The "System Properties" panel will appear.
   * Select the "Advanced" tab at the top of the "Systems Properties" panel.
   * Press the "Environmental Variables" button at the bottom of the "Advanced" panel. 
   * The "Environmental Variables" panel will appear. Only edit the "User variables" (top of panel). NEVER EDIT THE "System variables' (bottom of panel), because that could mess up your computer badly!
   * If there is no "PATH" variable under "User variables", click "New" under "User variables" and add a new user variable called PATH (if there is already a "PATH" variable under "User variables", go to the next step). Now set the value of the "PATH" variable to the "bin" directory for the Graphviz program. For example, if you installed Graphviz in the directory "C:\\Documents and Settings\\Joe Bloggs\\My Documents\\Graphviz" then set the "User variable" PATH variable to be: "C:\\Documents and Settings\\Joe Bloggs\\My Documents\\Graphviz\\bin". NOTE: DO NOT EDIT THE "System variables", as this could mess up your computer very badly!
   * If there is a "PATH" variable under "User variables", select it (if not, go to the next step below). Click "Edit", and edit the value of the "PATH" variable to add the path (address) to the "bin" directory for the Graphviz program. For example, if the value of the "User variable" PATH variable is already "C:\\cygwin\\bin", and if you installed Graphviz in directory "C:\\Documents and Settings\Joe Bloggs\\My Documents\\Graphviz" then edit the "User variable" PATH variable to be: "C:\\Documents and Settings\\Joe Bloggs\\My Documents\\Graphviz\\bin;C:\\cygwin\\bin" (see the picture below). NOTE: DO NOT EDIT THE "System variables", as this could mess up your computer very badly!
   * Press "OK" to exit the Control Panel.

|image4|

4. Once you have installed Graphviz, you then need to install the Rgraphviz R library. 
   Before you do that, if you have R running on your computer at the moment, you need to quit R, 
   and then restart it (this is so that R will recognise the new value of the "PATH" variable, 
   which you have just set in Step 3 above). 
5. The Rgraphviz R library is part of Bioconductor, so you need to install it by starting R, and typing in the R console:

::

    > source("http://bioconductor.org/biocLite.R")
    > biocLite("Rgraphviz") 

6. Once you have installed the Rgraphviz R library, you should now be able to load the Rgraphviz 
   library in R, by typing:

::

    > library("Rgraphviz")

Troubleshooting
---------------

If you have trouble installing R, the reason could be that your computer is set up so that you
are not able to install in the "Program Files" directory. If you think this is the case, you can
ask your System Administrator for help (if you work in a university or company). Alternatively,
you could try the following. In step 10 of `Installing R on a Windows PC`_, instead of installing  
R in the "Program Files" directory of your computer, you can choose to install R your 
"My Documents" folder. For example, if your "My Documents" folder has the path (address) 
"C:\\Documents and Settings\\Joe Bloggs\\My Documents", then click "Browse" and choose: 
"C:\\Documents and Settings\\Joe Bloggs\\My Documents\\R\\R-2.10.1". Then continue steps 11, etc.
of the R installation process. This may solve your R installation problem.

If you have trouble installing R libraries using the install.packages() function, the reason could
be that your computer may not be directly connected to the Internet. For example, many computers
in university teaching labs or companies are indirectly connected to the Internet through a proxy.
In this case, you can ask your System Administrator to help install the R libraries. Alternatively,
you could try the following. You can first install the R librariers on a computer that is
directly connected to the Internet (for example, a computer at home). Once installed,
the R libraries (eg. "yeastExpData") will be found in subdirectories of the directory
where you installed R on that computer. For example, if you installed R in 
"C:\\Documents and Settings\\Student\\My Documents\\R\\R-2.10.1", and then installed the
library yeastExpData, then you should find a subdirectory
"C:\\Documents and Settings\\Student\\My Documents\\R\\R-2.10.1\\library\\yeastExpData".
Say you want to install these libraries on a computer that is not directly connected to the 
Internet. To do this, you can first install R on the computer that is not directly connected
to the Internet. Then copy the subdirectories for the R libraries from the first computer (that
is directly connected to the Internet) onto a USB memory key, and copy them into the
"library" subdirectory of the directory where you have installed R on the second computer.



.. |image1| image:: ../_static/P0_image1.png
.. |image3| image:: ../_static/P0_image3.png
.. |image4| image:: ../_static/P0_image4.png

