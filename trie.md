# Trie

If you want to compare many strings, checking them one by one using brute force is slow and wastes a lot of computational effort.

```cpp
"cat" != "apple"
"cat" != "banana"
"cat" != "beach"
"cat" == "cat"
```

Instead, we can organize them into a *trie*, which is a tree-based data structure used to compare strings efficently.

```mermaid
graph TD;
    A[Root]-->B[a];
    B-->C[p];
    C-->D[p];
    D-->E[l];
    E-->F[e];

    A-->G[b];
    G-->H[a];
    H-->I[n];
    I-->J[a];
    J-->K[n];
    K-->L[a];

    G-->N[e];
    N-->O[a];
    O-->P[c];
    P-->Q[h];

    A-->R[c];
    R-->S[a];
    S-->T[t];
```

In a trie, if a character of the string doesn't match a node of corresponding depth, its children do not need to be searched, saving time compared to a brute force algorithm.

```
"c" != "a" // Cat
"c" != "b" // Cat
"c" == "c" // Cat
"a" == "a" // cAt
"t" == "t" // caT
```

