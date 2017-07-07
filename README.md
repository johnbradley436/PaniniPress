# The Panini Press
### Grammar is fun. Everything else leads back to zero.


= Panini Press
:neo4j-version: 3.1.4
:author: John Bradley

==  Completed Graph


//graph

=== OUR DATASET
[source, cypher]
----
CREATE
//Person
(Panini:Person {name: 'Panini'}),

//Organization
(WritingStudio:Organization {name: 'The Writing Studio'}),
(TutoringServices:Organization {name: 'Tutoring Services'}),

//Concept
(SanskritGrammar:Concept {name: 'Sanskrit Grammar'}),
(Zero:Concept {name: 'Zero'}),
(CollaborativeLearning:Concept {name: 'Collaborative Learning'}),
(Transdisciplinarity:Concept {name: 'Transdisciplinarity'}),

//Relationship
(Panini)-[:CREATED]->(Zero),
(Panini)-[:CREATED]->(SanskritGrammar),
(Panini)-[:SUBJECT_OF]->(CollaborativeLearning),
(Panini)-[:EXAMPLE_OF]->(Transdisciplinarity),
(WritingStudio)-[:INTERESTED_IN]->(Transdisciplinarity),
(WritingStudio)-[:INTERESTED_IN]->(CollaborativeLearning),
(TutoringServices)-[:INTERESTED_IN]->(Transdisciplinarity),
(TutoringServices)-[:INTERESTED_IN]->(CollaborativeLearning)

----
