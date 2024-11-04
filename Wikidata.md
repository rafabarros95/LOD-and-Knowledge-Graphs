---


---

<p><strong>Author(s): Rafael Barros and Bhagyasha Patil</strong><br>
<strong>Date: November 5th 2024</strong></p>
<h1 id="welcome">Welcome</h1>
<p><img src="https://diff.wikimedia.org/wp-content/uploads/2024/03/image_acf9c3.png?fit=584%2C600" alt="wikidata"></p>
<hr>
<h1 id="learning-outcomes">Learning Outcomes</h1>
<p><strong>Context and Meaning, Concepts, Structure,  Applications, Limitations and an example with SPARQL  and  Wikidata</strong></p>
<hr>
<h1 id="context">Context</h1>
<p><strong>Wikidata Environment</strong></p>
<ul>
<li>Before Wikidata, data across Wikimedia projects such as Wikipedia existed in a <em><strong>unstructured and decentralized format</strong></em>;</li>
<li><strong>Example:</strong> each wikipedia language version maintained its own datasets for items like birthdates, coodinates and so on;</li>
<li><strong>Result</strong>: it leaded to redundancy, inconsistency and bunch of coherence across languages;</li>
</ul>
<p><strong>Multi-Language centralized  Data Hub needed</strong></p>
<ul>
<li>The <strong>growing use of linked data in web applications and knowledge graphs</strong> revealed the need for a centralized, <em><strong>language-independent</strong></em>, machine-readable repository;</li>
</ul>
<hr>
<h1 id="purposes">Purposes</h1>
<ul>
<li>
<p>Wikidata’s goal is centralizing data for all Wikimedia projects and freely available for all users for reuse;</p>
</li>
<li>
<p><strong>mission</strong>: make the structured knowledge available for both humans and machines;</p>
</li>
<li>
<p><strong>Core focus:</strong> <em><strong>Open Data</strong></em> that can be edited by anybody and also reused anywhere;</p>
</li>
</ul>
<hr>
<h1 id="concepts">Concepts</h1>
<ul>
<li>
<p>defining <strong>items</strong> (unit) like people, places and <strong>property</strong> which describes its attibutes and relationships, like ‘birth date’, ‘occupation’, ‘educated at’ etc;</p>
</li>
<li>
<p><strong>Statements and references</strong>: a combo ( item-property-value ) define a factual information;</p>
</li>
</ul>
<hr>
<h1 id="structure-and-model">Structure and Model</h1>
<ul>
<li>same principle as with RDF  based on <strong>triples format</strong> (subject-predicate-object);</li>
<li><strong>Example:</strong></li>
</ul>
<pre class=" language-sparql"><code class="prism  language-sparql">- ASK WHERE {
 dbr:Cologne dbo:country dbr:Germany .
}
</code></pre>
<p><img src="https://th.bing.com/th/id/R.099b57f2ca635de32f62125d665cc0f8?rik=Y1Du%2fEgBkOw31A&amp;riu=http%3a%2f%2flim.univ-reunion.fr%2fstaff%2ffred%2fEnseignement%2fSW%2fSPARQL-by-example%2fspo-arrow.png&amp;ehk=t%2bd7wD6Wie0rfSDW%2f3TdT93%2fWU4xAro52EYV%2b6mgQtQ%3d&amp;risl=&amp;pid=ImgRaw&amp;r=0" alt="order"></p>
<hr>
<h1 id="what-is-wikidata">What is Wikidata?</h1>
<p><img src="https://www.wikimedia.de/2019/wp-content/uploads/sites/2/2020/06/wikidatat-grafik_jahrebericht_englisch-1440x1002.png" alt="Wikidata Concept and LOD"></p>
<hr>
<ul>
<li>
<p><em><strong>a free, collaborative, multilingual knowledge base.</strong></em></p>
</li>
<li>
<p>part of the <strong>Wikimedia Foundation</strong> (like Wikipedia - an encyclopedia hosted by Wikimedia  which provides the infrastructure for thousands of global volunteers to create and edit pages).</p>
</li>
<li>
<p>Wikidata stores information as structured data in a database.</p>
</li>
<li>
<p>the data stored and shared as LOD is discernable by machines and intelligent devices like Alexa, Siri, and others.</p>
</li>
<li>
<p><strong>Link to NLP (see in applications)</strong>: LOD provides structured, semantically rich data, which helps NLP algorithms interpret words and concepts in context;<br>
<strong>Example:</strong> if a virtual assistant like Siri queries a dataset containing LOD, it can retrieve precise information about entities (like people, places, or objects) and their relationships, improving its ability to understand and respond accurately.</p>
</li>
<li>
<p><strong>Bullet point:</strong> Central source for structured data that can be used across Wikimedia projects and beyond.</p>
</li>
</ul>
<hr>
<h1 id="thinking-of-contributing">Thinking of Contributing?</h1>
<p><strong>How to get started?</strong></p>
<ul>
<li>Set up an account</li>
<li>Basic editing tools</li>
</ul>
<p><strong>Types of Contributions</strong></p>
<ul>
<li>Adding new entities</li>
<li>Editing or updating statements</li>
<li>Translating labels and descriptions</li>
</ul>
<p><strong>Community Guidelines</strong></p>
<ul>
<li>Notability of entities</li>
<li>Citing reliable sources</li>
<li>Respecting data accuracy and applications</li>
</ul>
<p><strong>Why Contribute?</strong></p>
<ul>
<li>Improve global knowledge</li>
</ul>
<hr>
<h1 id="applications">Applications</h1>
<ul>
<li>
<p><strong>Wikidata</strong> as a training dataset for AI/ML models;</p>
</li>
<li>
<p><strong>NLP</strong>: Entity Recognition and Machine Translation as linked in the picture shown;</p>
</li>
<li>
<p><strong>chatbots</strong> and <strong>voice assistants</strong> like alexa need entity databases ( well-structured by wikidata );</p>
</li>
<li>
<p><strong>Integration with other platforms</strong> - Knowledge Graph, VIAF and Europeana;</p>
</li>
</ul>
<hr>
<h1 id="fields">Fields</h1>
<ul>
<li>
<p><strong>Healthcare</strong>: medical research databases, linking diseases and treatments;</p>
</li>
<li>
<p><strong>Cultural Heritage</strong>: Museum data, cataloging artifacts;</p>
</li>
<li>
<p><strong>E-Commerce</strong>: Product categorization and recommendation systems;</p>
</li>
</ul>
<hr>
<h1 id="others-real-world-user-cases">Others Real-World User Cases</h1>
<ul>
<li>Digital Libraries and archives</li>
<li>Cultural and Educational projects</li>
<li>Academic and scientific research</li>
<li>Used to populate infoboxes and update articles across languages</li>
</ul>
<hr>
<h1 id="limitations">Limitations</h1>
<ul>
<li>
<p><strong>Data quality and vandalism issues due to open editing data</strong></p>
</li>
<li>
<p><strong>Data management and maintenance in terms of complexity</strong></p>
</li>
<li>
<p><strong>Multilingual data challenges and need for standardization</strong></p>
</li>
</ul>
<hr>
<h1 id="querying-wikidata-with-sparql">Querying Wikidata with SPARQL</h1>
<p><img src="https://ubc-library-rc.github.io/intro-wiki/content/images/wikidata-data-model.png" alt="Wikidata  breaking down its content"></p>
<hr>
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
</table><hr>
<pre class=" language-sparql"><code class="prism  language-sparql">SELECT ?person ?personLabel ?birth_placeLabel ?coodinates
 
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
<hr>
<h1 id="references">References</h1>
<ul>
<li>
<p><a href="https://www.wikimedia.de/2019/en/themen/wikidata/#:~:text=The%20free%20knowledge%20database%20Wikidata%20is%20the%20largest,data%20sets%20and%20provide%20feedback%20on%20the%20software.">Wikidata – Wikimedia Germany</a></p>
</li>
<li>
<p><a href="https://query.wikidata.org/">Wikidata Query Service</a></p>
</li>
<li>
<p><a href="https://www.sciencedirect.com/science/article/pii/S0099133321000173">Much more than a mere technology: A systematic review of Wikidata in libraries - ScienceDirect</a></p>
</li>
</ul>
<hr>
<h1 id="conclusion">Conclusion</h1>
<p>Thank you for attending our presentation!</p>
<hr>

