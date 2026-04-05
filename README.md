# linked-data-project
This is my linked data project for LS 563.
This data is comprised of 50 different books from the platform Goodreads. 
The main vocabularies used here are BIBFRAME and Schema.org. 
For context, Goodreads has all editions of the same book tied to one large record for the Work as a whole. This means that different Expressions or Manifestations are all grouped together, so when a person leaves a rating, their rating is tied to the Work. For example, if a user has read the same book in French, and in English as the newest hardback edition, and has also listened to the audiobook, they cannot give three separate ratings because these all fall under the same Work. That being said, the average rating and number of ratings are attributes of the Work in this project and are expressed as literals. 
On the other hand, ISBN numbers, number of pages, publication date, and title are attributes of the Instance (the specific editions) and are expressed as literals. 
Each author and publisher was given a URI because they are their own entities (people and organizations) and they exist independently of the books they are connected to in this dataset. By using URIs, these entities can be linked to multiple other books (or thinging else), which is what allows for better discoverability on the web. That being said, authors are tied to the whole Work and publishers are tied to the Instance in the RDF diagram. 
Some examples of RDF triples from this dataset are: Instance -> bf:title -> literal xsd:string
