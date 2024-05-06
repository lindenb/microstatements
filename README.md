# microstatements

## Motivation

cutsom RDF statements for bioinformatics to complete larger RDF databases like MONDO

## How to contribute

* clone this repo
* open `data/statements.01.ttl` with a text editor
* add your info in the first lines, using your **ORCID** ID as a unique identifier. e.g:

```
orcid:0000-0000-0123-456
    rdf:type foaf:Person ;
    foaf:name "your name"
    .
```

* add a new statements. e.g:

```ttl

<#stmt1786>
    dc:description "PITX2 and atrial fibrillation" ;
    rdf:type rdf:Statement ;
    rdf:subject obo:MONDO_0004981  ;
    rdf:predicate obo:RO_0004003 ;
    rdf:object hgnc:9005 ;
    dc:creator orcid:0000-0003-0148-9787 ;
    dc:created "2024-05-16"^^xsd:date ; 
    dc:source pmid:38643172
    .

```

where:

- `stmt1786` is a unique name for your statement
- `dc:description "PITX2 and atrial fibrillation"` is a short description of the statement.
- `rdf:subject obo:MONDO_0004981` the subject for this statement statement is [http://purl.obolibrary.org/obo/MONDO_0004981](http://purl.obolibrary.org/obo/MONDO_0004981) **atrial fibrillation**
- `rdf:predicate obo:RO_0004003`  the property for this statement is [http://purl.obolibrary.org/obo/RO_0004003](http://purl.obolibrary.org/obo/RO_0004003) **has material basis in germline mutation in**
- `rdf:object hgnc:9005`  the object for this statement is [https://www.genenames.org/data/gene-symbol-report/#!/hgnc_id/HGNC:9005](https://www.genenames.org/data/gene-symbol-report/#!/hgnc_id/HGNC:9005) **PITX2**
- `dc:creator orcid:0000-0003-0148-9787 ` the author for this statement
- `dc:created "2024-05-16"^^xsd:date` the date this statement was created
- `dc:source pmid:38643172` an article supporting this statement : [https://pubmed.ncbi.nlm.nih.gov/38643172/](https://pubmed.ncbi.nlm.nih.gov/38643172/) "TAD boundary deletion causes PITX2-related cardiac electrical and structural defects"
 
* submit the new statement using a pull request.
 
## See also
 
* https://www.ebi.ac.uk/ols4/
* https://www.genenames.org/
* https://github.com/monarch-initiative/mondo

## License

The project is licensed under the MIT license.

## Author

Pierre Lindenbaum PhD

