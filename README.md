# pbsmrtpipe-registered-tool-contracts
Registered Tool Contracts (JSON files) for pbsmrtpipe

## Manifest
- tc/ -- Flat directory of Registered Tool Contracts.
- tc/makefile -- for convenience
- canonicalize.py -- Script to strip tailing whitespace, since the standard
  dumper in pbsmrtpipe tends to add it. This might also reformat the JSON
  and add a newline at EOF.

## Maybe someday
- chunkops/ -- Flat directory of chunk operators (XML). (Maybe we should rename this module?)
