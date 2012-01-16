# levigo, LevelDB via CGO

## Building

You'll need the LevelDB shared library installed on your machine. Right now,
that means applying my [latest patch for LevelDB's
Makefile](http://code.google.com/p/leveldb/issues/detail?id=27#c10).

Now, suppose you built the LevelDB is in /path/to/lib and the headers
directory of LevelDB is in /path/to/include. In your clone of levigo, you'll run:

  CGO_CFLAGS="-I/path/to/leveldb/include" CGO_LDFLAGS="-L/path/to/lib" make install

and there you go.