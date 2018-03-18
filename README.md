There wasn't a super simple implementation of a Merkle tree available online so we decided to make one.

## Install

`pip install merk`

## How to Use

```
# Initialize a Merkle Tree by passing a list of leaves
m = MerkleTree(['a', 'b', 'c'])

# Now you can access any of the nodes either via list,
# or by passing a hash of a node and receiving the children.
m.leaves
m.root()
m.children(m.root())
etc..

# Implementation uses SHA3 256 via Python 3's hashlib
```
