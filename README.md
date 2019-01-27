# Route-Optimization
Find an optimal route of the Paris subway stations

## Problem Statement
 
 The goal of this project is to find an optimal route of the Paris subway stations following rules that can be summarized as: 
-	The route must include all intramural stations ;
-	The path might include non-intramural stations;
-	Total time may not exceed 20 hours;

This problem is similar with the **Chinese Postman Problem** (CPP)/**Route Inspection Problem**: 
A mailman needs to deliver mail to a neighborhood and wants to find the shortest route following the criteria:  
- it’s a closed circuit and 
- the mailman must go to every street at least once.

The main difference from our problem to the CPP problem is that in our case we don’t have a closed circuit (the start station doesn’t have to be the same as the end station), and instead of visiting all streets our target is to visit a certain amount of stations (not all of them).



## Algorithm
This problem is well suited to be solved with **Graph Theory**. Not as a coincidence, the CPP problems are suitable to be solved with graph theory too.
The approached chosen in this project uses a weighted graph, in order to establish priorities for the stations to be visited. 

And finally, every time the algorithm crosses an edge the weight is updated making the edge less likely to be revisited.
The algorithm has a loop to test several starting stations (represented by nodes also known as vertices) and choosing the shorter trajectory considering the total time to go through all desired stations.



