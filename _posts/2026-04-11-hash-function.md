---
layout: post
title: Hash Function in Partitioning
---

### Why not using mod as hash funciton in partitioning in distributed system

When new node is added to the system, rebalancing could happen. When we use mod(%) as the hash function, all the hash value we have calculated befored will be different, e.g. if the hash value is 1 applied from mod using key 11 mod 10, the new hash value could become 0 if the mod become 11. Some much change of hash values will result in low efficiency and overhead in system.

### What other hash function do
Hash funcitons like MD and SHA-1 will generate the same hash value when new node is added to the system. That will make only little part of whole data be transfered, which can be fast.
