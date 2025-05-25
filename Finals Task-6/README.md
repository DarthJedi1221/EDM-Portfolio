# Finals Task 6 – MongoDB Practice
## Task 1: Insert Movies
db.movies.insertMany([
  {
    title: "Fight Club",
    writer: "Chuck Palahniuk",
    year: 1999,
    actors: ["Brad Pitt", "Edward Norton"]
  },
  {
    title: "Pulp Fiction",
    writer: "Quentin Tarantino",
    year: 1994,
    actors: ["John Travolta", "Uma Thurman"]
  },
  {
    title: "Inglorious Basterds",
    writer: "Quentin Tarantino",
    year: 2009,
    actors: ["Brad Pitt", "Diane Kruger", "Eli Roth"]
  },
  {
    title: "The Hobbit: An Unexpected Journey",
    writer: "J.R.R. Tolkien",
    year: 2012,
    franchise: "The Hobbit"
  },
  {
    title: "The Hobbit: The Desolation of Smaug",
    writer: "J.R.R. Tolkien",
    year: 2013,
    franchise: "The Hobbit"
  },
  {
    title: "The Hobbit: The Battle of the Five Armies",
    writer: "J.R.R. Tolkien",
    year: 2014,
    franchise: "The Hobbit",
    synopsis: "Bilbo and Company are forced to engage in a war against an array of combatants and keep the Lonely Mountain from falling into the hands of a rising darkness."
  },
  {
    title: "Pee Wee Herman's Big Adventure"
  },
  {
    title: "Avatar"
  }
])
![image](https://github.com/user-attachments/assets/93b4749c-7d30-46b9-b15d-a20e602fcaed)
## Task 2: Querying Documents
  db.movies.find()
  ![image](https://github.com/user-attachments/assets/8a5bc2be-8863-4c56-a5d3-71707f0e8337)
  - Get all documents with writer set to "Quentin Tarantino"
db.movies.find({ writer: "Quentin Tarantino" })
![image](https://github.com/user-attachments/assets/860fc7d3-e06f-4491-bfaf-5f04ca6f3ba6)
 - Get all documents where actors include "Brad Pitt"
db.movies.find({ actors: "Brad Pitt" })
![image](https://github.com/user-attachments/assets/0ad62c76-88a9-4e9f-b33d-e7c0af3f28f4)
- Get all documents with franchise set to "The Hobbit"
db.movies.find({ franchise: "The Hobbit" })
![image](https://github.com/user-attachments/assets/5d9d93bb-331c-4a1d-a486-ca770e047d00)
- Get all movies released in the 1990s (1990 ≤ year ≤ 1999)
db.movies.find({ year: { $gte: 1990, $lte: 1999 } })
![image](https://github.com/user-attachments/assets/855e7276-89ce-4e57-863c-bdbdc1dc26b5)
- Get all movies released before 2000 or after 2010
db.movies.find({ $or: [ { year: { $lt: 2000 } }, { year: { $gt: 2010 } } ] })
![image](https://github.com/user-attachments/assets/f82f41cf-5eab-4637-8616-dfaddff20916)
## Task 3: Updating Documents
Update documents in the movies collection as follows:
- Add a synopsis to "The Hobbit: An Unexpected Journey": "A reluctant hobbit, Bilbo Baggins, sets out to the Lonely Mountain with a spirited group of dwarves to reclaim 
  their mountain home - and the gold within it - from the dragon Smaug."
![image](https://github.com/user-attachments/assets/462224f8-687a-40a1-acad-2e9cb4b71fa3)
- Add a synopsis to "The Hobbit: The Desolation of Smaug": "The dwarves, along with Bilbo Baggins and Gandalf the Grey, continue their quest to reclaim Erebor, their 
 homeland, from Smaug. Bilbo Baggins is in possession of a mysterious and magical ring."
![image](https://github.com/user-attachments/assets/7f8b58f0-bfa1-49eb-b9ec-bb15ca9dca99)
- Add the actor "Samuel L. Jackson" to "Pulp Fiction".
![image](https://github.com/user-attachments/assets/7539da74-efbe-459d-86ee-1f1dab1771c4)
## Task 4: Text Search Queries
Write queries to:
- Find all movies whose synopsis contains the word "Bilbo".
![image](https://github.com/user-attachments/assets/a31a892b-c041-4d91-8465-926e57baf088)
- Find all movies whose synopsis contains "Gandalf".
![image](https://github.com/user-attachments/assets/bd740944-aef4-4490-ae8b-2fbdbeba801e)
- Find all movies whose synopsis contains "Bilbo" but not "Gandalf".
![image](https://github.com/user-attachments/assets/886e3152-ebef-4c10-b48b-78b9e5926b73)
- Find all movies whose synopsis contains "dwarves" or "hobbit".
![image](https://github.com/user-attachments/assets/84646597-930d-44ea-a695-83b746c8f566)
- Find all movies whose synopsis contains both "gold" and "dragon".
![image](https://github.com/user-attachments/assets/94f5e0a5-1f49-4c50-af4f-a7b681db6ffe)
## Task 5: Delete Documents
Remove the following movies from the collection:
- Pee Wee Herman's Big Adventure
![image](https://github.com/user-attachments/assets/92281902-33d6-4f26-bcc3-34b2f6b0d707)
- Avatar
![image](https://github.com/user-attachments/assets/402163c8-a68f-40e0-aa4f-237e4e16593f)
## 📄 Task 6 – MongoDB Files
[Mongodb files](https://github.com/Blooper1209/Portfolio/blob/main/Finals%20Task-6/Files%20/mongo_practice.movies.json)










