# How-Similar-Are-Two-Text-Files
This repository is for implementing a way for find how similar are two text files with python. (Linear Algebra Methods)

# Linear Algebra

## Introduction
This report details the implementation of a program to check the similarity of two text files using Python. Two approaches were explored: one straightforward and easy to understand, and the other optimized for efficiency.

## Base Step
The first step involved preparing text files, one about "Assembly X86" containing around 1200 words, and the other about "programming in the new generation" with nearly 1700 words. The data cleaning process included removing punctuation, splitting words, and converting all words to lowercase. A function called `cleanData()` was implemented for this task. Additionally, a function named `extractUniqueWords()` was developed to extract a unique list of words for more accurate results.

## Approach-1
In the first approach, three dictionaries were used: one for each text file and one for combining them. Words and their frequencies were stored in these dictionaries. The inner product of the two dictionaries was calculated by treating the values as vectors. The result was scaled to a percentage by dividing by the length of the combined dictionary.

## Approach-2 (Optimized)
The second approach focused on optimizing space usage and efficiency. Two main ideas were implemented:
1. Instead of capturing a sparse matrix, only the item name (words) and its frequency were stored, saving space.
2. Merge Sort and two-pointer technique were used for merging the words from both text files. A function named `sortDictionary` was developed to sort the dictionaries based on their keys.

The iteration continued until one of the pointers reached the end or both. Three conditions were considered based on the values pointed to by the pointers. After the main loop, any remaining elements in the arrays were handled with two additional loops. Similarity calculation was performed using the product, yielding the final result.

## Conclusion
Two approaches for determining the similarity of two text files were explored, with the second approach being more optimized. The result obtained was 20.97 percent, indicating that the two files are not very similar.

The project files, including documentation, are available on GitHub.

Thanks for your time.
