# Corpus Analysis With Antconc by Devin Lawson

## Overview of Tutorial

1. [Introduction to corpus analysis and Antconc](#Introduction-to-Corpus-Analysis-and-Antconc)
2. [Tutorial downloads](#Tutorial-Downloads)
3. [Working with plain text files](#Working-with-Plain-Text-Files)
4. [The Antconc interface](#The-Antconc-Interface)
5. [Loading corpora](#Loading-Corpora)
6. Applications
    1. [Word list](#Applications-Word-List)
    2. [Concordance](#Applications-Concordance)
        1. [Search operators](#Search-Operators)
              1. ["*"](#The-Star-Operator-Wildcard)
              2. ["?"](#The-Question-Mark-Operator)
              3. ["+"](#The-Plus-Operator)
              4. ["@"](#The-At-Operator)
              5. ["#"](#The-Pound-Operator)
              6. ["|"](#The-Or-Operator)
              7. [Combining search operators](#Combining-operators)
              8. [Exporting data from search operators](#Exporting-Data-from-Search-Operators)
         2. [Stopword lists](#Stopword-Lists)
    3. [Concordance plots](#Applications-Concordance-Plots)
    4. [File view](#Applications-File-View)
    5. [Clusters/N-Grams](#Applications-ClustersN-Grams)
    6. [Collocates](#Applications-Collocates)
    7. [Keyword list](#Applications-Keyword-Lists)
7. [What we do with the data?](#What-Do-We-Do-With-The-Data)
8. [Acknolwedgements and further resources](#Acknolwedgements-and-Further-Resources)

## Introduction to Corpus Analysis and Antconc

Corpus analysis is a form of text analysis that allows us to compare textual objects “from a distance.” In many ways, corpus analysis is the opposite of a close reading. In a close reading, a small portion of text is looked at and evaluated at a minute level; in Classics, this often means paying special attention to the specific forms of words or meter. In sum, every bit of a small chunk of text is picked apart in detail. On the other hand, corpus analysis focuses instead on a much larger amount of text; for example, one author’s entire literary corpus. The focus here is instead on finding large-scale patterns, such as common grammatical usages or frequently used words. 

Corpus analysis is incredibly helpful in distinguishing patterns that the human eye might not pick up on, but that could raise important research questions about the text. However, corpus analysis is also a good way to confirm intuitions or gut instincts that we have about a text. For example, I took a course on Plato & Thucydides my first semester of grad school. We read Book 6 of Thucydides, in which the Athenians are debating whether or not to aid the Sicilians who have asked for their help. The book is presented as a series of speeches between Alcibiades and Nicias. One of my classmates asked whether or not the increased complexity of Nicias’ grammar and syntax was a reflection of his cautious and indecisive character. We read an article, written in the 70s, that argued exactly that (for those interested, the article is *Stylistic characterization in Thucydides: Nicias and Alcibiades* by Daniel Tompkins. While this article was published well before Digital Humanities became an established discipline, the author used many techniques that are now commonplace in Digital Humanities; in fact, Antconc would have been particularly useful for this kind of project.

Antconc is a standalone software package for the linguistic analysis of texts. It offers more features than a tool like Voyant, but is much simpler than coding in R or Python. It is free to download and use and runs on all operating systems (Windows, Mac OS, and Linux). The creator, Anthony Laurence, has done an excellent job of maintaining the software, making it a powerful tool for any level of experience.

## Tutorial Downloads

1. Software: Download Antconc from Laurence Anthony’s website [here](http://www.laurenceanthony.net/software/antconc/). It may be necessary to unzip the file. After the download is complete, launch the application. For reference, in this tutorial, I am using Antconc version 3.5.8 for Windows.
2. Corpus: We will be using a corpus I constructed made up of governing documents, primarily constitutions, from various countries. You can download the corpus [here](https://github.com/dnlawson/antconctutorial/files/4641428/AntConc.Documents.zip).

## Working with Plain Text Files

The first important thing to note about Antconc is that it will only work with plain-text files (.txt); this includes XML files that are saved as .txt files. This means that Antconc will not read .doc, .docx, or .pdf files - if you want to use data from these files, you will have to convert them to .txt files.

Plain-text editors include Notepad (on Windows; this is what I use) or TextEdit (on Mac). Other free text editor options with more advanced features include Notepad++ (Windows) and TextWrangler (Mac).

In order to construct a corpus, you would have to go to where your data is stored and then copy and paste it into a .txt file. This process would then have to be repeated for each file. Corpus construction is a time-consuming task and an art in its own right. We will be using a premade corpus consisting of the constitutions/governing documents of different countries. This is a corpus that I have constructed on my own; as such, it is not the cleanest data ever. If you are interested in cleaning data, please see Antconc's tutorial on data cleaning with OpenRefine [here](https://programminghistorian.org/en/lessons/cleaning-data-with-openrefine).

## The Antconc Interface

This is what Antconc looks like when it launches:

![interface](https://user-images.githubusercontent.com/57447342/81733316-a8de8b80-9446-11ea-9728-d61b6d0b6532.png)

## Loading Corpora

We want to open the documents that we will be evaluating. However, for this tutorial, rather than opening each file one by one, we want to open the entire directory. Click "File at the top of the interface:

![loadingcorpora2](https://user-images.githubusercontent.com/57447342/81733897-8e58e200-9447-11ea-9d08-096978f01ff3.png)

Next, click "Open Dir":

![loadingcorpora3](https://user-images.githubusercontent.com/57447342/81733905-9022a580-9447-11ea-9b28-5dd0c91c902f.png)

You can store the documents wherever on your computer you want (I usually keep mine in a Bryn Mawr folder), but I would recommend storing them on your Desktop for this tutorial. Navigate to desktop on the menu, click on the Antconc Documents folder, and then hit "OK". 

![opendir](https://user-images.githubusercontent.com/57447342/81733908-91ec6900-9447-11ea-92e9-c5d421de3a88.png)

This should load 16 files - you can see how many files have been opened in the "Total No." box at the bottom left of the interface.

![loadingcorpora](https://user-images.githubusercontent.com/57447342/81733890-8c8f1e80-9447-11ea-9961-e4ee90265963.png)

If you would like to only upload certain files (which there is certainly reason to do on occasion), follow the same directions but click on Open File rather than Open Dir. You will have to add each file individually.

## Applications: Word List

The word list is a simple, yet powerful tool. Navigate to the Word List tab on the top of the interface:

![wordlist1](https://user-images.githubusercontent.com/57447342/81733958-a6306600-9447-11ea-86fb-e987180aa88e.png)

Click "Start" at the bottom of the interface, underneath the search box, without entering a search term:

![wordlist2](https://user-images.githubusercontent.com/57447342/81733962-a7619300-9447-11ea-8d13-a16f94398bbb.png)

This will generate a list of every single word that appears in the corpus, along with the frequency of that word:

![wordlist3](https://user-images.githubusercontent.com/57447342/81733964-a892c000-9447-11ea-9240-af2259eb2876.png)

Unsurprisingly, words like "the", "of", and "a" are incredibly common. More substantive words appear further down the frequency list.

## Applications: Concordance

While the word list is a helpful first step, especially for gaining a broad overview, you may want to view the frequency and context of a specific word. The Concordance tool allows you to do this.

Make sure you have clicked the "Concordance" tab at the top of the interface.

In the search box at the bottom, type the word "shall" and hit "Start". This will show you **Key Words in Context (KWIC)**, that is every single time that a specific word appears, as well as a certain number of words on either side. 

![concordancew](https://user-images.githubusercontent.com/57447342/81733809-71bcaa00-9447-11ea-90f0-f6b2851b35ce.png)

Depending on the word you search for, the data may be overwhelming. It may be helpful to hit the sort button.

![concordancew2](https://user-images.githubusercontent.com/57447342/81733814-73866d80-9447-11ea-9848-1f100f9e8256.png)

This will sort the data alphabetically, if it isn’t already. If you want more or different information about the words surrounding your KWIC, you can change the parameters indicated below.

![concordancew3](https://user-images.githubusercontent.com/57447342/82173710-10e80400-9883-11ea-835d-87676b478614.png)

L means left and R means right, while the number indicates how many words to the left or right of your KWIC will be highlighted; the standard is 1L (first word to the left), 2R (second word to the right), 3R (third word to the right). This will list the data in alphabetical order by the first highlighted word (here, 1L). You can adjust as you need to. For example, you may want to go further to the left in order to capture specific phrases. If you don’t want any sorting data, you can leave it on the standard setting or set all three to 0. 

### Search Operators

Search operators offer more flexibility in searches for KWICs than the Concordance tool. For example, there are search operators to find the singular or plural form of a word or for finding all the words built off a certain stem rather than having to do individual searches for each word. To view all the possible search operators, go to "Global Settings" > "Wildcards".

![searchoperators1](https://user-images.githubusercontent.com/57447342/81733911-93b62c80-9447-11ea-96ce-47a75017dc3f.png)

![searchoperators2](https://user-images.githubusercontent.com/57447342/81733919-94e75980-9447-11ea-8f0d-36e4b720232e.png)

All of the search operators are a more specific application of the Concordance tool. We will talk about each of these more in depth.

#### The "Star" Operator (Wildcard)

The * operator, which finds zero or more characters, can be particularly helpful in finding both the singular and plural forms of a noun. 

In the Concordance tool, type "qualit*" into the search bar and hit "Start". Your results should look like this:

![searchoperators3](https://user-images.githubusercontent.com/57447342/81733925-96b11d00-9447-11ea-90ac-0543d4648f31.png)

Thus, we get the word "quality" (one character in addition to the stem qualit), but also "qualities" (three characters in addition to the stem qualit) and "qualitative" (five characters in addition to the stem qualit). These are each different words; as a result, they will be surrounded by different words, and used in different ways.

#### The "Question Mark" Operator

The "?" operator functions similarly to the * operator, but the "?" is more specific than * operator since the "?" operator only finds one character, rather than zero or more. For example, enter "m * n" in the search bar in the Concordance tool and hit "Start".  This search will give you these results:

![searchoperators4](https://user-images.githubusercontent.com/57447342/81733931-987ae080-9447-11ea-9362-d1a71f2c3955.png)

On the other hand, enter "m?n" into the search bar in Concordance tool and hit "Start". This search will give you these results:

![searchoperators5](https://user-images.githubusercontent.com/57447342/81733932-9a44a400-9447-11ea-8087-1c2bce48f508.png)

#### The "Plus" Operator:

The "+" operator finds zero or one character. Enter "me+" into the search bar in the Concordance tool and press "Start". Your results should look like this:

![searchoperators6](https://user-images.githubusercontent.com/57447342/81733934-9b75d100-9447-11ea-80f8-0687028237c3.png)

This search result finds all occurrences of "me" (zero characters) as well as any occurrences of "me" and one other letter (for example, "men", "met" etc).

#### The "At" Operator

The "@" operator allows you to account for words that may appear between two words that you are interested in. This is easiest to see in an example. You can put as many "@" operators as you like; however, if you put one, it will be equivalent to the "#" operator, which is in the next section. In this example, we will input the phrase "is@@president" in the Concordance tool and hit "Start". This will give us any phrases in the form of "is any word #1 any word #2 president". The output will look like this:

![searchoperators13](https://user-images.githubusercontent.com/57447342/82178007-e0f32d80-988f-11ea-91a1-0ecac89123d1.png)

#### The "Pound" Operator

The "#" operator functions like the "@" operator, but can only be used once. Enter "is#president" in the Concordance tool and hit "Start". The output will look like this:

![searchoperators14](https://user-images.githubusercontent.com/57447342/82178010-e2bcf100-988f-11ea-8908-234324dc76b3.png)

#### The "Or" Operator

Let’s say you wanted to find every instance of one or another word. You can use the “or” search operator, "|".  Let’s try "men" and "women". In the Concordances view, type "men|women" into the search box and press "Start". Your results should look like this:

![searchoperators7](https://user-images.githubusercontent.com/57447342/81733940-9d3f9480-9447-11ea-8e00-e5b3bdbb832e.png)

This shows you every occurence of either "men" or "women", a total of 75 (found at the top of the interface next to “Concordance Hits”). Now search for "men" and "women" separately; there are 27 instances of "men" and 48 of "women". This is rather counterintuitve, and an investigation into this phenomenon would make the beginnings of a great research question!

#### Combining Operators

Suppose you wanted to find all the instances of "man" or "woman" or "men" or "women". Good news: Antconc can do that by combining operators! Try entering "m?n|wom?n" into the search bar in the Concordances tool and pressing "Start". Your results should look like this:

![searchoperators8](https://user-images.githubusercontent.com/57447342/81733942-9e70c180-9447-11ea-9c6b-ab39ebe637bc.png)

You can mix and match search operators as needed.

#### Exporting Data from Search Operators 

Suppose that you found some really interesting results when you compared the words "man" and "woman" using one of the search operators and want to do further work with the data. You can export your results into a .txt file. First, make sure your data is sorted in a meaningful way that will be helpful, using the parameters talked about in the Applications: Concordance section above. Then click on "File":

![searchoperators9](https://user-images.githubusercontent.com/57447342/81733946-9fa1ee80-9447-11ea-8b81-80c3bd6a85b8.png)

Click on "Save Output":

![searchoperators12](https://user-images.githubusercontent.com/57447342/81733957-a4ff3900-9447-11ea-9019-b72d3d6e28f2.png)

It will save the results as antconc_results:

![searchoperators10](https://user-images.githubusercontent.com/57447342/81733947-a16bb200-9447-11ea-9e38-168d7a0a6419.png)

The file will then be saved as a .txt file, which opens up the door for further analysis!

![searchoperators11](https://user-images.githubusercontent.com/57447342/81733950-a29cdf00-9447-11ea-88cd-e9aeddcb231e.png)

### Stopword Lists

Suppose that you didn't want to see words like "a", "an", or "the" when looking at KWICs. Antconc allows you to create a stopword list. Antconc will remove any words on your stopword list from the search results. To create a stopword list, click on "Tool Preferences" at the top of the interface.

![stopwordlist1](https://user-images.githubusercontent.com/57447342/82180025-86a89b80-9894-11ea-8507-1ab6d1bc239f.png)

Then click on "Word List" at the left of the interface:

![stopwordlist2](https://user-images.githubusercontent.com/57447342/82180032-88725f00-9894-11ea-8070-315c331cee2d.png)

Under "Word List Range", click "Use stoplist below":

![stopwordlist3](https://user-images.githubusercontent.com/57447342/82180034-8a3c2280-9894-11ea-9173-a63d811c2cf2.png)

Type a word into the "Add Word" box; here, I used "the".

![stopwordlist4](https://user-images.githubusercontent.com/57447342/82180037-8b6d4f80-9894-11ea-87d2-3d3141c8021f.png)

Click "Add":

![stopwordlist5](https://user-images.githubusercontent.com/57447342/82180039-8dcfa980-9894-11ea-9916-e4c7f40749da.png)

The word will appear in the box:

![stopwordlist6](https://user-images.githubusercontent.com/57447342/82180043-8f00d680-9894-11ea-9b8f-81971503c071.png)

You will have to do this for each word on your stoplist. Once you have completed your list, click "Apply":

![stopwordlist7](https://user-images.githubusercontent.com/57447342/82180474-7513c380-9895-11ea-8074-665ce285cf0b.png)

It is important to think about whether or not a stopword list should be used. If you decide to use one, it is also important to think critically about what words should be put on your stopwrod list. If you are interested, [here](http://www.lextek.com/manuals/onix/stopwords2.html) an example, the Buckley-Salton Stoplist

## Applications: Concordance Plots

Concordance plots will calculate how often a word appears in each file from the directory and then output a graph showing each place that word appears in the document. Make sure you have clicked Concordance Plots at the top of the interface. Enter "law" in the search bar and hit "Start".

![concordanceplots](https://user-images.githubusercontent.com/57447342/82176133-b94d9680-988a-11ea-85de-751b7ea5cd09.png)

This tool tends to be more helpful for literature, particularly for tracking certain characters or phrases, although the visualizing measures certainly don't hurt in this study. The ability to visually see where certain words appear most frequently can reveal particularly fruitful places to focus your attention. This data can be exported following the steps outlined in the Exporting Data from Search Operators section above, although it exports as a .ps file.

## Applications: File View

File view shows the text of individual files. This allows for closer examination of the results obtained from other tools. Choose File View from the tabs at the top of the interface. Click on a file from the left hand side of the interface. First, hit start with no search term entered. This will display the text of that specific file:

![fileview1](https://user-images.githubusercontent.com/57447342/81733827-7719f480-9447-11ea-998f-281c77fae478.png)

Next, enter a search term in the search box and hit start. This will show you the search term in context within the file:

![fileview2](https://user-images.githubusercontent.com/57447342/81733830-78e3b800-9447-11ea-88d4-6aacd4fed5ea.png)

You can navigate to the next appearance of the search term using the hit location tab:

![fileview3](https://user-images.githubusercontent.com/57447342/81733837-7aad7b80-9447-11ea-9b51-6e725123b0a4.png)

File view allows for more detail and contextualization than is afforded by, for example, the Concordance tool.

## Applications: Clusters/N-Grams

The "clusters" view shows words that frequently appear together. For example, say we wanted to know what words commonly appear with the word shall. Make sure you click Clusters/N-Grams tab at the top of the interface. Enter shall into the search box and hit start.

![clusters](https://user-images.githubusercontent.com/57447342/81733685-46d25600-9447-11ea-9616-c0aac990dd81.png)

If you want to view more than pairs of words, you can choose to look at N-Grams, which refer to clusters that are of length n. First, check that the N-Grams box at the bottom of the interface is checked:

![clusters2](https://user-images.githubusercontent.com/57447342/81733688-4934b000-9447-11ea-989e-9f97ec86bbc8.png)

You can then choose how long you want your N-Gram to be by adjusting the N-Gram size, also at the bottom of the screen:

![clusters3](https://user-images.githubusercontent.com/57447342/81733692-4b970a00-9447-11ea-9ce3-b2cb5aa8ec64.png)

Hit start (Antconc will not allow you to enter a search term). Depending on how large your corpus is, this process can take awhile. Your results should look like this:

![clusters4](https://user-images.githubusercontent.com/57447342/81733700-4d60cd80-9447-11ea-98bb-e00672a7d2b9.png)

The primary difference between clusters and N-Grams, besides the variable length, is that clusters take a specific search term, while N-Grams do not take a search term and instead return any string of words of the length you requested.

## Applications: Collocates

Clusters and collocates may seem to be the same thing. They are, indeed, very similar; however, clusters show words that definitely appear together, while collocates shows words that are statistically likely to appear next to one another.

The collocates view gives you a list of the words that are most likely to appear with your keyword. Click Collocates at the top of the interface. Enter "shall" and hit "Start". Antconc will tell you that you need to generate a word list first. We generated one earlier in this tutorial, so Antconc will automatically use that one. However, if you are using Antconc and didn't generate a word list first, hit okay and it will generate one for you.

![collocates1](https://user-images.githubusercontent.com/57447342/81733710-4f2a9100-9447-11ea-91c5-8c11a4f352ba.png)

![collocates2](https://user-images.githubusercontent.com/57447342/81733715-518ceb00-9447-11ea-883d-cc2d38f3c4fb.png)

Like concordance, you can decide what parameters you want your data sorted by. 

![collocates3](https://user-images.githubusercontent.com/57447342/81733721-5356ae80-9447-11ea-94a3-9559deefb1dd.png)

You can sort by "word", which alphabetizes the list of words; by "word end", which alphabetizes the list of words by the last letter of the word; by "freq", which orders the list by the total number of times the word occurs; "freq(L") and "freq(R)", which orders the list of words by how often the word appears to the left of and to the right of the keyword respectively; and by "stat", which "measures how 'related' the search term and the collocate are" (definition from page 6 of Laurence' Anthony's [readme file](http://www.laurenceanthony.net/software/antconc/releases/AntConc335/help.pdf).

## Applications: Keyword Lists

The keyword list is arguably Antconc’s most powerful and important function because it allows one corpus to be compared to a larger, reference corpus. It is also by far the most complex tool that Antconc offers. 

It is important to think about what your research corpus should or could look like. In this example, we will compare American documents with non-American documents. Other examples could include comparing different geographical areas or comparing the governing documents of one ocuntry across time. Once again, it is important to remember that corpus construction is a sub-field in its own right, and it is worthwhile to think about how and why we construct and define corpora in certain ways. 

First, we will add our reference corpus. Select "Tool Preferences" at the top of your screen.

![keywordlist1](https://user-images.githubusercontent.com/57447342/81733839-7c773f00-9447-11ea-8369-c2b8e5b5ced9.png)

Click on "Keyword List" in the left-hand column.

![keywordlists2](https://user-images.githubusercontent.com/57447342/81733842-7e410280-9447-11ea-81c2-bc9fe30cdefe.png)

Click "Add File".

![keywordlists3](https://user-images.githubusercontent.com/57447342/81733850-800ac600-9447-11ea-84b4-dcc13bb0a126.png)

Navigate to your desktop and select the file you would like to open and then click "Open". For this example, let’s load the first non-American file, canadianconstitution.

![keywordlists4](https://user-images.githubusercontent.com/57447342/81733853-813bf300-9447-11ea-8a53-a57b0f14e27d.png)

We will have to do this for each file in our reference corpus. After you have loaded all your files, check the total number to ensure that you have all your files. In this example, we started with sixteen documents. Since we have to add our research corpus (the Constitution and Declaration of Independence) separately, we would expect fourteen documents here, which we have. These will constitute our larger, reference corpus. Click "Load".

![keywordlists5](https://user-images.githubusercontent.com/57447342/81733856-826d2000-9447-11ea-8ff5-b66dca535edd.png)

Hit "Apply".

![keywordlists6](https://user-images.githubusercontent.com/57447342/81733861-8436e380-9447-11ea-9fc7-2e9aeddeed20.png)

These documents will not show up on the left side of the interface like they would if we loaded them as we did earlier in this tutorial - that’s normal.
Next, make sure to load the American corpus like we did at the beginning. After hitting "Apply" and loading the American corpus, your interface should look like this.

![keywordlists7](https://user-images.githubusercontent.com/57447342/81733866-85681080-9447-11ea-9f42-8055f9bb1b4f.png)

Now hit the "Start" button one more time. Your results should look like this:

![keywordlists8](https://user-images.githubusercontent.com/57447342/81733870-8731d400-9447-11ea-8352-0bb9332dd029.png)

In simple terms, this is a list of words that appears more in your research corpus than in the corpora it is being compared to, that is words that are statistically more unexpected in your corpus when compared with the reference. Antconc establishes the statistical significance by using a concept called “keyness.” Keyness is “the frequency of a word in the text when compared with its frequency in a reference corpus, ‘such that the statistical probability as computed by an appropriate procedure is smaller than or equal to a p value specified by the user’” (definition from the Programming Historian). The automatic Antconc setting is that words with a p-value less than or equal to 0.05 will be displayed, which is the norm for establishing statistical significance; however, if you want, you can change the p-value in "Tool Preferences" > "Keyword List", along with other statistical elements like stastic threshold, effect size meansure, and effect size threshold.

![keywordlists9](https://user-images.githubusercontent.com/57447342/81733882-8ac55b00-9447-11ea-895e-e457e5d20ef1.png)

I'm not a staistician, so if you are interested in how Antconc uses statistics for this function, you can read more in the section on keyness on page 7 in Laurence Anthony’s [readme file](http://www.laurenceanthony.net/software/antconc/releases/AntConc335/help.pdf).

## What do we do with the data?

As with many Digital Humanities projects, the most important question is what to do with the data once you have it. While computers are very good at identifying patterns and analyzing data, it is ultimately people that formulate the research questions, draw conclusions from the data, and make arguments about what it means. As such, it is worthwhile to think about how we use this data in order to make meaningful comparisons and ask useful questions.

First, as mentioned earlier, it is important to ensure that corpora are representative. While corpus construction is not the most enjoyable task, ensuring that a corpus is representative is key to gaining meaningful results. It is beyond the scope of this tutorial to talk about how to construct a representative corpus, but if you are interested see [here](https://academic.oup.com/dsh/article-abstract/8/4/243/928942) and [here](https://www.amazon.com/Developing-Linguistic-Corpora-Practice-Guides/dp/1842172050/ref=sr_1_1)(thank you to the Programming Historian for the references!). 

Second, do not discount minor words. Words like "a", "an", and "the" are some of the most common in the English language. As such, they tend to be overrepresented in topic modeling ("an unsupervised machine learning technique that’s capable of scanning a set of documents, detecting word and phrase patterns within them, and automatically clustering word groups and similar expressions that best characterize a set of documents" - definition from [here](https://monkeylearn.com/blog/introduction-to-topic-modeling/)). While such words may seem unimportant on the surface, the differences between a definite and an indefinite article or places where "not" is used may prove illuminating, and computers are very good at picking up patterns, especially high frequency patterns that might overwhelm someone attempting to track them by hand. However, it is possible to create a stopword list if necessary, although it is not advisable simply to discount minor words because of their perceived unimportance. Computers are very good at picking up patterns, especially high frequency patterns that might overwhelm someone attempting to track them by hand. 

Third, as in any research project, it is essential to ask what kinds of questions are meaningful based on the data and results. This may include thinking about why two corpora can or should be compared (for example, geographically? temporally?) or investigating peculiarities that arise from the data (for example, why the word "women" appears more often than the word "men"). At the end of the day, Antconc is only as powerful as the questions you ask about the data!

In sum, it is important to think about:
* Why two corpora should be compared
* Ensuring representative corpora
* Methodology, especially with respect to stopwords
* What kinds of questions are meaningful based on the data

## Acknolwedgements and Further Resources

I would like to thank the following people/organizations for releasing free tutorials and resources for Antconc, which I used both to learn this software and to structure and create my own tutorial:

* This [Programming Historian tutorial](https://programminghistorian.org/en/lessons/corpus-analysis-with-antconc) was how I learned to use Antconc and was my primary resource in structuring and writing my own tutorial. It is a good, fairly in-depth overview of Antconc with lots of extra activities throughout.
* Laurence Anthony also has a basic tutorial [here](http://www.laurenceanthony.net/software/antconc/resources/help_AntConc321_english.pdf), as well as a more complex and detailed tutorial [here](http://www.laurenceanthony.net/software/antconc/releases/AntConc335/help.pdf)
* If videos are more your style, Laurence Anthony also has a playlist of video tutorials on YouTube [here](https://www.youtube.com/playlist?list=PLx4CiNE_oyfPp9uVMmbByd-ncdN2aUDu8)
* If you need a simple, easy to read cheat sheet, [this tutorial](https://wmtang.org/corpus-linguistics/antconc-tutorial/) will be helpful



