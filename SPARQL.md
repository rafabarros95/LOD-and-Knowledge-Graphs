---


---

<p><strong>RAFAEL RODRIGUES BARROS<br>
October 2024</strong></p>
<h1 id="sparql---introduction-origins-challenges-and-applications">SPARQL - Introduction: Origins, Challenges and Applications</h1>
<h2 id="covering-points-of-this-presentation">Covering points of this presentation:</h2>
<ul>
<li>Origin: Contex and limitations of Traditional Relational Databases;</li>
<li>Early Challenges with RDF Data;</li>
<li>Sparql:  Overview, Purpose and Basic Syntax;</li>
<li>Its Application in LOD;</li>
<li>Examples ( Isaac Newton data from Wikipedia );</li>
<li>Limitations and Future Analysis for Improvements in Knowledge Graphs;</li>
<li>References;</li>
</ul>
<h2 id="contextual-analysis-sparql---deep-diving-into-the-query-of-semantic-web">Contextual Analysis: SPARQL - deep diving into the query of semantic web</h2>
<ul>
<li><strong>Data Access</strong> and <strong>Query Language</strong>  in order to handle large, complex and interconnected datasets**;</li>
<li><strong>Semantic Web Principle</strong>: data should be able to get accessed across platforms and universally understood;</li>
<li><strong>Data Silos and its Interoperability</strong>: database tables with rows and columns makes difficult to understand and link the relationships between different datasets;</li>
<li><strong>Relational Databases</strong>: rely on restructure while adding new data type when the pre-structured or predefined schema is modified;</li>
<li><strong>SQL Queries Limitations</strong>: as the data are more interconnected, the traditional SQL queries struggle with optimized ways of querying and retrieving complex interlinked data and its relationships;</li>
<li><strong>Limitation of Data Interpretation</strong>: the ability to reason and understand the meaning behind data by previously data systems was missing;</li>
<li><strong>Sharing Data on Internet</strong>: the ability to reason and understand the meaning behind data by previously data systems was missing;</li>
</ul>
<p><img src="https://cdn.analyticsvidhya.com/wp-content/uploads/2024/02/Relational-Database-vs-Graph-Database-1-1-scaled.jpg" alt="SPARQL Overview comparison"><br>
<img src="https://cdn.analyticsvidhya.com/wp-content/uploads/2024/02/image-77-2048x1426.png" alt="Graph Dataset Connection Example"></p>
<h2 id="what-is-sparql-overview">What is SPARQL? Overview:</h2>
<ul>
<li><strong>SPARQL</strong> is the standard query language for RDF data, enabling users to query, retrieve, and manipulate data in RDF format.</li>
<li>Developed by the <strong>W3C</strong> (World Wide Web Consortium), SPARQL is designed to interact with data on the Semantic Web.</li>
</ul>
<h3 id="purpose">Purpose:</h3>
<p>SPARQL, which stands for <strong>SPARQL Protocol and RDF Query Language</strong>, is a powerful query language standardized by W3C and supposed to query and manipulate data stored in <strong>RDF</strong> (Resource Description Framework) format. It is widely used to interact with linked open data and knowledge graphs, especially in Semantic Web Context.</p>
<h3 id="sparql-types">SPARQL Types:</h3>
<ol>
<li><strong>ASK</strong>: check if at least one match exists and return boolean ( TRUE or FALSE );</li>
<li><strong>CONSTRUCT</strong>: Create new RDF triples from matches;</li>
<li><strong>DESCRIBE</strong>: Create RDF triples about a resource;</li>
<li><strong>SELECT(Most used)</strong>: Return matches as a collection of solution bindings;</li>
</ol>
<p><img src="https://image.slidesharecdn.com/sparql-cheat-sheet-090616011306-phpapp01/85/SPARQL-Cheat-Sheet-6-320.jpg" alt="4 types of SPARQL"></p>
<h2 id="application-in-lod">Application in LOD</h2>
<ul>
<li><em><strong>Linked Open Data</strong></em> is a network of interlinked datasets from different sources acessible through RDF and SPARQL;</li>
<li><em><strong>SPARQL</strong></em> viable users to query datasets such as DBpedia, Wikidata etc… That’s the limitation of formers Relational Datasets Retriever;</li>
</ul>
<p><img src="https://www.researchgate.net/publication/321328847/figure/fig1/AS:565603641823232@1511861824288/Linked-Open-Data-Cloud-and-Data-publishers.png" alt="LOD Cloud Example"></p>
<h3 id="syntax">Syntax:</h3>
<p>Similar to SQL, SPARQL queries involve selecting specific data from structured triples (subject, predicate, object).</p>
<h3 id="example-of-rdf-triples">Example of RDF Triples</h3>

<table>
<thead>
<tr>
<th>Subject</th>
<th>Predicate</th>
<th>Object</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>&lt;John&gt;</code></td>
<td><code>&lt;likes&gt;</code></td>
<td><code>&lt;Pizza&gt;</code></td>
</tr>
<tr>
<td><code>&lt;City:Paris&gt;</code></td>
<td><code>&lt;isInCountry&gt;</code></td>
<td><code>&lt;Country:France&gt;</code></td>
</tr>
</tbody>
</table><hr>
<p><img src="https://th.bing.com/th/id/R.099b57f2ca635de32f62125d665cc0f8?rik=Y1Du%2fEgBkOw31A&amp;riu=http%3a%2f%2flim.univ-reunion.fr%2fstaff%2ffred%2fEnseignement%2fSW%2fSPARQL-by-example%2fspo-arrow.png&amp;ehk=t%2bd7wD6Wie0rfSDW%2f3TdT93%2fWU4xAro52EYV%2b6mgQtQ%3d&amp;risl=&amp;pid=ImgRaw&amp;r=0" alt=""></p>
<p><em><strong>Code -  Triple pattern query:</strong></em></p>
<p><img src="https://www.researchgate.net/publication/375618644/figure/fig3/AS:11431281204802839@1699967742547/a-Example-of-SPARQL-triple-pattern-query-b-After-translation-of-the-predicate-and.png" alt=""></p>
<h2 id="basic-sparql-query-structure">Basic SPARQL Query Structure</h2>
<p>A basic SPARQL query contains the following components:</p>
<ol>
<li><strong>SELECT</strong> - Specifies which variables to return.</li>
<li><strong>WHERE</strong> - Defines patterns to match against the RDF triples in the dataset.</li>
<li><strong>FILTER</strong> - (Optional) Adds conditions to limit the results based on certain criteria.</li>
<li><strong>LIMIT</strong> - That defines how many researched data should be retrieved.</li>
</ol>
<h2 id="sparql-wikidata--example">SPARQL (Wikidata)  Example:</h2>
<h3 id="example-sparql-query">Example SPARQL Query</h3>
<p>The following highlighted SPARQL query retrieves all people who studied at Trinity College:</p>
<p><strong>?person wdt:P69 wd:Q332342 .</strong></p>

<table>
<thead>
<tr>
<th>wdt</th>
<th>wd</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>&lt;property&gt;</code></td>
<td><code>&lt;entity&gt;</code></td>
</tr>
<tr>
<td><code>&lt;educated at&gt;</code></td>
<td><code>Trinity College</code></td>
</tr>
</tbody>
</table><pre class=" language-sparql"><code class="prism  language-sparql">SELECT ?person ?personLabel ?birth_placeLabel ?coodinates
 
WHERE{

  ?person wdt:P69 wd:Q332342 . # all those who studied at Trinity College in Ireland
  
  ?person wdt:P106 wd:Q170790 . # ordered by occupation listed
  ?person wdt:P21 wd:Q6581097 . # male who studied at Trinity College
  ?person wdt:P19 ?birth_place . # place of birth , make sure the name given is at select query on top
  ?birth_place wdt:P625 ?coodinates . # with Label after the name ensure the name of that searched identifier
  
   SERVICE wikibase:label { 
       bd:serviceParam wikibase:language "en" . }
     #service provided by examples on wikidata query service

}
</code></pre>
<h3 id="sources-used">Sources used:</h3>
<p>Source_1: <a href="https://link.springer.com/chapter/10.1007/978-3-642-12814-1_4">Using SPARQL and SPIN for Data Quality Management on the Semantic Web | SpringerLink</a></p>
<p>Source_2: <a href="https://dl.acm.org/doi/10.1145/3397512">A review of the semantic web field | Communications of the ACM</a></p>
<p>Source_3: <a href="https://dev.to/edent/sparql-an-absolute-beginner-s-guide-2c65#:~:text=Assign%20to%20the%20variable%2C%20data%20where%20the%20property,entity%2C%20and%20Q84%20is%20the%20ID%20of%20London.">SPARQL - An Absolute Beginner’s Guide - DEV Community</a></p>
<p>Source_4: <a href="https://comunica.dev/docs/query/advanced/sparql_query_types/">Comunica – SPARQL query types</a></p>

