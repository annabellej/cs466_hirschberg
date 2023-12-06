# CS466 Final Project - Hirschberg's Algorithm

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Global alignment is a common task in bioinformatics, seeking to align a given pair of sequences with minimum cost. Naively, this can be done in exponential $O(3^{n+m})$ time by just comparing every possible insertion, deletion, and substitution for all possible alignments of the two sequences, however this is clearly far too slow. Needleman-Wunsch provides a time optimization, utilizing a dynamic programming based algorithm to compute the alignment in only quadratic $O(nm)$ time, while also taking quadratic $O(nm)$ space in order to enable a backtrace.

Hirschberg's algorithm aims to address the inefficiencies in space for Needleman Wunsch. Instead of storing the entire dynamic programming table, it optimizes space efficiency through a divide and conquer paradigm, reducing the space complexity to $O(n)$ while maintaining the same quadratic time complexity $O(nm)$. This allows for handling of much larger sequences as it reduces the amount of memory required to handle a given pair significantly.

In this project, we implement the naive Needleman-Wunsch global alignment algorithm as well as the linear space Hirschberg algorithm. Using randomly generated datasets of DNA/protein sequences, we will compare the execution time and memory usage of these to algorithms over inputs of various sizes. 

Development was done in Python using Google Colab. Our project notebook is included in this repository along with our benchmarking results.

## Results:

### Needleman-Wunsch
| Memory | Time |
| ------ | ---- |
| <img width="610" alt="nw_time" src="https://github.com/annabellej/cs466_hirschberg/assets/39597635/56bebac8-3cfe-42a0-a70a-c2c3cc5a99e6"> | <img width="629" alt="nw_mem" src="https://github.com/annabellej/cs466_hirschberg/assets/39597635/317cde54-ab14-41c4-81d6-f4eeeb59ffab"> |

### Hirschberg:
| Memory | Time |
| ------ | ---- |
| <img width="624" alt="h_time" src="https://github.com/annabellej/cs466_hirschberg/assets/39597635/1b99ddd4-63b6-45ae-8231-4b24f66237fa"> | <img width="647" alt="h_mem" src="https://github.com/annabellej/cs466_hirschberg/assets/39597635/72924a46-d2b1-4b27-8b0f-eb23c315aac8"> |
