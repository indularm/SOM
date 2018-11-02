Self-organizing map(SOM) is a clustering technique which can be used to view topological nature of the dataset in a graphical view by reducing the higher dimensions to lower dimensions. It’s more advantageous than K-means algorithm in the sense that SOM can preserve the topology of the original dataset. It can be used to get an idea of how many clusters the dataset can be sub divided into.

A SOM is made of neurons located on a regular, usually 1 to 2 dimentional grid. (Higher dimentional grids are possible, but they are not generally used since their visualization is much more difficult). The neurons are connected to adjacent neurons by a neighbourhood relation dictating the structure of the map. In 2 dimentional case the structure can be rectangualr or hexagonal. The sides of the map can also be connected, in that case the shape becomes a cylinder or toroid. 










There are several graphical outputs that can be created to understand the nature of the dataset. The U-Matrix shows the distances between the neighbouring map units. It reveals the dissimilarities that separate the dataset into clusters. 



A component plane shows the values in each map unit for one variable. This allows us to know which features has affected the most for the classification and this can be used to get a final picture of the best classification.

Here we can see that the feature ‘Number of buyers standard deviation of holidays’ has affected the most for a clear classification. 
 

The hit map can be used to see how the data points are distributed on the map.



The dark coloured neurons are the best matching units for the datasets. 

Then hence there are 5 cut qualities in the data set we applied the K- means algorithm on the trained SOM and following classification could be seen, which can be concluded that it’s in close resemblance with the component plane with the ‘table’ feature.

(Here we have used the SOMPY library created by Vahid Moosavi.)




### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/indularm/SOM/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
