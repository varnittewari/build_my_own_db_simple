Created my own simple Redis-like database server.

The server I built should respond to the following commands:
GET <key>
SET <key> <value>
DELETE <key>
FLUSH
MGET <key1> ... <keyn>
MSET <key1> <value1> ... <keyn> <valuen>


These are the supported data types:
Strings and Binary Data
Numbers
NULL
Arrays (which may be nested)
Dictionaries (which may be nested)
Error messages

The Redis protocol uses a request/response communication pattern with the clients. Responses from the server will use the first byte to indicate data-type, followed by the data, terminated by a carriage-return/line-feed.
