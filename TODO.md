# TODO

## Rough Outline

1. Build skeleton graph - For each fip and each week, create a node in a NetworkX graph. Add the fip, shape data, and week number as a node attribute for each node.
2. Make a copy of this graph and generate the admissible set of edges. Use the geopandas method to get neighbors, and for each week, for each fip, add an edge between it and its neighbor in the next week.
3. Make a copy of the graph with no nodes for building the Bayesian network. Then pop edges from the the admissible edge graph from (2), add it to the bayesian network, and see if BIC increased like you did last semester.
    - Since the covid case count is (kind of) an unbounded discrete random variable (and not just 0/1), computing the CPD may need to be different. We can talk more about this once you get to that step. The code from last semester will (probably) work, but one natural modification is to learn a poisson RV parameter, then compute the CPD from the respective poisson distribution. We can talk more about this if your original code doesn't work well.
    - To speed up the optimization, you could also test adding an edge between two FIPs for every week at once, rather than testing one edge for one week at each step.
    - Since this step might take a while to run, you should test your code out on only a few weeks or a small region from the US
4. Once you have a Bayesian Network, you can plot it on a Folium map by turning the edges into polylines. You'll need to specify a week to plot, and the edges will be from a FIP to a correlated neighbor from the next week. The weight parameter you give the polyline can come from the mutual information score you were computing from last semester.
5. After we've got this working, we can decide whether to look at better visualization or adding more admissible edges to the model (e.g. connecting airports).

### Useful Links

- http://www.acgeospatial.co.uk/geopandas-shapefiles-jupyter/ - plotting geopandas dataframe
- https://python-visualization.github.io/folium/latest/index.html - Folium docs
- https://python-visualization.github.io/folium/latest/user_guide/vector_layers/polyline.html - draw lines on Folium maps
- https://github.com/python-visualization/folium/issues/829  - question about how draw a network on a map.
- https://gis.stackexchange.com/questions/302699/extracting-longitude-and-latitude-from-shapefile - extracting lat/long from shape file. I'm not sure if this is exactly what you need, but something like this. There'll be some geopandas method to obtain the lat/long from the centroid of each shape (i.e. the center of each fip).

## Checklist
