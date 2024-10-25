---


---

<h1 id="sparql">SPARQL</h1>
<h2 id="contextual-analysis-sparql">Contextual Analysis: SPARQL</h2>
<ul>
<li><strong>Data Access</strong> and <strong>Query Language</strong>  in order to handle large, complex and interconnected datasets**;</li>
<li><strong>Semantic Web Principle</strong>: data should be able to get accessed across platforms and universally understood;</li>
<li><strong>Data Silos and its Interoperability</strong>: database tables with rows and columns makes difficult to understand and link the relationships between different datasets;</li>
<li><strong>Relational Databases</strong>: rely on restructure while adding new data type when the pre-structured or predefined schema is modified;</li>
<li><strong>SQL Queries Limitations</strong>: as the data are more interconnected, the traditional SQL queries struggle with optimized ways of querying and retrieving complex interlinked data and its relationships;</li>
<li><strong>Limitation of Data Interpretation</strong>: the ability to reason and understand the meaning behind data by previously data systems was missing;</li>
<li><strong>Sharing Data on Internet</strong>: the ability to reason and understand the meaning behind data by previously data systems was missing;</li>
</ul>
<p><img src="https://cdn.analyticsvidhya.com/wp-content/uploads/2024/02/Relational-Database-vs-Graph-Database-1-1-scaled.jpg" alt=""></p>
<hr>
<p>SPARQL, which stands for <strong>SPARQL Protocol and RDF Query Language</strong>, is a powerful language designed to query and manipulate data stored in RDF (Resource Description Framework) format. It is widely used to interact with linked open data and knowledge graphs, especially in the context of the Semantic Web.</p>
<hr>
<h2 id="what-is-sparql">What is SPARQL?</h2>
<ul>
<li><strong>SPARQL</strong> is the standard query language for RDF data, enabling users to query, retrieve, and manipulate data in RDF format.</li>
<li>Developed by the <strong>W3C</strong> (World Wide Web Consortium), SPARQL is designed to interact with data on the Semantic Web.</li>
<li><strong>Syntax</strong>: Similar to SQL, SPARQL queries involve selecting specific data from structured triples (subject, predicate, object).</li>
</ul>
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
<h2 id="basic-sparql-query-structure">Basic SPARQL Query Structure</h2>
<p>A basic SPARQL query contains the following components:</p>
<ol>
<li><strong>SELECT</strong> - Specifies which variables to return.</li>
<li><strong>WHERE</strong> - Defines patterns to match against the RDF triples in the dataset.</li>
<li><strong>FILTER</strong> - (Optional) Adds conditions to limit the results based on certain criteria.</li>
</ol>
<h3 id="sparql-wikidata--example">SPARQL (Wikidata)  Example:</h3>
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

