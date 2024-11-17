---


---

<p><strong>Author(s): Rafael Barros and Bhagyasha Patil</strong><br>
<strong>Date: November 5th 2024</strong></p>
<h1 id="welcome">Welcome</h1>
<h2 id="rdf-and-property-graphs-interoperability-status-and-issues">RDF and Property Graphs Interoperability: Status and Issues</h2>
<h3 id="authors-renzo-angles-harsh-thakkar-dominik-tomaszuk"><em><strong>Authors:</strong></em> Renzo Angles, Harsh Thakkar, Dominik Tomaszuk</h3>
<h3 id="affiliations-universidad-de-talca-university-of-bonn-university-of-bialystok"><em><strong>Affiliations:</strong></em> Universidad de Talca, University of Bonn, University of Bialystok</h3>
<hr>
<h1 id="introduction">Introduction:</h1>
<p><strong>RDF and Property Graphs:</strong> ​</p>
<ul>
<li>Both are graph-oriented database models. ​</li>
<li>RDF uses triples (subject, predicate, object). ​</li>
<li>Property Graphs use nodes and edges with properties.</li>
</ul>
<p><strong>Objective:</strong></p>
<ul>
<li>Study interoperability between RDF and Property Graph databases.</li>
</ul>
<hr>
<h1 id="types-of-interoperability-​">Types of Interoperability ​</h1>
<ul>
<li>
<p><strong>Syntactic Interoperability:</strong></p>
<ul>
<li>Data exchange at the level of serialization formats. ​</li>
</ul>
</li>
<li>
<p><strong>Semantic Interoperability:</strong></p>
<ul>
<li>Common understanding of data meanings.​</li>
</ul>
</li>
<li>
<p><strong>Query Interoperability:</strong></p>
<ul>
<li>Transforming queries between different query languages.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="rdf-databases">RDF Databases</h1>
<ul>
<li><strong>Data Model:</strong>
<ul>
<li>RDF triples (subject, predicate, object). ​</li>
<li>Visualized as graphs. ​</li>
</ul>
</li>
<li><strong>Schema:</strong>
<ul>
<li>RDF Schema, OWL, SHACL, ShEx. ​</li>
</ul>
</li>
<li><strong>Query Language:</strong>
<ul>
<li>SPARQL.</li>
</ul>
</li>
</ul>
<hr>
<p><img src="https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195306/RDF-data-Turtle-syntax-1024x581.png" alt="RDF Data - tuples format"></p>
<ul>
<li>You can see that the triples are identified by a URI, which is the <strong>subject</strong>. The <strong>predicate</strong> is the name and the <strong>object</strong> will be <em>Sketches of Spain</em>, which together is a sequence of triples.</li>
</ul>
<hr>
<h3 id="lets-look-at-how-this-information-is-displayed-graphically">Let’s look at how this information is displayed graphically:</h3>
<p><img src="https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195358/RDF-graph-example-graphconnect-1024x537.png" alt="RDF Graph"></p>
<hr>
<h1 id="property-graph-databases">Property Graph Databases</h1>
<ul>
<li><strong>Data Model:</strong>
<ul>
<li>Directed labeled multi-graph with properties. ​</li>
</ul>
</li>
<li><strong>Schema:</strong>
<ul>
<li>Node types, edge types, integrity constraints. ​</li>
</ul>
</li>
<li><strong>Query Languages:</strong>
<ul>
<li>No standard; examples include Cypher, PGQL, G-CORE.</li>
</ul>
</li>
</ul>
<hr>
<p><img src="https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195506/LPG-data-cypher-1024x519.png" alt="Cypher example"></p>
<ul>
<li>The <strong>semantics</strong> are the same. There’s no standard serialization format or a way of expressing a labeled property graph, but rather a sequence of <code>CREATE</code> statements do the job here.</li>
</ul>
<hr>
<h3 id="lets-look-at-how-this-information-is-displayed-graphically-1">Let’s look at how this information is displayed graphically:</h3>
<p><img src="https://s3.amazonaws.com/dev.assets.neo4j.com/wp-content/uploads/20170617195625/LPG-Graph-Example-graphconnect-1024x533.png" alt=""></p>
<ul>
<li><strong>Core Difference:</strong> nodes have this internal structure and values of attributes don’t represent vertices in the graph.</li>
</ul>
<hr>
<h1 id="syntactic-interoperability">Syntactic Interoperability</h1>
<ul>
<li><strong>Challenges:</strong>
<ul>
<li>No standard data format for Property Graphs. ​</li>
<li>Different serialization formats (e.g., Turtle, RDF/XML for RDF). ​</li>
</ul>
</li>
<li><strong>Approaches:</strong>
<ul>
<li>Textual mappings, intermediate data formats.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="semantic-interoperability">Semantic Interoperability</h1>
<ul>
<li><strong>Challenges:</strong>
<ul>
<li>Special RDF features (e.g., blank nodes, reification). ​</li>
<li>Partial schemas in RDF. ​</li>
</ul>
</li>
<li><strong>Approaches:</strong>
<ul>
<li>Data and schema transformation methods. ​</li>
<li>Use of transformation languages (e.g., XSPARQL, RML).</li>
</ul>
</li>
</ul>
<hr>
<h1 id="query-interoperability-​">Query Interoperability ​</h1>
<ul>
<li><strong>Challenges:</strong>
<ul>
<li>Lack of a standard query language for Property Graphs. ​</li>
<li>Different paradigms (declarative vs. imperative). ​</li>
</ul>
</li>
<li><strong>Approaches:</strong>
<ul>
<li>Tools like Gremlinator for SPARQL to Gremlin translation. ​</li>
<li>Efforts to standardize Property Graph query languages.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="issues-and-challenges">Issues and Challenges</h1>
<ul>
<li><strong>Syntactic Interoperability:</strong>
<ul>
<li>No standard data format for Property Graphs. ​</li>
<li>Differences in serialization formats. ​</li>
</ul>
</li>
<li><strong>Semantic Interoperability:</strong>
<ul>
<li>RDF features not easily modeled in Property Graphs. ​</li>
<li>Need for schema discovery and transformation. ​</li>
</ul>
</li>
<li><strong>Query Interoperability:</strong>
<ul>
<li>No standard query language for Property Graphs. ​</li>
<li>Different query paradigms and semantics.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="conclusions">Conclusions</h1>
<ul>
<li><strong>Importance of Interoperability:</strong> ​
<ul>
<li>Facilitates data exchange, integration, and reuse. ​</li>
</ul>
</li>
<li><strong>Future Directions:</strong>
<ul>
<li>Standardization of Property Graph data model and query language. ​</li>
<li>Development of robust transformation methods.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="acknowledgments-​">Acknowledgments ​</h1>
<ul>
<li><strong>Funding:</strong>
<ul>
<li>Millennium Institute for Foundational Research on Data. ​</li>
<li>EU H2020 R&amp;I project BOOST4.0. ​</li>
<li>National Science Center, Poland.</li>
</ul>
</li>
</ul>
<hr>
<h1 id="references">References:</h1>
<ul>
<li><strong>About 48 written in the Article</strong></li>
</ul>
<hr>
<h1 id="thank-you">Thank you</h1>
<ul>
<li><strong>Questions?</strong></li>
</ul>

