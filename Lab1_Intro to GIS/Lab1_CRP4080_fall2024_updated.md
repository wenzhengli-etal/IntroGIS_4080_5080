**Lab Exercise #1: Intro to ArcGIS Pro Due Tuesday, 09/10/2024**

## CRP 4080: Introduction to Geographic Information Systems 

## Instructor: Wenzheng Li (wl563)

## Lab TAs:  Gauri Nagpal (gn247); Shubham Singh (ss3736); Anika Sinthy (ats243)

## Location: Sibley 305, Barclay Gibbs Jones Computer Lab

## Points Possible: 40 

By the end of this lab, you should be familiar with the basic functions
and organization of ArcGIS Pro. You should be able to create folders,
add data, create a unique layer map and put together a map layout, as
well as use some of the basic analysis tools in Arc Pro, and save your
project.

At the beginning of each lab, you should copy the data from the course
folder or Canvas site to your own folder at the beginning of each lab.
Also, be sure to keep your course folder organized so that you will be
able to find things in the future. Take the time now to set up a system
that you can build upon in a logical manner.

Examine data structure in your Lab1_data folder. There is only one
shapefile for polling places for Tompkins County (we will be adding more
later), but it is comprised of a number of files: a .shp file (shape
file) and then several support files: .sbn, .sbx, .shx, .prj (this one
defines the projection) and .dbf (the last one contains the attribute
information).

1.  **[Creating a project]{.underline}**

You will notice that you have the option of opening a recent project or
template. As we have not created a project, on the opening page, please
click on the "Map" option under Blank Templates.

Figure 1. Select project folder

The "Create a new project" dialog box opens. Give your project a name
(e.g., "lab_1"), and select the project folder you created with the lab
1 data (Figure 1). Uncheck the "Create a new folder for this
project" box and click OK again to create the project (Figure 2).

Figure 2. Create new project dialog.

## User Interface 

The interface of ArcGIS Pro includes four major components: a
**Ribbon**, a **Contents Pane**, a Map (View), and a Catalog Pane and
Others (see Figure 3).

![A map of the united states Description automatically
generated](media/image5.png){width="5.874453193350831in"
height="3.2146314523184603in"}

*Figure 3: Main GUI window.*

You will see a **Contents** pane (Figure 3, left side), a **Catalog**
pane (Figure 3, right side). Panes are windows that help you manage
views and projects, or that give you access to specific functionality.

The **Contents** pane lists items in the active view, such as layers in
a map, or layout elements in a layout. The **Catalog** pane lists mostly
data sources that belong to the project, such as databases, toolboxes,
and folder connections. The **Catalog** pane also provides access to
portal items, such as web layers.

## Open and dock panes

As you work, you\'ll often open and close panes that you need for
specific tasks. The view above shows the Contents and Catalog panes in a
docked state. You may also want to reposition panes or minimize them to
make room for maps and other views. You can do this by dragging them
around the window or dragging them off the window to make them a
separate floating window (Figure 4).

![Graphical user interface, application, map Description automatically
generated](media/image6.png){width="6.0in" height="2.7875in"}*Figure 4.
Main GUI window with Panes as separate windows.*

Pane states are independent of the project and will often appear in the
arrangement of the previous ArcGIS Pro session. When you accidentally
close them, you can go to View ---\> Windows and you can turn on them
again.

## Ribbon

Above the map view is the **ribbon (**Figure 5**)**. The ribbon has a
set of **tabs**---Map, Insert, Analysis, View, Edit, Imagery, and
Share---that are always present when a map view is active. Each **tab**
organizes a set of **tools** with similar or thematically grouped
functions.

For example, the Map tab has tools for interacting with the map. On the
Map tab, the Explore tool ![Explore
Tool](media/image7.png){width="0.16666666666666666in"
height="0.16666666666666666in"} is selected in the Navigate group. The
Explore tool ![Explore
Tool](media/image7.png){width="0.16666666666666666in"
height="0.16666666666666666in"} allows you to move around the map and to
read information about map features of interest.

On the ribbon, click the **View** tab. In the **Windows** group, click
**Reset Panes** ![Reset
Panes](media/image8.png){width="0.16666666666666666in"
height="0.16666666666666666in"} and click **Reset Panes for Mapping
(Default)**.

If the panes are stacked, they may also have tabs at the bottom that
allow you to switch from one pane to the other.

Figure 5. Ribbon with tabs and groups

As you drag the pane, docking targets---represented by a blue
shadow---appear in the center of the map view and at the edges of the
application window. Each target represents an area where the pane can be
positioned.

Hover over a docking target. You can see where the pane will be docked
if you drop it on that target.

The panes should now be docked on opposite sides of the ArcGIS Pro
window. By default, panes stay open as you work. You can autohide a pane
by clicking ![Auto Hide](media/image11.png){width="0.2in"
height="0.2in"} so it doesn\'t take up space when you aren\'t using it.
You can then toggle the panes to hide and reveal them.

Now that we have covered the very basic ways of interacting with the
main GUI, experiment a little with the configuration to find a mode that
works for you.

2.  **[Making a map]{.underline}**

Now we will begin to make a local map of Ithaca polling places using the
data from ArcGIS online and the Lab 1 data folder. We will make a map
with Parcels, ...

First, we should zoom to Ithaca so we can see the data once we load it.

1.  Under the Map tab, use the Locate tool to find Ithaca, NY.
    ![](media/image12.png){width="0.38149496937882765in"
    height="0.3678696412948381in"}

2.  Adjust the base map

    a.  Go to Map ribbon, under layer group, and click Basemap.
        ![Graphical user interface, application, Word Description
        automatically
        generated](media/image13.png){width="1.5972222222222223in"
        height="0.6944444444444444in"}

    b.  You have a number of options. Select the one you prefer (In my
        case, the OpenStreetMap).

## Add a portal connection to ArcGIS online

There are two ways to add data in ArcGIS Pro: local data and online
data. The new ArcGIS Pro is integrated with ArcGIS online, a cloud-based
tool that users can upload datasets to. You can search and add data that
is uploaded and maintained by other users in the ArcGIS cloud.

To add an ArcGIS online portal connection, complete the following steps:

1.  ![A screenshot of a computer Description automatically
    generated](media/image14.png){width="2.7694444444444444in"
    height="2.1666666666666665in"}Click the **Project** tab on the
    ribbon and Click the **Portals** page from the left side (see Figure
    6).

2.  Click **Add Portal**. Enter the URL for the portal on the **Add
    Portal** dialog box: <https://cugis.maps.arcgis.com> and Click
    **OK**.

3.  Optionally sign-in to the portal. Click the **Options** button
    ![Options](media/image15.png){width="0.16666666666666666in"
    height="0.10277777777777777in"} or right-click the portal and Click
    **Sign in**. Enter your Cornell NetID as the username and NetID
    password. You can also [sign in to a portal using a web
    browser](https://pro.arcgis.com/en/pro-app/2.8/help/projects/sign-in-to-your-organization.htm#ESRI_SECTION1_1CAD4AEC94E54C1BA236F5CB2DC197D0).

Figure 6. Add portal

4.  To make the new connection your active portal, Right-click the URL
    Click **Set As Active Portal**. To confirm this, you should see a
    green circle with a check mark next to this portal.

Click the back arrow in the top left corner to return to map view. Now
we will add data to the map from the portal we just added. On the
**Map** tab, click **Add Data** ![Add
Data](media/image16.png){width="0.16666666666666666in"
height="0.16666666666666666in"}. Select ArcGIS Online (Figure 7).

We will now use the search bar at the top to search for datasets. Let's
search for data owned by TompkinsGIS:

Figure 7. Add data dialogue

-   Tompkins County parcels (search for "Parcels Tompkins", then add
    Parcels_Public),

-   building footprints (TCBuildings),

-   streets (TcStreetEx) and

-   municipal boundaries (TCMunis).

As you search, many options come up. Find the data sets that are owned
by TompkinsGIS. For each layer, select the appropriate layer and Click
OK to add it to the map. Make sure you can view the layers.

-   Notice that some layers may not render properly when you are zoomed
    out (e.g., TCParcels). You can change this setting by right-clicking
    on the layer, selecting Properties, and under General, change
    Visible Scale Range to "show layer at all scales." For some layers,
    like TCBuildings, you will want "show layer between certain scales"
    to speed up rendering when you are zoomed out.

Now, let's add another layer from your **local drive**.

1.  In the **Add Data** dialog, find your Lab 1 folder

2.  select polling_places13.shp -- polling locations. Note that only the
    file with the **.shp** extension shows up.

You can turn the various "layers" on and off, as well as rearrange the
order in which they are presented by dragging them. **Rearrange the
order from the top; polling_places13, TcStreetEx, TCBuildings, Parcels,
and TCMunis**.

Note that there are shortcuts for commonly used functions. By right
clicking on the layer in the Contents pane, you can directly access the
attribute table and other options (e.g. remove layer, copy layer, etc.).
"**Zoom to layer**" zooms to the full extent of the specific layer.

## Attribute table

Now we will examine the attribute table, which is tabular data about
each feature in the shapefile. In the **Contents** pane, right click
TCParcels layer and go to Attribute Table.

![](media/image19.png){width="1.7019466316710412in"
height="0.26843503937007873in"}

A window opens with the **parcels** layer attributes (Figure 8.
Attribute table window), which will contain the attribute information
about this layer.

![](media/image20.png){width="6.305637576552931in"
height="1.3921533245844269in"}*Figure 8. Attribute table window*

The attribute table is like a spread sheet in which rows represent
features or shapes in the shapefile and columns represent attributes of
those features. In this case, each row represents a parcel and each
column corresponds to the attributes of the parcels. There is a
[one-to-one]{.underline} link between the features in the map and the
rows in the table. This allows users to retrieve attribute information
about any feature in the map. It also allows users to display one or
more attributes for each geographic feature and create maps displaying
attribute values.

The first column in the attribute table (**FID**) is a Feature ID, which
is a unique number assigned to each feature, starting from zero. The
**FID** is assigned automatically and cannot (and should not) be
changed. The last column in the attribute table shows the
[type]{.underline} of feature (in this case polygon). The other columns
all contain various attribute information. Some of these are
recognizable, while others are probably not, and will require an
examination of the metadata to determine what they represent.

Now let's begin to assess the data. One keyway of doing this is through
descriptive statistics, which summarize the distribution of attributes
in our data.

1.  Right click on the "Calcacres" column heading and

2.  Go to 'Statistics'. This will display a basic frequency distribution
    of parcel size.

Not particularly helpful. We can make a more detailed summary table.

3.  Right click on TCParcels and Click to Create
    Chart![](media/image21.png){width="0.23943897637795275in"
    height="0.3373917322834646in"}.

4.  Click Bar chart ![](media/image21.png){width="1.090602580927384in"
    height="0.21812007874015749in"}.

In Chart properties,

5.  Select PROPCLASS as the category, SUM as the aggregation, and
    CALACRES as the Numeric field.

6.  You may need to click "Apply", or simply wait for the new chart to
    render.

This produces a more useful chart of acreage according to the property
class. We could then export this chart as an image file using the Export
button.

![](media/image22.png){width="5.709928915135608in"
height="1.6242683727034122in"}

## Change the layer's name

The current layer names and map names are not particularly legible. We
can change layer names, so they are more legible and understandable
(note: sometimes you may have to open the attribute table and look for
clues to determine a more appropriate title).

1)  First, give our Map a name.

    a)  In the Contents pane, right click on the Map and

    b)  Go to Map properties.

    c)  Under the General tab, change the name to 'Ithaca'. Click OK.

2)  let us change the name of a layer.

    a)  Right click on "TcStreetEx" layer and Select "Properties".

    b)  In the Layer Properties dialog box, select the "General" tab.

    c)  Under "Name" type "Tompkins County Roads" and Click OK.

3)  Change so the others read as follows:

    -   TCBuildings: Building footprints

    -   TCMunis: Municipal boundaries

    -   polling_places13: Polling locations

    -   TcStreets: Tompkins County roads

    -   Tompkins County Parcels: Parcels

Note that you are not changing the name of the original layer files,
only the name as it appears within the software.

# 3. Create a Map using the Municipal Boundaries layer

## Symbology

1)  Turn off all layers except for Municipal boundaries.

Figure 9. Symbology panel

2)  Right click on Municipal boundaries layer and look at the attribute
    table. Note that while each municipality has a Name, these are often
    duplicate and contingent on the 'MUNITYPE' (City of Ithaca, Town of
    Ithaca, etc.). The attribute 'FULLNAME' will give us a unique name
    for each polygon.

3)  Close the table, right click again and

4)  Click on "Symbology" which will open the Symbology panel (Figure 9)

Since municipalities are *nominal* (also referred to as categorical)
data, we want to create a 'unique values' map.

5)  Under primary symbology, go to unique values.

6)  For "Field 1," choose FULLNAME, then

7)  Click the ***add all values*** button
    ![](media/image25.png){width="0.2956266404199475in"
    height="0.2737270341207349in"} ArcGIS assigns colors according to
    the color scheme that is currently selected.

If you click on the down arrow for Color scheme, you will find many
other choices. Select one of your choice. If you want to edit a
particular feature, you double-click on it.

8)  Double click on 'City of Ithaca' and change its color. Note that the
    symbol selector also includes pattern symbols in addition to solid
    colors.

> Now to see the full extent of the layer, right click on the
> municipalities layer and go to 'Zoom to layer'

## Creating Labels

1)  Close the Symbology pane. Again, right click on the municipalities
    layer in the Contents and

Figure 10. Label class dialog

2)  Go to the Labeling properties.

3)  Find the Expression box (Figure 10)

4)  Notice the default attribute ('\$feature.NAME').

5)  Replace "NAME" with "FULLNAME"

6)  Click Apply.

7)  Return to the table of contents,

8)  Right click on the municipalities layer, and go to 'Label' -- the
    name of each municipality will now appear.

You have now created a *unique value map* for Tompkins County
municipalities. You can also edit the placement, color, size, character
case (upper or lower) and other attributes of labels.

Click
[here](https://pro.arcgis.com/en/pro-app/latest/get-started/label-your-map.htm)
for extensive tutorial on label formatting.

## Adjusting Symbology

Now we will explore other ways to adjust the layer symbologies, or how
they are visualized on the map, which is a powerful design and
analytical tool in GIS. Adjust the symbology of other features.

1)  Right click on the Polling Locations, and

2)  Select "Symbology." This opens the Symbology dialog (Figure 11).

3)  Change the points to stars (note that you can adjust the color and
    size as well)

. Symbology dialog for point layer

4)  You will note that several of the layers from ArcGIS online were
    added with their symbology already classified. For example, streets
    are already classified according to the Maintenance variable, and
    Buildings are categorized according to type (BTYPE)

5)  Right click on the Parcels layer and go to symbology. In the
    symbology dialog box, select 'unique values' as the primary
    symbology, 'PROPCLASS' as the field.

> We now have created a *unique value* map of parcels categorized
> according to property type.

6)  Please see
    [here](https://pro.arcgis.com/en/pro-app/latest/get-started/symbolize-your-data.htm)
    for an extensive tutorial on symbology in ArcGIS Pro.

## Save your Project

Save your project. Above the project tab, click Save:
![](media/image29.png){width="0.2757305336832896in"
height="0.2511428258967629in"}. **Remember to save your project along
the way!**

ArcGIS Pro uses \*.aprx as its default project file type. A project is a
set of ArcGIS geographic and database files that have been saved in a
certain organized form. A project finds the data based on where they are
located using file paths and URLs. You are ***not*** resaving and
changing any of the data in the map. If you move the data or the project
without moving the other one, your project document will not find the
data!

From now on, you should create and save a project for each lab or
homework assignment! First, copy all relevant data from the course
folder to a (well labeled) folder you have created on your drive. Then
create a new project. Save your project back into your folder with the
data so you can return back to it, remember, the project is simply
pointing to the data -- if it can't find the data you won't be able to
recreate the project.

Once you resume an ongoing ArcGIS Pro Project and find a red exclamation
point ![](media/image30.png){width="0.12547134733158355in"
height="0.2419805336832896in"} after certain layers. It means that you
edit or change the data files (for example: changed the name of the data
in folder or moved them to other directories) related to an existing
project. The current project connection to the corresponding dataset is
invalid. You have to rebuild the connection to restore the saved
progress. See this detailed instruction on how to [**repair project
items**](https://pro.arcgis.com/en/pro-app/2.8/help/projects/repair-project-items.htm).

**[\
]{.underline}**

**[4. Creating a map layout]{.underline}**

Most lab assignments require you to submit maps. We can make maps using
a map layout. For this layout, we will include a **zoomed view of
downtown Ithaca** that displays **streets, parcels, and polling
locations** with a **context map of Tompkins County** that has **all the
municipal boundaries labeled with municipal names included**. Yes, each
time you fail to include one of these elements you will lose points.

**Most importantly, these are the basic elements you should include to
your map layout every time you create a map, or you will lose points on
your homework.**

1.  Title (and sub-titles if necessary)

2.  Legend: Is it legible? Does it make sense? Are the titles coherent?
    Do the number breaks make sense?

3.  Metadata/notes: Tell us about the map! Who created it? Where? Date?
    What is the data source? Projection? Units? How is the data
    classified? What is the purpose of the map?

4.  Scale bar: Do units (feet, miles), breaks (not too many!) make
    sense?

5.  A north arrow

## Creating a layout

1.  Insert a blank layout.

    a.  On the ribbon, click the **Insert** tab if necessary.

    b.  In the **Project** group, click **New Layout** ![New
        Layout](media/image31.png){width="0.16666666666666666in"
        height="0.16666666666666666in"} to show page size and
        orientation options.

    c.  Under **ANSI - Landscape**, click **Letter** (this is a matter
        of preference)

A new, blank layout view opens.

2.  Name the layout.

    a.  Activate the Layout tab.

    b.  In the Contents pane, right-click the layout,

    c.  Click **Properties**

    d.  Click General,

    e.  Change the name from **Layout** to 'Ithaca'.

## Insert a map frame

Now let's create a **Map Frame** in our layout.

a)  Under the **Insert** tab, click the **Map Frame** drop-down arrow.

b)  Select the frame with your data (not the default extent).

c)  Use your mouse to draw a large rectangle on the layout and wait for
    it to load.

The map frame is added to the layout. It is currently selected, as
indicated by selection handles. This will allow us to move it around the
page to position it correctly.

d)  Right click inside the frame and

e)  Select 'Activate' (this can also be accessed through the Layout Tab
    at the top).

This will allow you to manipulate the layout data within the map frame
and select the correct size and position for your data.

f)  In the **Contents** pane, right-click **Map** and

g)  Click **Properties**.

h)  In the Map Frame **Properties** dialog box, click the **General**
    tab if necessary.

i)  Change the name of the Map Frame to 'Ithaca'. Notice at the top, we
    can toggle between the layout view and the map view.

This will be our main Map Frame, and the context map will have a
different name.

In the Layout view, zoom in to the City of Ithaca area (remember you
must have the map frame activated).

-   The symbology of the polling places should be red stars.

-   The symbology of the streets should be a single symbol.

-   The symbology of the parcels should be categorized according to
    property class.

To **close an activation** session to avoid unintended changes, click
the back to layout ![](media/image32.png){width="1.7815791776027996in"
height="0.22366141732283465in"} Or just simply click the red-cross on
the top-right of your layout frame.

## Add a second map frame (context map)

Now, let us create a context map. We need to create a new Map (not a Map
Frame) before we can add this as a new Map Frame.

1)  Under the **insert** tab, add a **New Map**. Note that insert a map,
    not a layout frame!!! In the **Contents pane**, Change the name to
    'Tompkins County'.

2)  This time, add only the Municipal boundaries layer to this map
    frame. You can copy and paste from the Ithaca Map.

![A screenshot of a computer Description automatically
generated](media/image33.png){width="6.0in"
height="1.5104166666666667in"}

3)  Rename the layer and create labels for their full names (feel free
    to experiment with placement and stylistic considerations).

4)  Now add a second Map Frame to your **Ithaca layout** to display the
    Tompkins County map. This time when you select Map Frame drop down,
    you will see a second Map to select from, the Tompkins County Map.

5)  Within the Table of contents, rename this Map frame 'Tompkins
    County'.

Adding data frames is useful if you wish to include inset/overview maps,
or to display maps of different variables in the same layout (e.g. for a
poster presentation). Now, you can individually adjust each of the map
frames on the page. To do that remember to **activate and
de-activate** different map frames.

## Add map extent indicator

1)  Let us include an extent indicator to indicate the relationship
    between the two map frames.

    a)  ![Graphical user interface, application, Word Description
        automatically
        generated](media/image34.png){width="1.9444444444444444in"
        height="0.6388888888888888in"}Click the Map Frame of Tompkins
        County

    b)  On the **Insert** tab, click the **Extent Indicator** drop-down
        arrow

2)  Format the Extent Frame (Figure 13)

    a)  Select the Ithaca map frame. (You must be clear what kind of
        relationship you want to indicate among these maps. In this
        case, the indicator is from Tompkins County to Ithaca!)

    b)  Right-click the **Extent of Ithaca** layer in the Contents pane
        to open the **Format Extent Indicator** pane.

    c)  In the **Format Extent Indicator** pane, under **Extent
        Indicator**, click the symbol, select an appropriate symbol for
        the extent map.

    d)  Under Extent Indicator, check the **Apply Symbol outside extent
        tab**, and

    e)  for Leader style select **Callout to Edges**.

This draws lines linking the source map frame and the extent indicator
(Figure 13).

![A map of a city Description automatically
generated](media/image35.png){width="4.994396325459317in"
height="2.982186132983377in"}

Figure 13. Context frame, detail frame, and callout lines contextualize
this map nicely.

## Map layout elements

You\'ll add a legend, north arrow, and scale bar to the layout. The
legend explains the map\'s symbology. The north arrow and scale bar
provide geographic context.

**[Insert Legends:]{.underline}**

Note: Before inserting a legend*,* spaces and any extraneous or
unnecessary symbols or icons should be removed. You will also want to
take this opportunity to delete unnecessary elements (for example,
parcels contain a field for 'All other values", which is not
particularly useful in a legend. Also, there are missing values in this
layer, delete them for now. Open the Symbology for the parcels layer,
and adjust (i.e., delete) both the Symbology and the text for this
category (Just right-click and remove).

For this map, the legend should include the property classes, streets,
and polling places.

*[General notes on Legends:]{.underline}*

The legends below are for a map of household median income based on
census data. Think about all the ways in which the legend on the left,
which is what you get by accepting the ArcGIS defaults, is hard to
understand. [The bottom line: **DO not create a map with a legend that
looks like the one on the left!**]{.underline}

![](media/image36.png){width="4.433333333333334in"
height="2.0181594488188974in"}

Now, let's insert the legend. Under the Insert tab, click **Legend**
![Legend](media/image37.png){width="0.16666666666666666in"
height="0.16666666666666666in"}.

On the layout, anywhere suitable on the map frame, draw a rectangle
using your mouse for your legend. To work with the properties of the
legend as a whole, right-click the **Legend** heading in the
**Contents** pane and click **Properties** (Alternatively, right-click
the selected legend on the layout). We are interested in displaying a
legend for the 'Ithaca' map frame (not Tompkins County).

Note you can select which **Map frame's** legend to show here. Try
cleaning up the legend so that only the most important information is
shown. Click the** Show Properties** and have a look at all those
options under **Show**, normally, you don't need show both layer name
and headings.

Also, under **Feature Display Options**, select ***Only show features
visible in the map extent***. This will help your legend look efficient!

Note: If you fail to clean the legend, you can convert the legend to a
graphic and manipulate the legend independently. ***You should only use
this function if the tools in legend properties window are not
sufficient. Once you convert your legend to a graphic it is no longer
connected to the data, which means the legend will no longer reflect
changes you make on your map, e.g., it will not add new layers or
reflect changes in colors.***

*The steps are as follows:*

*1. Right Click* on the legend and choose **Convert to Graphics.**

*2. Right Click* on the legend and choose **Ungroup.** You now can move
and edit all of the elements of the legend independently.

3\. When you are done with your edits, click the mouse and drag a
rectangle over all of the elements of your legend to highlight all of
them. Right click and choose **Group.**

***[Insert Scale Bars:]{.underline}***

*A word on scale bars:*

![](media/image38.emf){width="4.789583333333334in"
height="1.8173556430446194in"}

-   The first scale bar above is what ArcGIS gave as the default after
    we inserted a scale and did nothing else. It shows quite arbitrary
    numbers, e.g., 2,350 and 4,700, which are not acceptable.

-   The second scale bar reflects the fact that we specified that the
    distance units be in miles, because for distances over a mile, it is
    easier to understand miles than feet (same with meters and
    kilometers). But again, the numbers are quite arbitrary.

-   The last scale bar is in miles, and it is easy to read and to use as
    a measure on the map because it uses **whole numbers** **and has
    easily understandable divisions (0.25, 0.5, 0.75).** This was done
    easily by simply stretching out the scale bar manually until it said
    2 miles (alternatively we could have compressed it to 1 mile)

The bottom line is -- **NEVER** simply accept the default if it is not
easy to read and to use! Take control over your scale bar!

*Now insert a scale bar: There are many options. Feel free to find one
that works for you.*

*Place the scale bar, notice that the default may not be the most
intuitive!*![](media/image39.png){width="2.8701279527559054in"
height="1.159090113735783in"}

We can grab the end and extend the scale bar so that it includes more
obvious break points.

![](media/image40.png){width="2.953584864391951in"
height="0.9430118110236221in"}

![](media/image41.png){width="1.85in" height="3.470138888888889in"}Still
a bit cluttered for my taste (0.13 miles is not an intuitive distance!)
In the format scale bar pane, **reduce the number of divisions from 2 to
1**. Also note that we can adjust the map units as well as the map frame
(Tompkins County is merely the context, so no need to create a scale
bar). The downtown Ithaca map frame is important one here.

For the downtown Ithaca map, feet may be appropriate. For the Tompkins
County data frame, miles may be appropriate.

> Much better in my opinion!
>
> ![](media/image42.png){width="2.763005249343832in"
> height="0.805158573928259in"}

## *[Insert text]{.underline}*

Next, you\'ll add a map title and some descriptive text. On the
**Insert** tab, in the **Graphics and Text** group, click the
**Rectangle text** tool ![Rectangle
text](media/image43.png){width="0.16666666666666666in"
height="0.16666666666666666in"}. On the layout, above the map frame,
draw a rectangle for your map title.

When you release the mouse button, the word **Text** appears inside an
outline of the box. The text is highlighted so you can start to edit it.

On the ribbon, under **Text** tab, Adjust the font, style and size
appropriately. Alternatively, double click the text you just created;
the text properties panel appears. Click Text Symbol and edit the text
format.

![](media/image44.png){width="3.4514676290463693in"
height="0.998928258967629in"}

*Change Text Format under Ribbon*

![](media/image45.png){width="2.1498261154855642in"
height="2.8636996937882766in"}

*Editing Text Format Under text symbol/properties*

Add an appropriate title (short, concise, direct) and sub-title (if
necessary). When you\'re finished, click an empty area on the layout.
The text element is now selected on the layout.

It also typical to include a text box with name, date, data source and
projection information, as well as other pertinent information. For now,
the name and date are fine.

***[Insert a north arrow]{.underline}*** (personally I prefer one with
clean, modern lines, but that's just me!), size and place on layout
accordingly.

## *[Export the layout]{.underline}*

Now that your layout is finished, you can print it or export it to a
file that can be easily shared. On the ribbon, click the **Share** tab.
In the **Output** group, click **Export Layout** ![Export
Layout](media/image46.png){width="0.16666666666666666in"
height="0.16666666666666666in"}.

The **Export Layout** pane appears. On the **Properties** tab, change
**File Type** to PNG, JPEG or TIFF necessary.

In the **Name** box type Lab 1 or something similar. Click **Browse**
![Browse](media/image47.png){width="0.16666666666666666in"
height="0.16666666666666666in"} and browse to the location where you
want to save the file.

At the bottom of the pane, click **Export**.

When the export is completed, click **View exported file** at the bottom
of the pane. The file opens in your default image viewing application.
If you want to print the layout, on the **Share** tab, click **Print
Layout** ![Print
Layout](media/image48.png){width="0.16666666666666666in"
height="0.16666666666666666in"}. You may need to change some printer
settings, such as the page orientation, before you send the layout to
the printer.

**LAB 1 DELIVERABLES**

**Deliverables** *(should be submitted as a single word document saved
as **last name_lab 1** to the Assignments link on Canvas. From now on,
**all labs** should be submitted in a similar fashion). 40 points
total.*

**MAP 1:** *A cleaned up, well organized map depicting parcels
classified according to property class, polling places and streets for
downtown Ithaca, plus a context map depicting municipalities for
Tompkins County (i.e., the map we just produced). Be sure to include*

-   *north arrow,*

-   *scale bar,*

-   *title, and*

-   *text box with name, date, and data sources.*

> *NOTE: You do not need to include the projection on this map since we
> have not discussed them yet.*
>
> 10 points

**Rubric**

One point each for:

1.  Clear Title on -what, -where (and -when if appropriate)

2.  Name and date,

3.  Legend must have correct elements and be well-designed (no default
    layer names etc.)

4.  north arrow and scale bar,

5.  (2 pts) correct zoom on downtown Ithaca (approximate) and correct
    zoom on context map,

6.  extent indicator and leader,

7.  overall formatting is clear and clean

8.  (2 pts) All layers are styled appropriately (roads, polling places,
    land uses)

![](media/image49.png){width="4.284844706911636in"
height="3.297104111986002in"}

(This map is missing the data source: Barclay Lab; Tompkins County is
merely the context, so no need to create a scale bar)

**MAP 2:** *Create a unique value map of all parcels in Tompkins County
categorized by School District. Include roads and change the symbology
so the state routes (NYS DOT) stand out (as we are including all of
Tompkins County, no need for a context map).* 10 points

HINT: Examine this screen shots: Format parcel fill and outline the
same.

![Graphical user interface, application, map Description automatically
generated](media/image50.png){width="6.0in"
height="3.1777777777777776in"}

First, format all roads the same.

![Graphical user interface, application, map Description automatically
generated](media/image51.png){width="6.0in"
height="3.1930555555555555in"}

Then change the formatting for NYS DOT roads.![Graphical user interface,
application, map Description automatically
generated](media/image52.png){width="6.0in"
height="3.2777777777777777in"}

MAKE SURE TO CLEAN THE LEGEND!

**MAP 3:** *Create a unique values map of downtown Ithaca buildings
categorized by building type.* *Change the symbology to highlight
buildings categorized as commercial and retail (this time include
Tompkins County context map).* 10 points

**Rubric**

One point each for:

1.  Clear Title on -what, -where (and -when if appropriate)

2.  Name and date,

3.  Legend must have correct elements and be well-designed (no default
    layer names, only show categories reflected on the map, etc.)

4.  north arrow and scale bar,

5.  (2 pts) correct zoom on downtown Ithaca (approximate) and correct
    zoom on context map,

6.  extent indicator and leader,

7.  overall formatting is clear and clean,

8.  (2 pts) All layers are styled appropriately (buildings by type,
    highlighting commercial and retail)

**MAP 4.** *A map of polling places labeled with addresses zoomed to the
City of Ithaca. Include roads and context map.* 10 points

**Rubric**

One point each for:

1.  Clear Title on -what, -where (and -when if appropriate)

2.  Name and date,

3.  Legend must have correct elements and be well-designed (no default
    layer names, only show categories reflected on the map, etc.)

4.  north arrow and scale bar,

5.  (2 pts) correct zoom on downtown Ithaca (approximate) and correct
    zoom on context map,

6.  extent indicator and leader,

7.  overall formatting is clear and clean,

8.  (2 pts) All layers are styled appropriately (polling place labels
    are legible and appropriate size, road layer included)
