Contains code files for conversion

Query being used for conversion of Wiki Ids to DBpedia Ids as present in Simple Questions input files:

PREFIX wikiID: <http://www.wikidata.org/entity/>
select distinct ?ent ?type where { 
?ent owl:sameAs wikiID:Q76 . ?ent rdf:type ?type 
FILTER( regex( ?type, "http://dbpedia.org/ontology/"))
}

#here Q76 is just taken as an example

Query being used for conversion of Freebase Ids to DBpedia Ids as present in Web Questions input files:
