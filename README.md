# linked-data-project
This is my linked data project for LS 563.
This data is comprised of 50 different books from the platform Goodreads. 
The main vocabularies used here are BIBFRAME and Schema.org. 
For context, Goodreads has all editions of the same book tied to one large record for the Work as a whole. This means that different Expressions or Manifestations are all grouped together (different translations, editions, and formats are combined under one umbrella for the Work). For example, if a user reads the same book as a French translation, an English hardback, and has listened to the audiobook, they cannot provide three separate ratings because all three versions fall under the Work, and there can only be one rating per user per Work. Therefore, the average rating and number of ratings are treated as attributes of the Work and are expressed as literals in this project.
On the other hand, ISBN number, number of pages, publication date, and title are attributes of the Instance (the specific editions) and are expressed as literals. 
Each author and publisher are assigned a URI because they are distinct entities (people and organizations) that exist independently of the books in this dataset. By using URIs, these entities can be linked across multiple resources, which significantly improves discoverability on the web. Within this project, authors are tied to the overall Work, while publishers are tied to the Instance because they vary based on specific edition. 

Some examples of RDF triples in this dataset are:

ex:InaSunburnedCountry_Instance bf:title "In a Sunburned Country"@en .

ex:TheKnownWorld_Instance bf:date "2006-08-29"^^xsd:date .
