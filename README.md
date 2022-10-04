# Minimax Waved Sort

---

Minimax Waved Sort combines the fast average case of randomized quicksort with the fast worst case of heapsort, while achieving linear time on inputs with certain patterns.
Below are the algorithmics complexity.

    Best        Average     Worst       Memory      Stable      Deterministic
    n           n log n     n log n     log n       No          Yes

### The best case

Linear time is achieved for inputs that are any of:

- Strictly ascending or descending in order.
- Only contain equal elements,
- Strictly in ascending order followed by one out-of-place element.

### The average case

On average case data where no patterns are detected and it reduces to a quicksort that uses
median-of-3 pivot selection, switching to insertion sort if the number of elements to be
(recursively) sorted is small. The overhead associated with detecting the patterns for the best case
is so small it lies within the error of measurement.
