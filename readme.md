<img src="https://github.com/Antonio-Cruciani/dynamic-random-graph-generator/blob/master/img/Dynamic.png?v=3&s=200" title="Dynamic Random Graph" alt="DynamicRG" height=256 width=386>


# Dynamic Random Graph Generator

 This is a function package for people interested in studying graphs that evolve over time. Anyone with a basic understanding of Python can create their own dynamic graph.






## Table of Contents 



- [Installation](#installation)
- [Description](#description)
- [RAES Random Graph](#RAES)
- [Edge Dynamic Random Graph](#EdgeDynamic)
- [Vertex Dynamic Random Graph](#VertexDynamic)
- [Papers ](#Papers)
- [License](#license)







## RAES
Dynamic Random Graph G(n,d,c) where:

-	 **n** is the number of vertices 
-  **d** is the minimum required degree in the graph
-  **c** is the tolerance (c*d = Max Degree in the graph)


RAES evolves over time with the following rules:

<img src="https://github.com/Antonio-Cruciani/dynamic-random-graph-generator/blob/master/img/RAES.png?v=3&s=200" title="RAES" alt="RAESRG" height=356 width=786>

```python 
# Initializing parameters
n = 30
d = 3 
c = 1.5 
p = 0
lamb = 1
beta = 0.01
G = DynamicGraph(n,d,c,lamb,beta,p,"Multiple")
# is regular return False if all vertices has d <= degree <= c*d, else return True
while(G.isregular()):
    # Phase 1
    G.add_phase()
    # Phase 2
    G.del_phase()  
```
Demo of the example,
       
- **blue nodes** : d <= degree <= c*d  
- **red nodes** :  degree < d or degree > c*d 
 
<img src="https://github.com/Antonio-Cruciani/dynamic-random-graph-generator/blob/master/img/RAES.gif?v=3&s=200" title="RAES" alt="RAESRG" height=256 width=486>
