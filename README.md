# SPARQL 

# Introduction to SPARQL

SPARQL, which stands for **SPARQL Protocol and RDF Query Language**, is a powerful language designed to query and manipulate data stored in RDF (Resource Description Framework) format. It is widely used to interact with linked open data and knowledge graphs, especially in the context of the Semantic Web.

---

## What is SPARQL?

- **SPARQL** is the standard query language for RDF data, enabling users to query, retrieve, and manipulate data in RDF format.
- Developed by the **W3C** (World Wide Web Consortium), SPARQL is designed to interact with data on the Semantic Web.
- **Syntax**: Similar to SQL, SPARQL queries involve selecting specific data from structured triples (subject, predicate, object).

### Example of RDF Triples
| Subject         | Predicate       | Object          |
|-----------------|-----------------|-----------------|
| `<John>`        | `<likes>`       | `<Pizza>`       |
| `<City:Paris>`  | `<isInCountry>` | `<Country:France>` |

---

## Basic SPARQL Query Structure

A basic SPARQL query contains the following components:

1. **SELECT** - Specifies which variables to return.
2. **WHERE** - Defines patterns to match against the RDF triples in the dataset.
3. **FILTER** - (Optional) Adds conditions to limit the results based on certain criteria.
### SPARQL (Wikidata)  Example:

### Example SPARQL Query

The following highlighted SPARQL query retrieves all people who studied at Trinity College:

[comment]:<> (query specifying what i meant)

**?person wdt:P69 wd:Q332342 .**

| wdt| wd|          
|-----------------|-----------------|
| `<property>`        | `<entity>`       | 
|   `<educated at>` | `Trinity College`	|  


```sparql
SELECT ?person ?personLabel ?birth_placeLabel ?coodinates
WHERE{

  ?person wdt:P69 wd:Q332342 . # all those who studied at Trinity College in Ireland
  
  ?person wdt:P106 wd:Q170790 . # ordered by occupation listed
  ?person wdt:P21 wd:Q6581097 . # male who studied at Trinity College
  ?person wdt:P19 ?birth_place . # place of birth , make sure the name given is at select query on top
  # with Label after the name ensure the name of that searched identifier
  ?birth_place wdt:P625 ?coodinates .
  
   SERVICE wikibase:label { 
       bd:serviceParam wikibase:language "en" . }
     #service provided by examples on wikidata query service

}
```

[comment]: <> (Source: [Using SPARQL and SPIN for Data Quality Management on the Semantic Web | SpringerLink](https://link.springer.com/chapter/10.1007/978-3-642-12814-1_4)

[comment]: <> (Source: [A review of the semantic web field | Communications of the ACM](https://dl.acm.org/doi/10.1145/3397512)

[comment]: <> (Source: [SPARQL - An Absolute Beginner's Guide - DEV Community](https://dev.to/edent/sparql-an-absolute-beginner-s-guide-2c65#:~:text=Assign%20to%20the%20variable%2C%20data%20where%20the%20property,entity%2C%20and%20Q84%20is%20the%20ID%20of%20London.)
