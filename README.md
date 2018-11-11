Self organising maps or kohonen networks provide a way of representing multi-dimentional data in much lower dimentional space, usually 1 or 2 dimentions. It's also a data compression technique known as vector quantisation. In addition the SOM can be used as a method of storing information in such a way that any topological relationships within the training data set is manitained. (Topology deals with the spatial and structural properties of geometric data). Hence it's in a way advantageous compared to K-means, because it can preserve and display a clear visualization of the data. Therefore it can be used to get an idea of how many clusters the dataset can be sub divided into.

A SOM is made of neurons located on a regular, usually 1 to 2 dimentional grid. (Higher dimentional grids are possible, but they are not generally used since their visualization is much more difficult). The neurons are connected to adjacent neurons by a neighbourhood relation dictating the structure of the map. In 2 dimentional case the structure can be rectangualr or hexagonal. The sides of the map can also be connected, in that case the shape becomes a cylinder or a toroid. 

<img src="grids.gif" alt="blobs" class="inline"/>

<img src="shapes.gif" alt="blobs" class="inline"/>

Let's understand how the map works, 

Each unit is associated with weight vector (or codebook vector) W<sub>i</sub>  which is of the same dimention as the input data. 

<img src="Figure_10.png" alt="blobs" class="inline"/>

The codebook vectors W<sub>i</sub> must be initiated with values similar to those of the input data. During the training of the map the input vectors are presented to the map consecutively. The unit with a codebook vector W<sub>i</sub> that sohows the smallest distance to the input vector x is declared as the best matching unit(BMU). You can view the best matching units with the hits map. This process is known as so called vector quantization.
The codebook vectors are unpdated via following equation, 


(Here we have used the SOMPY library created by Vahid Moosavi.)

