# <i>h</i>MDS Corpus Construction Guidelines 

In the following, you can find the guidelines which were provided to the annotators to guide their work. The 12 individual steps are accompanied by the topic "Luc Bourdon" (https://en.wikipedia.org/wiki/Luc_Bourdon) as an example. The example was also provided to the annotators. The authors of the paper provided the annotators with Wikipedia featured article URLs (which we call "topics") coming from 3 different domains:

* Domain 1: https://en.wikipedia.org/wiki/Wikipedia:Featured_articles#Art.2C_architecture.2C_and_archaeology
* Domain 2: https://en.wikipedia.org/wiki/Wikipedia:Featured_articles#History
* Domain 3: https://en.wikipedia.org/wiki/Wikipedia:Featured_articles#Law + https://en.wikipedia.org/wiki/Wikipedia:Featured_articles#Politics_and_government 

Identifiers for topics use a combination of running numbers for topics (e.g. T01, T02, ...) and domains (D01, D02, D03). D02T07 is short for Topic 7 of Domain 2.

### 1. Create new folder for new topic D02T07_Luc_Boudon


### 2. Extract plain text of lead (first paragraph) of the Wikipedia article and store it in text file Luc_Bourdon.txt.
Example of file *Luc_Bourdon.txt*:
```
Joseph Luc Bourdon (February 16, 1987 – May 29, 2008) was a Canadian professional ice hockey defenceman who played for the Vancouver Canucks of the National Hockey League (NHL) and their American Hockey League (AHL) affiliate, the Manitoba Moose, from 2006 until 2008. After overcoming childhood arthritis, he was selected third overall in the 2003 Quebec Major Junior Hockey League (QMJHL) draft and played for the Val-d'Or Foreurs, Moncton Wildcats, and Cape Breton Screaming Eagles, spending four seasons in the QMJHL. The Canucks drafted Bourdon with their first selection, tenth overall, in the 2005 NHL Entry Draft. Noted as a strong defenceman who could contribute on offence, Bourdon represented Canada in three international tournaments, winning two gold medals at the IIHF World U20 Championship and a silver medal at the IIHF World U18 Championship. Bourdon died at the age of 21 near his hometown of Shippagan, New Brunswick, when his motorcycle collided with a tractor trailer.
```

### 3. Store the URL of the article with the version id below the extracted lead text, in a new line. The version id can be retrieved by clicking on "View History" in the upper right corner of the article and then by clicking on the most recent date displayed in the table.
Example of file *Luc_Bourdon.txt*:
```
Joseph Luc Bourdon (February 16, 1987 – May 29, 2008) was a Canadian professional ice hockey defenceman who played for the Vancouver Canucks of the National Hockey League (NHL) and their American Hockey League (AHL) affiliate, the Manitoba Moose, from 2006 until 2008. After overcoming childhood arthritis, he was selected third overall in the 2003 Quebec Major Junior Hockey League (QMJHL) draft and played for the Val-d'Or Foreurs, Moncton Wildcats, and Cape Breton Screaming Eagles, spending four seasons in the QMJHL. The Canucks drafted Bourdon with their first selection, tenth overall, in the 2005 NHL Entry Draft. Noted as a strong defenceman who could contribute on offence, Bourdon represented Canada in three international tournaments, winning two gold medals at the IIHF World U20 Championship and a silver medal at the IIHF World U18 Championship. Bourdon died at the age of 21 near his hometown of Shippagan, New Brunswick, when his motorcycle collided with a tractor trailer.
https://en.wikipedia.org/w/index.php?title=Luc_Bourdon&oldid=705822268
```

### 4. Extract the most important information nuggets from this text (between 10  and 20 nuggets) and store them in text file Luc_Bourdon_nuggets.txt. One nugget per line. Remove all irrelevant words like "was a" in the nugget "was a Canadian". The information nuggets should be atomic information, i.e. omitting one word would change the meaning significantly. Enumerate the lines.

Example of file *Luc_Bourdon_nuggets.txt*:
```
1:Joseph Luc Bourdon
2:February 16, 1987
3:May 29, 2008
4:Canadian
5:professional ice hockey defenceman
6:Vancouver Canucks
7:Manitoba Moose
8:from 2006 until 2008
9:childhood arthritis
...
15:died at the age of 21
16:near his hometown of Shippagan
17:motorcycle
18:tractor trailer
```

### 5. Use a web search engine (e.g. Google or Bing, log off from your account before) to search for 
1. the topic itself - you can use quotes "..." if necessary, then select one source.
2. each information nugget (in quotes "..." if necessary), then select one source that contains the information nugget. In most cases the nugget needs to be combined with the topic, in order to add context. For example, the nugget "Canadian" needs to be combined with the topic "Luc Bourdon". One source for each information nugget is sufficient. 

Within the first 10 minutes: decide if it is necessary to move on to the next topic, i.e. if you have the impression that you will not find enough sources.

The sources should: 
* include as many of the different text types (see below) as possible, e.g. mainly not be "news"
* not be too similar with the Wikipedia article, that means:
  * source should not contain all the information nuggets from the Wikipedia article
  * source should contain content that is unrelated to the topic
* be written in English
* not have too low writing quality (e.g. full of typos, grammar errors)
* nice to have, but not necessary: freely available (e.g. Creative Commons license)
* not be PDFs
* not Google books (because we can not assign a stable ID)
* It is allowed to select sources that are listed as references in the Wikipedia article itself

Main criteria to judge the suitability of a source:
* can be archived in Web archive
* plain text can be extracted


### 6. Goto http://archive.org/web and store one web page for each information nugget. Store the retrieved link in a text file. Create one file per source. Enumerate the files (e.g. "01.txt", "02.txt", ...). Add the index of the matched information nugget to the line. Separate the index and the URL with a colon (":").

The example below matches nugget 4, i.e. is the content of file "04.txt":
```
4:http://web.archive.org/web/20160225201940/http://www.urbandictionary.com/define.php?term=luc+bourdon 
```

### 7. Store the nugget matching text below the URL, in a new line. 
Example of file "04.txt":
```
4:http://web.archive.org/web/20160225201940/http://www.urbandictionary.com/define.php?term=luc+bourdon 
Canadian
```

### 8. Store the type of the source (format: "id:type") below the matching text.
Possible types are:
1: article, e.g. news/high quality (blog) article (e.g. bbc.com, spiegel.de, ... )
2: forum post, e.g. blog/forum post (e.g., reddit, ), question answering site (e.g. quora, stackoverflow), youtube comments (low quality due to missing context)
3: twitter: very short, including possibly other microblogs
4: organization, e.g. announcements (company, NHL, ...), press releases, and other texts which have been written with the purpose of advertisement, also including commercial descriptions, e.g. for a book or a picture
5: encyclopedic short, e.g.  urban dictionary, duden, IMDB database, statistic sources
6: encyclopedic long, e.g. wiki (Wikipedia, wiki.ubuntu.com, ...), legislative text
7: social media, e.g. facebook, google+
8: scientific, e.g. scientific articles (containing citations and a bibliography), book reviews
9: education, e.g. tutorial, text book
10: dialogues, e.g. interviews, transcripts, discussions, texts with opinions from different persons (e.g. Merkel says X, Obama says Y, Putin says Z)

Example of file "04.txt":
```
4:http://web.archive.org/web/20160225201940/http://www.urbandictionary.com/define.php?term=luc+bourdon 
Canadian
5:encyclopedic
```

### 9. Extract and store metadata (each in a new line, below the text type)
* Title (if available), e.g. of the web page or of the article; otherwise: unknown
* License (only if clearly visible); otherwise: unknown

Example of file "04.txt":
```
4:http://web.archive.org/web/20160225201940/http://www.urbandictionary.com/define.php?term=luc+bourdon 
Canadian
5:encyclopedic
luc bourdon
unknown
```

### 10. Extract the relevant plain text from the web page. Do not include boilerplate text such as navigation links, ads, etc. Store it below the text type.
How to handle long source documents:
* Books: extract the surrounding chapter
* Maximum amount of text to be extracted as plain text: there is no fixed maximum, instead: use the corresponding "unit" of the source

Example of file "04.txt":
```
4:http://web.archive.org/web/20160225201940/http://www.urbandictionary.com/define.php?term=luc+bourdon 
Canadian
5:encyclopedic
luc bourdon
unknown

Top Definition
luc bourdon
Luc Bourdon was a Canadian professional ice hockey defenceman who played for the Vancouver Canucks of the NHL and the Manitoba Moose of the AHL.
Bourdon died in a motorcycle accident in Lamèque, New Brunswick, near his hometown of Shippagan, on May 29, 2008 when he hit a tractor-trailer after losing control of his bike and crossing the center line.
Hockey fan #1: Luc Bourdon had so much potential and a bright career ahead of him..
Hockey fan #2: RIP Luc Bourdon #28
by canucklove May 29, 2008
```

### 11. Store the folder "D02T07_Luc_Boudon" with all files in the repository.

### 12. Mark topic in the list as done (or as skipped).



# Q&A Section on Specific Cases

### Distinguishing between the predefined types of sources

Q: Does the category "forum post" mainly refer to low quality sources? Because there are also high quality forum/blog posts that were posted by experts.

A: A good indicator to differentiate between "forum post" and "article" is the length of the text. An article has an introduction and is a text on its own. "Forum posts" do not have an introduction and they are often a reply to a question or other forum posts. So they are texts which have a context (the surrounding posts) and are harder to understand without this context. Furthermore, an article is probably more trustworthy than a forum post. However, forum posts can contain very useful information. For example, a correct reply to a question on a platform like quora can be a very good source of information.

### When does an information nugget occur in a source document?

Q: Should the source contain the information nugget exactly, without any variation?

A: sources where the nugget occurs verbatim should be preferred. However, variants that can be recognized by common linguistic preprocessing components are allowed. This includes the following variants:
* Different word order, for example, in active vs passive constructions: e.g., the information nugget ''painted by Rogier van der Weyden'' can also occur as a construction in the active voice: "Rogier van der Weyden painted" (it)
* Inflected forms of the same word: a lemmatizer can be used to detect such cases
* Variants of proper names: these can be recognized by state-of-the-art entity-linking systems. Example: the nugget contains "Senator John W. Bicker" and in the source "Sen. John W. Bicker" is used
* Variants where hyphenation is used: can be detected by a lemmatizer. Examples: "nine stacked platforms" vs. "nine-stacked platforms", "14-th century" vs. "14th century".

The following variant should not be considered as occurrences of an information nugget:
* In the source, different words with the same meaning are used (i.e. synonyms). This would require a word sense disambiguation component, but the currently available components are restricted both regarding robustness (they depend on limited lexical resources) and performance.
