# Cerebellum Project Data Visualisation
Create plots for cerebellar and cerebral morphology in a range of primates.
Run alongside csv file containing brain morphological data from a range of studies.
CSV will be updated in the future as the project progresses.

<ins>Functions<ins>
    
**plot_variables():**<br>
Produces plots with legend, data point colours mapped to taxon.
- Keyword Arguments:
    - xy -- str. Tuple of tuples each containing variable pairs. default=all combinations for the relevant data
    - logged -- bool. If True, produces logged plots for xy. default=False.
    - save -- bool. If True, creates either 'Saved Simple Plots' or 'Saved Log Plots' folders depending on if the 'logged' keyword argument is specified as True or False. 
        - A text file is created in each of these folders with details on what each plot file contains. 
        - This is because including variable names in file name could cause confusion/more clutter than necessary.
    - show -- bool. If True, outputs plots to a new window. 
<br><br>
- Example Input:
    ```
    plot_variables(
                (('Cerebrum Volume', 'Cerebellum Volume'),),  
                logged=True, save=True, show=True
                )  
    ```

**plot_regression():**<br>
Plots linear regression line for the volume-against-volume plot.


**delete_folder():**<br>
Deletes simple or log save folder.
- Keyword Arguments:
    - logged -- bool. If True, deletes log save folder. default=False (deletes simple save folder).<br>
    

 <br>

**<ins>ABOUT THE CEREBELLUM PROJECT<ins>**

The cerebellum project studies cerebellar evolution at microscopic scale, across several primate species. It aims at creating precise delineations of the pial surface of the cerebellar cortex. With this, we measure the surface area and volume of each cerebellum and cerebrum in each primate brain. We will also attempt to use the annotations to generate 3D volumes and 3D meshes of the gorilla cerebellum. Eventually we will use these surface data to guide segmentation into cerebellar sub-structures with more precise functions.

Primarily, for annotation, we use MicroDraw, available at: https://microdraw.pasteur.fr/

To learn how we annotate each structure, visit: https://docs.google.com/document/d/1gAQIiEM9bAYKqiLpG9vHDmuaBk-LYpSIdsVsISAPzq4/edit

![AnnotationTransparent](https://user-images.githubusercontent.com/73407206/136446208-e2651756-359a-46e8-96cd-c526958828bb.png)

See our prototype reconstruction of an eastern lowland gorilla cerebellum:

![Gorilla3DTransparent](https://user-images.githubusercontent.com/73407206/136446331-42e5afb3-2867-4329-952f-3b5593972e9c.gif)

