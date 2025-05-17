# 👨‍💻 Finals Task 6 – MongoDB Practice

Task 1: Insert Movies

```sql
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
```

Task 2: Querying Documents

- Get all documents
```sql
  db.movies.find()
```
- Get all documents with writer set to "Quentin Tarantino"
db.movies.find({ writer: "Quentin Tarantino" })
Get all documents where actors include "Brad Pitt"
db.movies.find({ actors: "Brad Pitt" })
Get all documents with franchise set to "The Hobbit"
  db.movies.find({ franchise: "The Hobbit" })
Get all movies released in the 1990s (1990 ≤ year ≤ 1999)
db.movies.find({ year: { $gte: 1990, $lte: 1999 } })
Get all movies released before 2000 or after 2010
db.movies.find({ $or: [ { year: { $lt: 2000 } }, { year: { $gt: 2010 } } ] })

Task 3: Updating Documents
Update documents in the movies collection as follows:
1 Add a synopsis to "The Hobbit: An Unexpected Journey":
"A reluctant hobbit, Bilbo Baggins, sets out to the Lonely Mountain with a spirited group of dwarves to reclaim their mountain home - and the gold within it - from the dragon Smaug."

2 Add a synopsis to "The Hobbit: The Desolation of Smaug":
"The dwarves, along with Bilbo Baggins and Gandalf the Grey, continue their quest to reclaim Erebor, their homeland, from Smaug. Bilbo Baggins is in possession of a mysterious and magical ring."

3 Add the actor "Samuel L. Jackson" to "Pulp Fiction".

Task 4: Text Search Queries
Write queries to:

Find all movies whose synopsis contains the word "Bilbo".

Find all movies whose synopsis contains "Gandalf".

Find all movies whose synopsis contains "Bilbo" but not "Gandalf".

Find all movies whose synopsis contains "dwarves" or "hobbit".

Find all movies whose synopsis contains both "gold" and "dragon".

Task 5: Delete Documents
Remove the following movies from the collection:

Pee Wee Herman's Big Adventure

Avatar

## 📄 Task 6 – MongoDB Files

[Download SQL File](https://github.com/NaythanIsME/EDM-Portfolio/blob/main/Finals%20Task%205/Files/ft5.sql)
