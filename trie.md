# Trie

A trie is a tree-based data structure used for searching strings. If you want to check many strings, checking them one by one using brute force is slow and wastes a lot of computational effort.

```cpp
"cat" != "apple"
"cat" != "banana"
"cat" != "beach"
"cat" == "cat"
```

Instead, we can organize them into a *trie*, like this:

```mermaid
flowchart TRIE
  A[root] --> B[A]
```
