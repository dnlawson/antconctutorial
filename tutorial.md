# Corpus Analysis With Antconc by Devin Lawson

## Overview of Tutorial

1. Introduction to corpus analysis and Antconc
2. Tutorial downloads
3. Working with plain text files
4. The Antconc interface
5. Loading corpora
6. Applications
    1. Word list
    2. Concordance
            1. Search operators
                    1. *
                    2. ?
                    3. +
                    4. @
                    5. #
                    6. |
                    7. Combining search operators
                    8. Exporting data from search operators
    3. Concordance plots
    4. File view
    5. Clusters/N-Grams
    6. Collocates
    7. Keyword list
7. What we do with the data?
8. Acknolwedgements and further resources

## Introduction to Corpus Analysis and Antconc

Corpus analysis is a form of text analysis that allows us to compare textual objects “from a distance.” In many ways, corpus analysis is the opposite of a close reading. In a close reading, a small portion of text is looked at and evaluated at a minute level; in Classics, this often means paying special attention to the specific forms of words or meter. In sum, every single bit of a small chunk of text is picked apart down to the smallest detail. On the other hand, corpus analysis focuses instead on a much larger body of text; for example, one author’s entire literary corpus. The focus here is instead on finding large patterns, such as common grammatical usages or frequently used words. The smaller details are less important, and the focus is on the larger, overarching patterns that are present. Corpus analysis is incredibly helpful in distinguishing patterns that the human eye might not pick up on, but that could raise important research questions about the text. However, corpus analysis is also a good way to confirm intuitions or gut instincts that we have about a text. For example, I took a course on Plato & Thucydides my first semester of grad school. We read Book 6 of Thucydides, in which the Athenians are debating whether or not to aid the Sicilians who have asked for their help. The book is presented as a series of speeches between Alcibiades and Nicias. One of my classmates asked whether or not the increased complexity of Nicias’ grammar and syntax was a reflection of his cautious and indecisive character. We read an article, written in the 70s, that argued exactly that (for those interested, the article is *Stylistic characterization in Thucydides: Nicias and Alcibiades* by Daniel Tompkins. While this article was published well before Digital Humanities became an established discipline, the author used many techniques that are now commonplace in Digital Humanities; in fact, Antconc would have been particularly useful for this kind of project.
Antconc is a standalone software package for the linguistic analysis of texts. It mediates between the simplicity of a tool like Voyant and the complexity of Python and R programming. It is freely available and runs on Windows, Mac OS, and Linux. The creator, Anthony Laurence, is excellent at maintaining the software, making it a powerful tool for any level of experience.
In this tutorial, you will:
* Learn the basic applications of Antconc
* Think about how to generate research questions from that data that you have collected

              
