Self organising maps or kohonen networks provide a way of representing multi-dimentional data in much lower dimentional space, usually 1 or 2 dimentions. It's also a data compression technique known as vector quantisation. In addition the SOM can be used as a method of storing information in such a way that any topological relationships within the training data set is manitained. (Topology deals with the spatial and structural properties of geometric data). Hence it's in a way advantageous compared to K-means, because it can preserve and display a clear visualization of the data. Therefore it can be used to get an idea of how many clusters the dataset can be sub divided into.

A SOM is made of neurons located on a regular, usually 1 to 2 dimentional grid. (Higher dimentional grids are possible, but they are not generally used since their visualization is much more difficult). The neurons are connected to adjacent neurons by a neighbourhood relation dictating the structure of the map. In 2 dimentional case the structure can be rectangualr or hexagonal. The sides of the map can also be connected, in that case the shape becomes a cylinder or a toroid. 

<img src="grids.gif" alt="blobs" class="inline"/>

<img src="shapes.gif" alt="blobs" class="inline"/>

Let's understand how the map works, 

Each unit is associated with weight vector (or codebook vector) W<sub>i</sub>  which is of the same dimention as the input data. 

<img src="Figure_10.png" alt="blobs" class="inline"/>

The codebook vectors W<sub>i</sub> must be initiated with values similar to those of the input data. During the training of the map the input vectors are presented to the map consecutively. The unit with a codebook vector W<sub>i</sub> that sohows the smallest distance to the input vector X is declared as the best matching unit(BMU). You can view the best matching units with the hits map. This process is known as so called vector quantization.
The codebook vectors are unpdated via following equation, 

**W<sub>i</sub><sup>t+1</sup> = W<sub>i</sub><sup>t</sup> + h<sub>ci</sub><sup>t</sup>x A<sup>t</sup> x d(X,W<sub>i</sub><sup>t</sup>)**

here c means the codebook vector

Where t is a point in time. 
h<sub>ci</sub><sup>t</sup> is a neighbourhood function
A<sup>t</sup> is a learning rate

d(X,W<sub>i</sub><sup>t</sup>) is the distance between an input vector X and the codebook vector W<sub>i</sub>

Both A<sup>t</sup> and h<sub>ci</sub><sup>t</sup> lie within the interval [0,1] and discrete by time.  The neighbouring function h<sub>ci</sub><sup>t</sup> is defined by the topological or geometrical relationship between W<sub>i</sub><sup>t</sup> and the codebook vector W<sub>c</sub><sup>t</sup> of the BMU. 
After n training cycles the values of the codebook vectors W<sup>n</sup> will represent the distribution of the input vectors. 

To have a idea of the data set being analyzed we need to visualize the codebook vectors. There are several ways we can do that, and each way of visualizing gives different view of the dataset. 

**Visualization of the COdebook Vectors**

The codebook vectors tend to be closer to each other in the areas where they represent input vecotrs which are distributed tensly and vice versa the distance between the codebook vectors are large in areas where there is a sparse distribution of input vectors. 

*Component Planes* 
  This shows the relative values of the components of the codebook vectors. Therefore the number of component palnes per SOM is eqaul to the number of input vector's dimentionality. Component planes can be thought of as a sliced version of the SOM. Each component plane has the relative distribution of one data vector component. 
  In this representation, dark values represent relatively small values while white values represent relatively large values. By compairing component planes we can have an idea of the correlation between the input vector components. If the outlook pattern and colors are similar, the components strongly correlate. 
  
*U - Matrix*
  This figure shows the relative distances between the neurons in the map. Here the distance between the adjacent neurons is calculated and presented with different colorings between the adjacent nodes. 
  The light colouring between the neurons corresponds to a large distance and thus gap between the codebook values in the input space and the dark colors indicates that the codebook vecotrs are closer to each other. Therefore dark areas can be though of as clusters and light coloured areas as cluster seperators. This representation is helpful when one tries to find the clusters in the input data without having any priori information about the clusters. 


(Here we have used the SOMPY library created by Vahid Moosavi.)

