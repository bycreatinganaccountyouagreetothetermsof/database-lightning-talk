# todo
* middle ground stuff?
* maybe a bit on sql
* tables in slides

---

# databaes (no relation)
## lain (the/that)

---

# whats database

a database is specialized software for storing and retrieving data.

---

## but files

you might think, "but i already have a filesystem!" and that's valid. but you would eventually start to have a very bad time as your application got larger and started doing more stuff.

files are for files, generally larger chunks of binary or text data that is only going to change at rare intervals, intended to be accessed in human contexts.

---

## ok, db

databases are oriented towards managing data for which the individual datums are smaller than would make sense to write to a file alone, and the data may be accessed or changed rapidly and constantly in very complex ways by computer programs or large numbers of people.

---

a lot of extremely smart people have spent decades figuring out the fastest and lowest-complexity methods to achieve just about anything you might want to do with data

databases are optimized for high performance. they provide nifty features like searching, performing complex filtering operations on data, distributing scaling accross multiple computers, and enforcing consistency

---

### relational??

![[postgresql-logo.png|200]]	![[mysql-logo.png|200]]

very common, the "classic" database. relational databases use *relationships between data* as part of their structure. typically use SQL for queries.

---

### relational...

in practice this means defining *tables* in which each *row* inside the table has a *key* or *index* and fills out various *columns* and perhaps has *links* corresponding to other tables or keys.

![[relational-visual.png]]

---

### relational~

these data relationships can be very complex, and may result in lots of tables that exist just to define relationships. this set of relationships has to be carefully updated in tandem with your application as you create new behaviors and features.

---

### nonrelational!!

![[mongodb-logo.png|150]] ![[couchdb-logo.png|150]] ![[redis-logo.png|150]]

most of the time, especially for webapps, you don't need all that junk. at some point someone said heck it and wrote some software that just put everything in one big bucket. no more tables!!

think of it like a big hash map.

---

### nonrelational...

![[nonrelational-normalized-visual.png|300]]

simplified: every record in the database is a standalone *document*, referenced by a *key* that is typically just a *hash*, and relationships it may have can only be known by data within the document (or... another document?)

---

benefits of non-relational database | benefits of relational database
-|-
absence of strict structure enables rapid development | well-defined structure enforces sanity
handle links to other documents on a per-document basis | every relationship is explicit in the structure
all documents are treated the same | select any "type" of data by using tables
technically easier to scale | can handle complex queries

---

# middle ground

a non-relational database may implement simple tables/collections or other basic structure. some have column-like and linking features that provide some structure. they might even provide SQL interfaces just like a relational database!

many projects that use non-relational databases end up reimplementing some of the functionality provided by relational databases.

lots of relational database software has implemented hash-key lookups like nonrelational databases.