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

## Tutorial Downloads

1. Software: Download Antconc from Laurence Anthony’s website [here](http://www.laurenceanthony.net/software/antconc/). It may be necessary to unzip the file. After the download is complete, launch the application. For reference, in this tutorial, I am using Antconc version 3.5.8 for Windows.
2. Corpus: We will be using a corpus I constructed made up of governing documents, primarily constitutions, from various countries. You can download the corpus here.

## Working with Plain Text Files

The first important thing to note about Antconc is that it will only work with plain-text files (.txt); this includes XML files that are saved as .txt files. This means that Antconc will not read .doc, .docx, or .pdf files - if you want to use data from these files, you will have to convert them to .txt files.

Plain-text editors include Notepad (on Windows; this is what I use) or TextEdit (on Mac). Other free text editor options with more advanced features include Notepad++ (Windows) and TextWrangler (Mac).

In order to construct a corpus, you would have to go to where your data is stored and then copy and paste it into a .txt file. This process would then have to be repeated for each file. Corpus construction is a time-consuming task and an art in its own right. We will be using a premade corpus consisting of the constitutions/governing documents of different countries. This is a corpus that I have constructed on my own; as such, it is not the cleanest data ever (I DO INTEND TO GO BACK AND CLEAN THIS DATA). If you are interested in cleaning data, please see Antconc's tutorial on data cleaning with OpenRefine [here](https://programminghistorian.org/en/lessons/cleaning-data-with-openrefine).

## The Antconc Interface

This is what Antconc looks like when it launches:

![interface](https://user-images.githubusercontent.com/57447342/81733316-a8de8b80-9446-11ea-9728-d61b6d0b6532.png)

## Loading Corpora

We want to open the documents that we will be evaluating. However, for this tutorial, rather than opening each file one by one, we want to open the entire directory. Click File at the top of the interface:

![loadingcorpora2](https://user-images.githubusercontent.com/57447342/81733897-8e58e200-9447-11ea-9d08-096978f01ff3.png)

Next, click Open Dir:

![loadingcorpora3](https://user-images.githubusercontent.com/57447342/81733905-9022a580-9447-11ea-9b28-5dd0c91c902f.png)

You can store the documents wherever on your computer you want (I usually keep mine in a Bryn Mawr folder), but I would recommend storing them on your Desktop for this tutorial. Navigate to desktop on the menu, click on the Antconc Documents folder, and then hit OK. 

![opendir](https://user-images.githubusercontent.com/57447342/81733908-91ec6900-9447-11ea-92e9-c5d421de3a88.png)

This should load 16 files - you can see how many files have been opened in the Total No. box at the bottom left of your screen.

![loadingcorpora](https://user-images.githubusercontent.com/57447342/81733890-8c8f1e80-9447-11ea-9961-e4ee90265963.png)

If you would like to only upload certain files (which there is certainly reason to do on occasion), follow the same directions but click on Open File rather than Open Dir. You will have to add each file individually.

## Applications: Word List

The word list is a simple, yet powerful tool. Navigate to the Word List tab on the top of the interface:






              
