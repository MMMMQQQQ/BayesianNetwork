# Features
* Create interactive Bayesian Network models in the cloud
* Learn the structure of your network with powerful structural learning algorithms
* Learn the paramaters of your network with effective paramater learning methods
* Measure the importance of connections in your network with node and network measures
* Generate data from your network and export to your favorite app

# Overview
BayesianNetwork is a [Shiny](http://shiny.rstudio.com) web application for Bayesian Network modeling and analysis, powered by the excellent [bnlearn](http://www.bnlearn.com) and [networkD3](http://christophergandrud.github.io/networkD3/) packages. This app is a more general version of the [RiskNetwork](https://github.com/paulgovan/RiskNetwork) web app. To learn more about our project, check out this [publication](http://ascelibrary.org/doi/abs/10.1061/(ASCE)CO.1943-7862.0001136). For even more background, see this [publication](http://dx.doi.org/10.1061/(ASCE)CO.1943-7862.0001136).

# Getting Started
To run BayesianNetwork in [R](https://www.r-project.org):

```S
shiny::runGitHub('paulgovan/bayesiannetwork')
```

Or to access the app through a browser, visit [paulgovan.shinyapps.io/BayesianNetwork](https://paulgovan.shinyapps.io/Bayesiannetwork). 

# Example
## Dashboard
Launching the app brings up the *Dashboard*. The *Dashboard* is basically a landing page that gives a brief introduction to the app and includes two value boxes, one each for the number of *nodes* and *arcs* in the network. 

BayesianNetwork comes with a number of simulated and "real world" data sets. This example will use the "Sample Discrete Network", which is the default network loaded after launching the app.

![Dashboard](https://github.com/paulgovan/BayesianNetwork/blob/master/images/Dashboard.PNG?raw=true)

## Structure
Click *Structure* in the sidepanel in order to begin learning the network from the data.

The Bayesian network is automatically displayed inthe *Bayesian Network* box.

In order to learn the structure of the network for a given set of data, upload the data set in csv format using The *Network Input* box. Again, this example uses the "Sample Discrete Network", which should already be loaded. 

Select a learning algorithm from the *Structural Learning* box. A number of different stuctural learning algorithms are supported including:  
* Constraint-based algorithms
* Score-based algorithms
* Hybrid-structure algorithms
* Local discovery algorithms

To view the network score, select a score function from the The *Network Score* box. 

![Structure](https://github.com/paulgovan/BayesianNetwork/blob/master/images/Structure.PNG?raw=true)

"Sample Discrete Network" contains six discrete variables, stored as factors with either 2 or 3 levels. The structure of this simple Bayesian network can be learned using the grow-shrink algorithm, which is the selected algorithm by default.

Try different combinations of structural learning algorithms and score functions in order to see the effect (if any) on the resulting Bayesian network.

## Parameters
Select the grow-shrink algorithm once again and then click *Parameters* in the sidepanel in order to learn the parameters of the network.

The selected paramaters are automically displayed in the *Network Paramaters* box.

Select a learning algorithm from the *Parameter Learning* box. This app supports both maximum-likelihood and Bayesian estimation of the parameters. Note that Bayesian paramter learning is currently only implemented for *discrete* data sets. 

Then select a type of paramater chart in the *Paramter Infographic* box and, for the discrete case, choose a node. 

![Parameters](https://github.com/paulgovan/BayesianNetwork/blob/master/images/Parameters.PNG?raw=true)

For example, the selected node *A* is a discrete node with three levels *a*, *b*, and *c*.

## Measures
Click *Measures* in the sidepanel to bring up a number of tools for classical network analysis. 

The *Measures* tab has a number of both node and network measures. The node measures include:
* Markov blanket
* Neighborhood
* Parents
* Children
* In degree
* Out degree
* Incident arcs
* Incoming arcs
* Outgoing arcs

Select a node measure in the *Node Control* box and the result will be automatically displayed in the *Node Measure* box.

The so-called network measures are basically different options for hierarchical clustering of the network. Select the type of dendogram to display (row, column, both, or none) in the *Network Control* box and the resulting adjacency matrix will be displayed in the *Network Measure* box.

![Measures](https://github.com/paulgovan/BayesianNetwork/blob/master/images/Measures.PNG?raw=true)

## Simulation

Finally, click *Simulation* in the sidepanel in order to simulate data from the network.

Simply enter the sample size N in the *Network Simulation* box and click *Download* in order to download a random sample of data from the Bayesian network. 

![Simulation](https://github.com/paulgovan/BayesianNetwork/blob/master/images/Simulation.PNG?raw=true)

# Source Code
BayesianNetwork is an [open source](http://opensource.org) project, and the source code is available at [https://github.com/paulgovan/BayesianNetwork](https://github.com/paulgovan/BayesianNetwork)

# Issues
For issues or requests, please use the GitHub issue tracker at [https://github.com/paulgovan/BayesianNetwork/issues](https://github.com/paulgovan/BayesianNetwork/issues)

# Contributions
Contributions are welcome by sending a [pull request](https://github.com/paulgovan/BayesianNetwork/pulls)

# License
BayesianNetwork is licensed under the [Apache](http://www.apache.org/licenses/LICENSE-2.0) licence. &copy; Paul Govan (2015)
