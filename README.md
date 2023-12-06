# CS466 Final Project - Hirschberg's Algorithm

Global alignment is a common task in bioinformatics, seeking to align a given pair of sequences with minimum cost. Naively, this can be done in exponential $O(3^{n+m})$ time by just comparing every possible insertion, deletion, and substitution for all possible alignments of the two sequences, however this is clearly far too slow. Needleman-Wunsch provides a time optimization, utilizing a dynamic programming based algorithm to compute the alignment in only quadratic $O(nm)$ time, while also taking quadratic $O(nm)$ space in order to enable a backtrace.

Hirschberg's algorithm aims to address the inefficiencies in space for Needleman Wunsch. Instead of storing the entire dynamic programming table, it optimizes space efficiency through a divide and conquer paradigm, reducing the space complexity to $O(n)$ while maintaining the same quadratic time complexity $O(nm)$. This allows for handling of much larger sequences as it reduces the amount of memory required to handle a given pair significantly.

In this project, we implement the naive Needleman-Wunsch global alignment algorithm as well as the linear space Hirschberg algorithm. Using randomly generated datasets of DNA/protein sequences, we will compare the execution time and memory usage of these to algorithms over inputs of various sizes. 

Development was done in Python using Google Colab. Our project notebook is included in this repository along with our benchmarking results.

## Results:

[TODO: insert plots]
