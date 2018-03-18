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

This data structure also stores the unhashed data in `m.raw_leaves` so that it can be accessed for application usage. You can also pass a hash of a leaf and get the data back by using `m.data_for_hash(h)`. If a piece of data unhashed exists in the raw leaves, it will be returned.
