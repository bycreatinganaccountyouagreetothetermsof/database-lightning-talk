# databaes
## (no relation)
##### lain (this/that)

---

# whats database

#### a database is specialized software for storing and retrieving data.

a lot of extremely smart people have spent decades figuring out the fastest, most reliable methods to achieve just about anything you might want to do with data

---

### "but i already have a filesystem!"
#### that's valid.

you can use that! but you will eventually start to have a very bad time as your application gets larger and starts doing more stuff.

files are for discrete, standalone chunks of data that will only change at rare intervals, intended to be accessed in human contexts.

---

## ok, db

![[hackin.gif]]

#### relational and non-relational

---

### relational??
#### often "SQL"

![[postgresql-logo.png|200]]	![[mysql-logo.png|200]]

very common, the "classic" database. relational databases use *relationships between data* as part of their structure.

---

### relational...

in practice this means defining *tables* in which each *row* inside the table has a *key* or *index* and fills out various *columns* and perhaps has *links* corresponding to other tables or keys.

![[relational-visual.png]]

---

### relational~

these data relationships can be very complex, and may result in lots of tables that exist just to define relationships.

this set of relationships must be carefully updated in tandem with your application as you create new behaviors and features.

---

### nonrelational!!
#### aka "NoSQL"

![[mongodb-logo.png|150]] ![[couchdb-logo.png|100]] ![[redis-logo.png|150]]

most of the time, especially for webapps, you don't need all that junk.

at some point someone said heck it and wrote some software that just put everything in one big bucket. no more tables!!

think of it like a big hash map. 

---

### nonrelational...

![[nonrelational-normalized-visual.png|400]]

simplified: every record in the database is a standalone *document*, referenced by a *key* that is typically just a *hash*, and relationships it may have can only be known by data within the document (or... another document?)

---

# think of it like types
#### relational = strong types
#### nonrelational = dynamic types

---

relational database                 | non-relational database
------------------------------------------------|------------------------------------
well-defined structure enforces sanity          | absence of strict structure enables rapid development
every relationship is explicit in the structure | links handled on per-document basis
select any "type" of data by using tables       | data are treated the same
can handle complex queries                      | technically simpler, easier to scale

---

## cap theorem

![[cap-theorem.png]]

---


# middle ground

a non-relational database may implement simple tables/collections or other basic structure. some have column-like and linking features that provide some structure. they might even provide SQL interfaces just like a relational database!

lots of relational database software has implemented hash-key lookups like nonrelational databases.

some non-relational databases are literally just implemented on top of relational databases, or may be used as a cache for relational databases.

many projects that use non-relational databases end up reimplementing some of the functionality provided by relational databases.

---
 
 # none of this matters
 ## to you
 ### yet
 
 as a junior dev, you will literally not be making any of these decisions. it's someone else's problem. you will use whatever your team already has in place.
 
 by the time you are in a position to make these decisions, you should know a ton about both kinds of databases and you won't even remember these slides
 
 ---
 
 # bye
