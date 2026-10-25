# Knuth-Morris-Pratt

Imagine you're trying to find the string `"AAAAAB"` in the string `"AAAAAAAAAAB"`. A naive algorithm would have to waste time comparing the `A`'s, which wastes a lot of computational effort. KMP reduces this by making sure the search pointer only ever advances forward.

Before KMP starts searching the string, it has to build a prefix array, which contains the length of the maximum common prefix and suffix for every substring beginning at the first element. The algorithm for building the prefix is:

```python
fill prefix with zeros
set prefix[0] to 1
set j to zero
for every character i in the array starting from the second one:
    while there is no match and j is positive:
        set j to prefix[j]
    if i and the character at j match, increment j by one
    set prefix[i] to j
```

The most interesting part is in lines 5-6. In that part, we are looking for shorter prefix-suffix matches to fall back to. If we just decrement j, we would be wasting a lot of time checking known-invalid prefix-suffix pairs.
