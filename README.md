# wikipedia_network
Visualize your interests on contents and relation among contents staff by scraping wikipedia to gather info.
The python class which get staff information from wikipeia on TV, radio and Movie. Use networkx to visualize 
## warning
- tested on jp only.　　　　
- tested on very limited sample
- assumption: wikipedia has correct information. 

## files
- wikiparse_netwokrx.ipynb : include wikipedia scraping script and visualize with networkx
- wikiscraper_class_prototype.ipynb : trial and error for wikipedia scraping
- contents.csv : data input for wikipedia scraping

## Usage
1. create contents.csv file with contents you want to check relations
    - contents have タイトル,ポイント,id(optional) columns.
2. execute wikiparse_networkx.ipynb
    - Nodes have point attribute and that is sum of all points contents related to node
    - Nodes from input file(contents) have genre attribute.
    - Nodes will be removed from lower point nodes to make number of nodes less than 500 since too many nodes are difficult to see.
3. use gexf file viewer, e.g. Gephi to see network.
