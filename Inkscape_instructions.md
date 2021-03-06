##Instructions for creating a new Interactive Annotated Image
#####Collin Schwantes
03/21/16


Follow these instructions to create an annotated image in [inkscape](https://inkscape.org/en/) and the corresponding [jekyll site](https://jekyllrb.com/). 

1.  [Fork](https://github.com/collinschwantes/Annotated_Ultras/blob/master/Inkscape_instructions.md#fork-destination-box) this project to create a copy for your github account or 
[Download](https://github.com/collinschwantes/Annotated_Ultras/archive/master.zip) the repository and transfer the files to a folder with an appropriate name
2.  Move the image you will annotate into the **images** folder and delete the old file. 
3.  Open the **_data** folder and then open the **hao_terms.json** file
    -  you will notice that entry has 5 attributes including a unique `ID`
    ```
    {
    "title": "Antenna",
    "definition": "The appendage that is composed of ringlike sclerites and the anatomical structures encircled by these sclerites and that is articulated with the cranium.",
    "URI": "http://purl.obolibrary.org/obo/HAO_0000101",
    "Preferred.Term": "antenna",
    "ID": "HAO_0000101"
  },
    ```
    -  Leave this file open, you will use it as you annotate the SVG
4.  Start a new SVG file in Inkscape
5.  Import (`ctrl+i`) the image file from the images folder into your new svg 
    - select link 
    - resize the image to fit within the page (solid lines) 
    - alternatively, you can resize the document (`ctrl+shift+d`) to fit the image
6.  Save the document as a plain SVG and name it appropriately
7.  Start by outlining one of the larger segments (head, mesosoma, metasoma) - order is important for the click functionality 
    - Pressing `B` will bring up the bezier tool, this allows you to place points around a structure and then modify them to create curves. 
8.  After you have outlined the segment, change the fill `ctrl+shift+f` to RGBA **97cafcff** and the stroke to none
9.  Select the feature you just created (quickly switch to the selection tool by pressing `S`) and press `ctrl+shift+x` to open the XML editor. 
    - press `ctrl g` to make a new group 
    - ![xml editor](https://raw.githubusercontent.com/collinschwantes/Annotated_Ultras/master/Screenshot%202016-03-21%2013.00.40.png)
10. Click on `id` in the Name column
    - ![xml editor selected](https://raw.githubusercontent.com/collinschwantes/Annotated_Ultras/master/Screenshot%202016-03-21%2013.05.37.png)
11. Change the group id to the **HAO_terms** id
    - ![xml editor changed](https://raw.githubusercontent.com/collinschwantes/Annotated_Ultras/master/Screenshot%202016-03-21%2013.07.36.png)
    - *NOTE* use `ctrl v` to paste in inkscape
    - click `set` to change the id
12. Give the feature the `class` "bodypart" by entering "class" into the attribute name bar and "bodypart" into the attribute value box
    - ![xml editor class](https://raw.githubusercontent.com/collinschwantes/Annotated_Ultras/master/Screenshot%202016-03-21%2013.23.56.png)
    - this a good place to save
13. Repeat steps 7-12 until all visible HAO terms have been added. 
14. Open your SVG in a text editor (eg TextEdit) and delete the first line 
    - delete the line selected in this image
    - ![textedit_delete](https://raw.githubusercontent.com/collinschwantes/Annotated_Ultras/master/Screenshot%202016-03-21%2013.31.42.png)
15. Copy the remaining text and paste it into the file `svg.html` that lives in the **_includes** folder 
    - You can use TextEdit for this as well
    - If there is already text in the `svg.html` file, replace it with the new svg text
16. Upload the folder to the server. Pat yourself on the back ![done](http://i3.kym-cdn.com/photos/images/facebook/000/011/296/success_baby.jpg)
