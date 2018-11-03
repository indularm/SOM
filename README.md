Self organising maps or kohonen networks provide a way of representing multi-dimentional data in much lower dimentional space, usually 1 or 2 dimentions. It's also a data compression technique known as vector quantisation. In addition the SOM can be used as a method of storing information in such a way that any topological relationships within the training data set is manitained. (Topology deals with the spatial and structural properties of geometric data). Hence it's in a way advantageous compared to K-means, because it can preserve and display a clear visualization of the data. Therefore it can be used to get an idea of how many clusters the dataset can be sub divided into.

A SOM is made of neurons located on a regular, usually 1 to 2 dimentional grid. (Higher dimentional grids are possible, but they are not generally used since their visualization is much more difficult). The neurons are connected to adjacent neurons by a neighbourhood relation dictating the structure of the map. In 2 dimentional case the structure can be rectangualr or hexagonal. The sides of the map can also be connected, in that case the shape becomes a cylinder or a toroid. 

<img src="grids.gif" alt="blobs" class="inline"/>

<img src="shapes.gif" alt="blobs" class="inline"/>

Let's understand how the algorithm works, 




There are several graphical outputs that can be created to understand the nature of the dataset. The U-Matrix shows the distances between the neighbouring map units. It reveals the dissimilarities that separate the dataset into clusters. 



A component plane shows the values in each map unit for one variable. This allows us to know which features has affected the most for the classification and this can be used to get a final picture of the best classification.

Here we can see that the feature ‘Number of buyers standard deviation of holidays’ has affected the most for a clear classification. 
 

The hit map can be used to see how the data points are distributed on the map.



The dark coloured neurons are the best matching units for the datasets. 

Then hence there are 5 cut qualities in the data set we applied the K- means algorithm on the trained SOM and following classification could be seen, which can be concluded that it’s in close resemblance with the component plane with the ‘table’ feature.

(Here we have used the SOMPY library created by Vahid Moosavi.)

