Introduction
============
This is the source code used to create the principal diagram displayed in ["Measuring Transitions into the Workforce as a Form of Accountability"] and the [poster] using [Circos]. 

Requirements
============

This was developed under Circos-0.52, but has been updated and tested under Circos-0.61. Install Circos into the directory of your choice. Download and extract the set of files in the same directory. All of the necessary data, configuration files, and fonts are included in this directory.

Before creating the image, open the visualizing-transitions.conf folder and edit line 14 to specify where the image files should be saved. For instance, in Windows, the directory could be:
```bat
dir = "C:\Users\user_name\My Documents\visualizing transitions into the workforce\"
```

Create the image by typing the following into the Windows Command Prompt or Terminal:
```bat
cd C:/location/of/folder/from/Github
perl "C:/LocationOfCircosInstallation/bin" -conf visualizing-transitions.conf
```

Files
=====

visualizing-transitions.conf
----------------------------
The primary configuration file which contains references to other necessary configuration and data files. Also includes important information about the size of the image, output directory and image,
 
visualizing-transitions.png / visualizing-transitions.svg
---------------------------------------------------------
The default option provides PNG and SVG images at 1500 x 15000 resolution with a white background.

colors.conf
-----------
Contains the necessary colors specifications to create the document.

fonts.conf
----------
Contains the information about the fonts used in this diagram. This distribution contains the necessary open source font files.

fonts (folder)
--------------
Includes several fonts which are used to create the final diagram. This repository uses the  [Source Sans Pro] font--an open source front released by Adobe. However, the diagram published in the journal used Helvetica.

housekeeping.conf
-----------------
Contains several small, but important parameters needed to create the document. As of Circos-0.62, the housekeeping.conf file is required to generate any Circos output.

ideogram.conf
-------------
Provides additional information about the design of the diagram.

karyotype.clusters.txt
----------------------
Defines each segment of college major and NAICS code, including the short code (e.g., cc1, ic11), name, size, and color. The number following "cc" or "ic" corresponds to the college major and industry cluster found in transitions-data.txt.

segdup.txt
----------
Contains the full data set formatted for Circos input from transitions-data.txt. However, this implementation does not use this file and is included for future use. The data used in this diagram is described under segdup_CAREER-CLUSTER.txt.

segdup_CAREER-CLUSTER.txt
-------------------------
Where CAREER-CLUSTER denotes a college major. Each file contains the career transitions data for a specific college major.

ticks.conf
----------
Specifies the font and format of the tick marks on the outside of the diagram.

transitions-data.txt
--------------------
Contains a tab-separated table of data showing the relationship between college major and industry of employment. The first column of each row displays the college major identifier (1-16 and 99). The college majors are displayed in alphabetical order, with the exception of college parallel, which is displayed in the last row (99).

Each column shows an industrial 2-digit cluster. The top of each column displays the 20 2-digit NAICS code for each cluster.

Contact
=======
You can contact the original author on GitHub, at tomschenkjr@gmail.com, or on Twitter @tomschenkjr.

[poster]: http://tomschenkjr.files.wordpress.com/2009/10/visualizing-transitions-poster-copy1.pdf
[Circos]: http://circos.ca/
["Measuring Transitions into the Workforce as a Form of Accountability"]: https://www.airweb.org/EducationAndEvents/Publications/ProfessionalFiles/Documents/irapps32.pdf
[Source Sans Pro]: http://sourceforge.net/projects/sourcesans.adobe/files/
