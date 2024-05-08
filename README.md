

<h1>Minimum Spanning Tree for Computer Networks in a Growing Company</h1>

<p>This repository contains an implementation of various algorithms for finding the Minimum Spanning Tree (MST) of a graph, specifically designed for computer networks in a growing company. The algorithms implemented are Prim's Algorithm, a modified version of Prim's Algorithm (based on a research paper), and Kruskal's Algorithm.</p>

<p>The main goal of this project is to find the most efficient algorithm for constructing the MST of a computer network in a growing company, as this can help optimize the network infrastructure and reduce costs.</p>

<h2>Table of Contents</h2>

<ul>
  <li><a href="#aim">Aim</a></li>
  <li><a href="#problem-statement">Problem Statement</a></li>
  <li><a href="#method">Method</a></li>
  <li><a href="#algorithms">Algorithms</a>
    <ul>
      <li><a href="#prims-algorithm">Prim's Algorithm</a></li>
      <li><a href="#new-prims-algorithm">New Prim's Algorithm</a></li>
      <li><a href="#kruskals-algorithm">Kruskal's Algorithm</a></li>
    </ul>
  </li>
  <li><a href="#code">Code</a></li>
  <li><a href="#results">Results</a></li>
  <li><a href="#usage">Usage</a></li>
  <li><a href="#references">References</a></li>
</ul>

<h2 id="aim">Aim</h2>
<p>Implement Minimum Spanning Tree for Computer Networks in a Growing Company.</p>

<h2 id="problem-statement">Problem Statement</h2>
<p>Implement Minimum Spanning Tree for Computer Networks in a Growing Company by referencing the dataset given in the research paper and also implement it using Kruskal's algorithm. Compare the results.</p>

<h2 id="method">Method</h2>
<p>We use Prim's Algorithm, the New Prim's Algorithm (from the research paper), and Kruskal's algorithm to compare datasets which are generated randomly. The algorithms are provided, and we write code to verify their implementation.</p>

<h2 id="algorithms">Algorithms</h2>

<h3 id="prims-algorithm">Prim's Algorithm</h3>
<p>Prim's algorithm is a greedy algorithm that finds a minimum spanning tree for a weighted undirected graph. It starts with an empty spanning tree and builds the minimum spanning tree by adding edges one by one. The algorithm follows these steps:</p>
<ol>
  <li>Initialize a tree with a single vertex, chosen arbitrarily from the graph.</li>
  <li>Greedily pick the smallest weight edge that connects the tree to one of the vertices not in the tree.</li>
  <li>Add the vertex to the tree.</li>
  <li>Repeat step 2 and 3 until all vertices are in the tree.</li>
</ol>

<h3 id="new-prims-algorithm">New Prim's Algorithm</h3>
<p>This is a modified version of Prim's Algorithm, based on a research paper. The algorithm follows these steps:</p>
<ol>
  <li>Create the MST <code>T</code> of a graph using Prim's algorithm. Choose one of the edges <code>{e1, e2, ..., ek}</code>.</li>
  <li>If the edges <code>{e1, e2, ..., ek}</code> belong to <code>T</code>, then <code>T</code> is the MST. If the edges <code>{e1, e2, ..., ek}</code> don't belong to <code>T</code>, create a set <code>S</code> of edges that don't belong to <code>T</code>.</li>
  <li>Choose an edge from the set <code>S</code> and add it to <code>T</code>. In this case, a cycle occurs in <code>T</code>. Choose the longest edge outside the edges <code>{e1, e2, ..., ek}</code> in this cycle and remove the longest edge from <code>T</code>.</li>
  <li>Remove the latest edge added to <code>T</code> from the set <code>S</code>.</li>
  <li>Repeat from Step 3, until <code>S</code> is an empty set.</li>
</ol>

<h3 id="kruskals-algorithm">Kruskal's Algorithm</h3>
<p>Kruskal's algorithm is another greedy algorithm for finding the minimum spanning tree of a weighted undirected graph. It follows these steps:</p>
<ol>
  <li>Sort all the edges in non-decreasing order of their weight.</li>
  <li>Pick the smallest edge. Check if it forms a cycle with the spanning tree formed so far. If it doesn't, include this edge in the spanning tree.</li>
  <li>Repeat step 2 until there are (V-1) edges in the spanning tree.</li>
</ol>

<h2 id="code">Code</h2>
<p>The code is written in Python and uses the <code>networkx</code> library for graph operations and visualization. The following algorithms are implemented:</p>
<ol>
  <li>Prim's Algorithm</li>
  <li>New Prim's Algorithm (based on the research paper)</li>
  <li>Kruskal's Algorithm</li>
</ol>
<p>The code generates random graphs of different sizes (10, 20, 30, 40, and 50 nodes) and measures the execution time for each algorithm on these graphs. It also visualizes the generated graphs using <code>matplotlib</code>.</p>

<h2 id="results">Results</h2>
<p>The New Prim's Algorithm takes more time than Prim's and Kruskal's algorithms, but it obtains a minimum spanning tree that can be used for large datasets. This implementation provides various options for different paths in a company network.</p>

<h2 id="usage">Usage</h2>
<ol>
  <li>Clone the repository</li>
  <li>Install the required dependencies: <code>networkx</code>, <code>matplotlib</code></li>
  <li>Run the Python script</li>
  <li>The generated graphs will be displayed, and the execution times for each algorithm will be plotted.</li>
</ol>

<h2 id="references">References</h2>
<ul>
  <li>THE NEW ALGORITHM INVOLVING MINIMUM SPANNING TREE FOR COMPUTER NETWORKS IN A GROWING COMPANY∗ (Research Paper)</li>
  <li>Link to the paper: <a href="https://dergipark.org.tr/tr/download/article-file/1195132">https://dergipark.org.tr/tr/download/article-file/1195132</a></li>
</ul>
