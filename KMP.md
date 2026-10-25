# Knuth-Morris-Pratt

Imagine you're trying to find the string `"AAAAAB"` in the string `"AAAAAAAAAAB"`. A naive algorithm would have to waste time comparing the `A`'s, which wastes a lot of computational effort. KMP reduces this by making sure the search pointer only ever advances forward.


