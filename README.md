# Text analysis : Selected works by Benito Pérez Galdós \[Sample project\]  
**NOTE:** For sample projects in this GitHub account, the objective is not to have a fully-formed research question, valid sample, and methodology. The main objective is to showcase my learning about different tools used for digital scholarship.

In this project, I created a small corpus of works by [Benito Pérez Galdós](https://en.wikipedia.org/wiki/Benito_P%C3%A9rez_Gald%C3%B3s) and did some basic text analysis. I was especially interested in how a tool designed by and for text analysis in an English-speaking context would handle texts in another language (Spanish). Only basic data cleanup was done for this project.
## Tools  
### [Project Gutenberg](https://www.gutenberg.org/)  
Used to obtain plain text versions of selected works by Spanish author Benito Pérez Galdós:  
- [El 19 de marzo y el 2 de mayo](https://www.gutenberg.org/cache/epub/67189/pg67189.txt)
- [El amigo Manso](https://www.gutenberg.org/files/55563/55563-0.txt)
- [El abuelo](https://www.gutenberg.org/cache/epub/66488/pg66488.txt)
- [El caballero encantado](https://www.gutenberg.org/cache/epub/67126/pg67126.txt)
- [Cádiz](https://www.gutenberg.org/cache/epub/21906/pg21906.txt)
- [La corte de Carlos IV](https://www.gutenberg.org/cache/epub/67155/pg67155.txt)
- [Doña Perfecta](https://www.gutenberg.org/cache/epub/15725/pg15725.txt)
- [La fontana de oro](https://www.gutenberg.org/cache/epub/11070/pg11070.txt)
- [Fortunata y Jacinta](https://www.gutenberg.org/cache/epub/17013/pg17013.txt)
- [Marianela](https://www.gutenberg.org/cache/epub/17340/pg17340.txt)
- [La novela en el tranvía](https://www.gutenberg.org/cache/epub/53355/pg53355.txt)
- [Zaragoza](https://www.gutenberg.org/files/49433/49433-0.txt)

### Notepad++  
Given the small nature of this corpus and the relatively regular structure of the text files, basic regular expressions were used to clean up unwanted portions of the texts (such as bibliographic data and Project Gutenberg's license information).  

Sample regular expresion (to remove Project Gutenberg's license information from the text):  
```
Find what: \*{3}\sEND OF THE PROJECT GUTENBERG.*
Replace with:
```

Additional manual cleanup was required for data that did not follow predictable patterns.

### [Voyant Tools](https://voyant-tools.org/)
Used for data visualization and text analysis.

## Data
### Files
- bpg-cleaned-up-corpus.zip : 12 plain text files with the cleaned-up version of the works listed above
- bpg-stopwords.txt : list of [stopwords](https://voyant-tools.org/docs/#!/guide/stopwords) that were added to the out-of-the-box list for Spanish terms. The word selection was somewhat arbitrary, primarily intended to test the stopwords functionality in Voyant
- bpg-concordance.csv : concordance view for the word *casa* (house), which is one of the high-frequency terms in this corpus

## Text analysis: image examples
Image 01. Word cloud generated from word-frequency counts across the entire corpus :  
![bpg-word-frequency](https://user-images.githubusercontent.com/102780927/162101648-a8fdf724-f37b-4fe0-b823-35df9c3c77c3.png)

Image 02. *Amor y odio* (love and hate) relative frequency across all texts :  
![bpg-love-hate](https://user-images.githubusercontent.com/102780927/162102275-65d5b265-50b3-401c-98a7-e62fb54a77b0.png)

Image 03. *Miedo y esperanza* (fear and hope) relative frequency across all texts :
![bpg-fear-hope](https://user-images.githubusercontent.com/102780927/162102331-5ae12ac5-4949-4301-9ee3-a0bef5c8b4d3.png)
