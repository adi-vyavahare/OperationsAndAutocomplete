# Operations and Autocomplete

Autocomplete or Word Completion is a powerful feature that suggests possible extensions to a partially written text. It is widely used in search engines and enhances user experience. This project focuses on implementing autocomplete functionality using a basic Trie data structure.

## Trie Data Structure

The Trie data structure is a tree-like data structure used for efficiently locating specific keys within a set. It is particularly useful for retrieving keys in a large collection of strings. In the Trie structure, nodes store associated keys of strings, and traversing the trie helps access the desired key efficiently.

## Problem Statement

Given a Trie with a set of strings, the goal is to provide autocomplete suggestions to the user based on their partial search query. For example, if the Trie stores the strings { "abc", "abcd", "aa", "abbbaba" }, and the user types "ab" as the prefix, the program should suggest { "abc", "abcd", "abbbaba" } as autocomplete recommendations.

## Solution

The project implements a basic Trie data structure to achieve autocomplete functionality. The primary objective is to return a list of words when provided with a query prefix. The following steps outline the solution:

1. Search for the given query using the standard Trie search algorithm.
2. If the query prefix itself is not present, return -1 to indicate the absence.
3. If the query is present and marks the end of a word in the Trie, print the query.
4. If the last matching node of the query has no children, return.
5. Otherwise, recursively print all nodes under the subtree of the last matching node.

## Operations Performed

The project supports the following operations on the Trie:

1. Adding a word to the Trie
2. Deleting a word from the Trie
3. Searching for a word
4. Displaying the list of words in the Trie
5. Fetching a word list for a given prefix

## Time Complexity

Trie provides an efficient approach for autocomplete functionality. It reduces search complexities to an optimal limit based on the key length. When compared to storing keys in a binary search tree, a well-balanced BST requires time proportional to M * log N, where M is the maximum string length and N is the number of keys. The auxiliary space requirement for the Trie is constant, as it does not utilize any extra space. Adding a word to the Trie runs in time proportional to the length of the word. Using the Trie, we can search for a key in O(M) time, where M is the length of the key.
