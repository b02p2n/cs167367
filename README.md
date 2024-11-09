java c
GEOS 1002/1902 GIS Practical Task
Step-by-step guide
Worth: 20%
Due: Friday 01st November 2024 at 11:59 pm
Content: 5 x maps plus 1200 words (+/- 10%, excluding references)
This is a step-by-step guide on how to create your maps for the GIS practical assignment for this course. If you carefully follow the instructions in this document, you should be able to create high-quality maps using QGIS software and gain an   understanding of the distribution of levels of advantage and disadvantage across Sydney and some of the factors that influence this. This task will mostly be done in your own time, but your tutors will help you in your practical classes in the final three weeks of semester. Remember that making the maps is only half of the exercise, once you have made them you will then need to write a 1200 word report analysing the maps.
Data you are using
Understanding Australian Bureau of Statistics (ABS) census data:
The ABS is where all census data, as well as other population level statistical data, are stored and analysed. Census data is collected from households and workplaces  on a particular night every 5 years; the last two occurred in 2016 and just last year in 2021. For this assessment, we will be focussing on data from 2016.
Census data paints a picture of who we are as Australians and highlights the characteristics – in particular, what is different and what has changed – that make up our big, diverse community. These data – about whom we are, where we have come from, where we live and work – is underpinned by a strong foundation in geographic  location. It is important, therefore, to understand the basics of this geography before  tackling your Census data questions head-on.
Before using ABS data, it is important to understand the geography of how the data   is organised. All census data is collected and coded to specific household addresses and then aggregated in ‘Meshblocks’ . Meshblocks are aggregated to form. Statistical  Area level 1 (SA1) data. There are usually about 200 hundred households per SA1.
This means that, as population density of an area diminishes, the size of the SA1 increases. There are also other factors affecting the size of the SA1 (such as topography – SA1 boundaries are often defined by boundaries in the landscape).
Meshblocks and SA1s can be combined to form. a range of other ABS and non-ABS geographies. For example, a collection of SA1s form. SA2s, all the way up to SA4 then States. SA1s can also be aggregated to form. other non-ABS boundaries, including suburbs, electoral divisions, local government areas (LGAs) and so on. The diagram on the next page provides a schematic account of the hierarchy of geography. It is important to understand how the basic hierarchy of geography works before attempting to map out census data. The diagram below shows the boundaries up to SA3 for the inner Sydney area.
Note that data are not always published at the Meshblock scale, because of confidentiality and privacy issues. It is important to think about what scale is best suited to representing the information you want to display.

In this practical exercise, you will be using data at a range of different scales, including local government area boundaries (LGAs) and Statistical Area level 2 to level 4 boundaries (SA2 to SA4) depending on availability of data and the effectiveness of its display.
Local Government Areas (LGAs) approximate officially gazetted LGAs as defined by each State and Territory Local Government Department. These are good for understanding characteristics of an individual LGA at a point in time. Because these boundaries sometimes change between Census years, SA2s or SA3s might be better alternatives if you’re interested in trends or comparisons overtime. Local Government Areas cover incorporated areas of Australia only. Incorporated areas are legally designated parts of a State or Territory over which incorporated local governing bodies have responsibility. The major areas of Australia not administered by incorporated bodies are the northern parts of South Australia, and all the Australian Capital Territory and the Other Territories. These regions are identified as ‘Unincorporated’ in the ASGS Local Government Areas structure.
Statistical Areas Level 2 boundaries (SA2s) are medium-sized general-purpose areas built up from whole Statistical Areas Level 1. Their purpose is to represent a community that interacts together socially and economically. There are 2,310 SA2 regions covering the whole of Australia without gaps or overlaps. These include 18 non-spatial SA2 special purpose codes, comprising Migratory–Offshore– Shipping and No Usual Address codes for each State and Territory. SA2s will be the most common data distribution we will be working with in this task.
Understanding SEIFA
To map advantage and disadvantage, we are going to use SEIFA data (Socio-Economic Indexes for Areas). The four indexes of SEIFA each capture a slightly different concept of socio-economic advantage and disadvantage.
The ABS broadly defines relative socio-economic advantage and disadvantage in terms of people's access to material and social resources, and their ability to participate in society.
The four indexes included in SEIFA are:
•   the Index of Relative Socio-economic Disadvantage (IRSD)
•   the Index of Relative Socio-economic Advantage and Disadvantage (IRSAD)
•   the Index of Economic Resources (IER)
•   the Index of Education and Occupation (IEO)
Each index aims to capture a slightly different aspect of relative advantage and/or disadvantage and is constructed using different variables. It is therefore likely that the same area will have different rankings on each index. For example, it is possible for an area to rank relatively lowly in the Disadvantage index but not in the Advantage and Disadvantage index, because these indexes include different variables.
The Index of Relative Disadvantage identifies and ranks areas in terms of their relative socio-economic disadvantage. The Index of Relative Advantage and Disadvantage broadly measures both advantage and disadvantage (IRSAD), while the Index of Education and Occupation and the Index of Economic Resources both measure aspects of socio-economic advantage and disadvantage. It is therefore important to clarify what is meant by relative socio-economic advantage and disadvantage, as this is the concept SEIFA aims to summarise from the numerous Census variables available for analysis.
While income is the strongest variable in IRSAD, employment status and car ownership are also key indicators in this index. For the purposes of this practical exercise, we will be focusing on IRSAD to map advantage and disadvantage and consequently compare these to these key variables related to employment and mobility. We will also look at mode of transport to work and map this across Sydney to identify spatial trends and identify equity issues with relation to access to public transport (in this case, the train network). 
OK, let’s get started.
Making your first map: IRSAD vs unemployment
For this unit you will be using QGIS, an open source GIS software. It’s quite similar in functionality to ArcGIS that you would have used if you took GEOS1001 last semester, though it still will probably take some time to become familiar with the layout of this software. The advantage of using QGIS over ArcGIS is that it’s free for anyone to download and use, and it works for both PC and Mac computers. If you haven’t yet installed the software on your computer, go back to the Canvas page for this assignment and follow the linked instructions to download and install it. You will also need to download the “GIS data payload” zip file from the Canvas page and extract the files to your computer.
We suggest creating a new map file for each map as otherwise your map window will get very crowded and it becomes easier to lose information. If you have the software  installed and running on your computer, you can begin making your first map using the instructions below.
1.  Run QGIS and click on the “ New Project” button in the top left corner

2.  Next we will add a basemap, this will provide a background to the shapefiles that you will be displaying and manipulating. In the browser panel on the left side of the screen, expand the “XYZ Tiles” tab and double click “OpenStreetMap” . This will open up a global street map.

3.  Zoom in on the Sydney region on the east coast of Australia. This is the
region we are working with for all of our maps. You don’t have to zoom in too far, just enough so you can see the greater Sydney area and some of the regions and water around it.

4.  Now is a good time to save your work. I will add some reminders to save
throughout these instructions, but it’s a good idea to regularly save your work as you go as the software can occasionally crash. Call your file “Map 1” and save it to the hard drive if you are using your own computer, or to OneDrive or a USB stick if you are using a university computer.
5.  Next we will add the first shapefile to your map.
NOTE: If you haven’t yet unzipped your “GIS data payload.zip” file, you will not be able to add it to QGIS. To extract the file in Windows, right click on it and click “Extract All” . On a Mac, double-click the zip file and it should automatically extract the files. If you look through the files you will be using, you will notice many files with the same name and a different filename extension to it – this is how GIS shapefiles are stored. They typically have 5 or 6 files associated with each GIS file.
To add your first shapefile, click the “ Layer” menu at the top of the screen and then navigate down to “Add Layer” and click “Add Vector Layer”
When the “Data Source Manager” window pops up click on the  button  (next to “Source”) and navigate to the “GIS data payload” folder and open it up. Go to the “Sydney_boundary” folder. In there, you will find 6 files, all named “2016_GreaterSydney” . The file you need to add is called “2016_GreaterSydney.shp” . When adding any shapefiles, the “ .shp” file will always be the one you add – it can also be easily identified if your computer  shows the size of each file, as it will always be the largest file in the folder by a big margin. Once you have selected the .shp file, click “Open”, and then in  the Data Source Manager window, click “Add” . A window may pop up asking you to select the transformation for this file, just click “Ok”, close the Data 代 写GEOS 1002/1902 GIS Practical Task
代做程序编程语言Source Manager and the file will display in your QGIS map window. Note: the colour of the shapefile is randomised when added, so yours may be a different colour to the one in my screenshot.

6.  This shapefile is displaying most of Greater Sydney, and this is the area we
will be working with. How much you see will depend on your zoom level and your screen size, but as long as most of this shapefile is visible, this is okay. Obviously as a solid shape it doesn’t allow us to see much, so we are going to edit it so that it is just an outline. Double-click the “2016_GreaterSydney” file in the layers panel on the left side of the window and go to the “Symbology” section. You will see that it is currently displayed as a single symbol with a simple fill of one colour. If you click on “Simple Fill” near the top of this window, more details on the type of fill will appear. We want to change this so this file is just displayed by its outline. Next to “Symbol Layer Type”, click “Simple Fill” . In the drop down menu, change it to “Outline: Simple Line” . Next change the Stroke width to 0.5 millimetres and press Ok.

7.  The shapefile should now display as an outline with the map of Sydney visible beneath it.

8.  Next we will add the Index of Relative Advantage and Disadvantage shapefile to our map. Using the instructions from step 5, click the Layer → Add Layer   → Add Vector Layer menu item, click the 3 dots, navigate to the IRSAD folder and add the “IRSAD_LGA.shp” file. You’ll notice that this map is much larger than the Greater Sydney one, it covers all of New South Wales. You’ll also notice that this shapefile is broken up into smaller pieces (called polygons), this is because it has been broken up into LGAs. Stay focused on Sydney though.
9.  This map looks quite simple, but contains a lot more information than it initially seems. We can view this information using the attribute table. Depending on  your version of the software, you may need to first activate the plugin.
Open the Plugins menu at the top of the screen and then click on Manage and Install Plugins. When the window pops up, start typing in RasterAttributeTable and it should appear, then you need to click “Install Plugin” . If the plugin doesn’t appear when you search for it, it means that it’s already installed and you can skip this step.

Once you have installed the Raster Attribute Table plugin, close this window and right click on the IRSAD_LGA file in the layers panel and click “Open Attribute Table” . You’ll see that for each LGA, this file has the data on the name, area, population (in 2016) and some other categories – Score, Rank,  Decile and Percentile. “Decile” is the category we are interested in, as this is  the IRSAD ranking. Once you are finished looking at the table, you can close it.

10.What we want to do is display the map according to the IRSAD decile of each LGA. To do this, double click on the IRSAD_LGA file and open up the Symbology section, same as what you did for the Greater Sydney shapefile in step 6. This time, click on Single Symbol at the top of the screen and change it to Categorised. Under “Value”, we want to select Decile, then near the bottom of the window click “Classify” . The values of 1 - 10 and “all other   values” will pop up.

The first thing to do is remove the “all other values” category. We don’t need
it. Click the “all other values” text and click the  button near the bottom of  the screen. The rest of the categories we will change from random colours to   a meaningful colour scheme. Under “Colour Ramp”, click on the down arrow   to the right of where it says “Random colours” and select a colour scheme that is a spectrum (that is, gradually transforming from one colour to another).

11. If you followed the steps above, your map should look something like the
above image (with whichever colour scheme you chose). To see what these colours mean, click the little arrow next to “IRSAD_LGA” in the layers panel  on the left and a legend will pop up (you can see this in the above image).
What this is showing is that each colour is associated with an IRSAD value,   where an LGA with a value of 1 is ranked as the most disadvantaged and an LGA with a value of 10 is the most advantaged.
Take a moment to look at your map. What trends can you see about the   spatial distribution of the more advantaged and disadvantaged regions of Sydney?
12. Now is probably a good time to save your work again!
13.You will notice that with the IRSAD_LGA shapefile on display, you can no
longer see the 2016_GreaterSydney boundary. This is because QGIS uses a top-down display where the files that are highest on the list in the Layers
panel are on top of the files below them. If you untick the IRSAD_LGA file in this panel, it will disappear and you can see the greater Sydney boundary
again. Tick the IRSAD shapefile so it is on display again and make the
2016_GreaterSydney shapefile visible by right clicking it and clicking “ Move  to Top” . This will move the file to the top of the list and make it visible again.
14.Next we will add another shapefile to compare the rate of unemployment with the levels of advantage and disadvantage in Sydney. Click Layer → Add
Layer → Add Vector Layer again, navigate to the “ Unemployment” folder  and add the “SA2_unemployment.shp” file. This will look quite similar to the  IRSAD shapefile when you first added it, though divided into smaller areas – this is because this file is categorised according to Statistical Area Level 2
(SA2) rather than LGA. If you view the attribute table for this file (step 9) you will see another column – “PER_UNEMPL”, this column is giving us the
percentage of residents that were unemployed in each SA2 region in 2016.
15.Close the attribute table and double click on the SA2_unemployment file and open up Symbology. We are now going to change the symbology of this
shapefile in a similar way to what we did with the IRSAD file in step 10 but
with a few changes. In the Symbology window, click “Single Symbol” and this time change it to “Graduated” . Under “Value” choose “ Per_UNEMPL” and
click classify at the bottom. The unemployment rate data should pop up, but
this time in ranges (0 - 4.1%, 4.1 - 5.3% etc.). The colour scheme should
automatically be a spectrum for this shapefile, so click on the down arrow next to “Colour ramp” and choose a colour scheme you would like to use to display levels of unemployment. Click Ok and have a look at the map you’ve created.  Can you see any trends of which areas of Sydney have higher levels of
unemployment than others?
16.What would be useful would be to see if there is any relationship between
levels of unemployment and levels of advantage and disadvantage in Sydney, but unfortunately your shiny new unemployment map is now in the way of
your IRSAD map. To fix this, we are going to change the way unemployment is displayed so that the IRSAD levels are also visible.
Go back to the symbology settings for the unemployment shapefile. Near the
top of this window is a category called “Symbol” with a solid block of a
random colour next to it. Either click on this block of colour or click the arrow
next to it and then select “Configure Symbol” . The Symbol Settings window  will pop up you need to click on the text that says “Simple Fill” . In the section that appears below, under “Symbol layer type” you need to click on “Simple
Fill” and change it to “Centroid Fill” . This means that instead of displaying the unemployment rate as shaded polygons, it will instead be displayed as a
smaller symbol, allowing you to see both layers. Genius!

In the new section that appears, untick “Draw markers on every part of multi- part features” and then click “Simple Marker” to edit the marker you will use.

At this point you probably don’t need to change much, but you can come back to this window if you want to use a different shape or change the shape size.   For now, press Ok and close the Symbology window. Your map should now look something like this, according to whichever colour scheme you chose:

Make sure that the two colour schemes you have chosen are different enough from each other to see the trends! You’ll find that a red circle on a red
background is rather difficult to follow. 17.Save your work again
18.Now that we have the shapefiles we need for our first map, we are going to try and put them all together to make a polished map worthy of your GIS
assignment. But before this, we want to move the Greater Sydney shapefile to the top of the list so that it is on display again (right click → move to top).
Once you’ve done this, click the Project menu and click New Print Layout. A window will pop up asking you to give this map a name, call it something
meaningful such as “IRSAD vs Unemployment” and press Ok. A New blank  window will appear. Note: if you ever need to go back and edit a map, or you get halfway through creating a map and you want to close it and   finish it later, you can load it by going to Projects > Layouts.

19.The first thing we need to do is add the map to this page. Click the Add item  menu and choose Add map. Initially it will look like nothing has happened but you will notice that the cursor has changed. Try drawing a box on the blank sheet and see what happens. Your map is back! Click and drag from the corners of the map so that it fills up the whole sheet.



Your map should cover an area similar to this. If you need to move it or zoom in/out, click on the map and in the Item Properties panel that appears on the right side and click the button. This will allow you to click and drag your     map so that it is focused on the right area. You can also use your mouse
wheel to zoom in and out. If you find that it zooms in and out too much, you
can manually change the zoom by altering the Scale value in the Item
Properties panel (hint, I find that a scale of somewhere between 300,000 and 500,000 is the best for most of my maps of Sydney, but play around with it to see what works for you). Once you are satisfied with the display area, click
the 画 button on the left side (or possibly top) of the screen.
20.Now we need to add some display elements to your map. Try to remember that every GIS map you make needs to have a title, scale bar, north arrow and legend. This is important and is an easy way to lose marks if you forget.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
