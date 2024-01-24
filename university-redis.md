# What are Redis Data Structures

## Keys
Keys are the primary way to access data values.
- Redis commands operate on a key or keys

Keys are
  - unique
  - binary safe
  - 512MB

Key Spaces

Logical databases 

SET key value
  - set customer: 1000 fred
GET key

KEYS
- blocks until completed
- never run in production
- useful for debugging

SCANS
- iterates using a cursor
- safe for production
- return 0 or more keys per call

SCAN slot MATCH pattern
