# ggnet: simple network plots with ggplot2

A while ago, Moritz Marbach coded the `plotg()` function to [visualize networks with ggplot2 in R][mm]. 

Here's a slightly modified version that takes the following arguments:

		ggnet(net,               # an object of class network
		      value = 12,        # base node size
		      weight = "sum",    # weight nodes by "indegree", "outdegree" or sum
		      quartiles = FALSE, # break weights to quartiles
		      classes = NULL,    # what to color the nodes with
		      name = "",         # what to call the node color legend
		      scheme = NULL,     # color classes for the nodes
		      labels = FALSE,    # add vertex names in small print
		      legend.position = "right", # cosmetics
					arrow.size = 0.25)         # cosmetics

[mm]: http://sumtxt.wordpress.com/2011/07/02/visualizing-networks-with-ggplot2-in-r/

The function is not (yet) robust to omitting much of the options above, but as long as you have an object of class `network` with something to color the nodes, you should be fine.

If you need to convert an object of class `igraph` or whatever else you use, have a look at the [`intergraph` package][ig].

[ig]: http://intergraph.r-forge.r-project.org/

Comments welcome!

# Example

![French MPs on Twitter](example.png)

A plot of Twitter connexions between 339 French MPs currently in office, colored by parliamentary groups. Data assembled by scraping a few web sources with the help of [Jonathan Chibois][jc] and Benjamin Ooghe-Tabanou from [Regards Citoyens][rc]. Inspired by [Baptiste Coulmont][bc].

[bc]: http://coulmont.com/index.php?s=d%C3%A9put%C3%A9s
[jc]: http://laspic.hypotheses.org/
[rc]: http://www.regardscitoyens.org/
