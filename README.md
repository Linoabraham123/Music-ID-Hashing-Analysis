# Music ID Hashing and Search Analysis

## Objective
Implement a hash table using the Division Method for song IDs, handle collisions using linear probing, compare hashing with linear search, and analyse the load factor and complexity.

## Given Song IDs
105, 210, 315, 420, 525, 630, 735, 840

## Hash Function
h(k) = k % 10

Hash table size = 10.

## Collision Resolution
Linear probing is used to resolve collisions.

## Final Hash Table

| Index | Song ID |
|---:|---:|
| 0 | 210 |
| 1 | 420 |
| 2 | 630 |
| 3 | 840 |
| 4 | Empty |
| 5 | 105 |
| 6 | 315 |
| 7 | 525 |
| 8 | 735 |
| 9 | Empty |

## Load Factor
Load factor = Number of elements / Table size

= 8 / 10

= 0.8 = 80%

## Search IDs Used
105, 315, 525, 735, 840, 999

The program records the number of comparisons required by hashing and linear search.

## Complexity Analysis

| Operation | Hashing | Linear Search |
|---|---|---|
| Average search | O(1) | O(n) |
| Worst-case search | O(n) | O(n) |
| Space | O(m) | O(n) |

## Files

- `src/hashing_vs_linear_search.c` - C source code
- `input/input.txt` - input data
- `output/output.txt` - sample output
- `trace/trace_table.txt` - insertion trace table
- `analysis/complexity_analysis.txt` - complexity analysis
- `analysis/comparison_table.txt` - search comparison
- `conclusion/final_conclusion.txt` - final conclusion

## Final Conclusion
The Division Method was used to implement a hash table for the given song IDs. Since several song IDs produced the same hash values, collisions occurred frequently. Linear probing was used to resolve these collisions.

The load factor of the hash table was 0.8, indicating that 80% of the table was occupied. The experimental results show that hashing can require fewer comparisons than linear search, although collisions increase the number of probes for some IDs.

The theoretical average search complexity of hashing is O(1), while linear search has O(n) search complexity. In the worst case, hashing can also require O(n) comparisons when many collisions occur.

Therefore, hashing is suitable for a music application where fast song-ID searching is required, provided that the hash table size and collision-resolution method are chosen appropriately.
