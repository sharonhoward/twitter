# Digital History Twitter Hashtag Archives: Tweet ID Datasets

Between 2011 and 2016 I archived a range of Twitter hashtags of interest to historians. I have now discontinued archiving activity because I don't have time to maintain it properly, and Twitter's search facilities have substantially improved since the early days. 

This repository contains the tweet ID data for selected archives, in accordance with [Twitter's rules for sharing their data](https://dev.twitter.com/overview/terms/agreement-and-policy#f-be-a-good-partner-to-twitter) (see notes on licensing below) and the ethical guidelines outlined by [DocNow](http://www.docnow.io/). 

To reconstruct the full data from the bare IDs you will need to use the [Twitter API](https://dev.twitter.com/overview/api) or a specialised tool such as [DocNow's](http://www.docnow.io/)  [Hydrator](https://github.com/DocNow/hydrator) or [twarc](https://github.com/docnow/twarc).

## Datasets

Unless otherwise stated, each dataset consists of two data fields:

*   tweet_id: the unique ID of the tweet itself (id_str in the Twitter API)
*   user_id: the user ID (user_id_str)
   
The archived data was in all cases collected via the Twitter Search API (normally at 30 minute intervals, and more frequently if necessary). There may be small gaps but the method proved generally reliable over several years.

### #twitterstorians (October 2011 - October 2016)

The #twitterstorians hashtag was the brainchild of Katrina Gulliver. It has been used for a wide range of purposes by historians including publicity, asking questions, and general networking.

* twitterIDs_twitterstorians.csv (613169 tweets)

### American Historical Association Meetings 2012-2016

In each case the tweets archived include both the "long" hashtag (eg #AHA2016) and shorter form (#AHA16). They may also include other hashtags that were in common use at that meeting (eg #thatcampaha).

In most cases, the archives include tweets dating from some months before and after the conference itself. I have done some cleaning but they are likely to include various irrelevant tweets ('AHA' is a remarkably popular acronym/abbreviation, not least for a certain Scandinavian pop music band).

* twitterIDs_AHA2012.csv (4900 tweets)
* twitterIDs_AHA2013.csv (5401 tweets)
* twitterIDs_AHA2014.csv (9325 tweets)
* twitterIDs_AHA2015.csv (23910 tweets)
* twitterIDs_AHA2016.csv (16606 tweets)

### #earlymodern (July 2012 - October 2016)

* twitterIDs_earlymodern.csv (64280 tweets)

### #ozhst (July 2012 - October 2016)

A hashtag for Australian history (may also include #ozhist)

* twitterIDs_ozhst.csv (16845  tweets)

### Australian History Association conferences 2012-2016

* twitterIDs_ozha2012.csv (1112 tweets)
* twitterIDs_ozha2013.csv (817 tweets)
* twitterIDs_ozha2014.csv (679 tweets)
* twitterIDs_ozha2015.csv (2884 tweets)
* twitterIDs_ozha2016.csv (374 tweets)

### Future Additions

To include:
* #dhist and #digitalhistory
* #histsci and #histstm

## Licensing

I'm not releasing this data under a standard CC/open licence, because of the restrictions Twitter places on redistribution of data obtained using their API. Any re-use of data derived from the IDs should comply with the Twitter policy, and the following represents a guide to the conditions of re-use.

The Twitter rules say this:

> If you provide Content to third parties, including downloadable datasets of Content or an API that returns Content, **you will only distribute or allow download of Tweet IDs and/or User IDs**...

and

> **Any Content provided to third parties via non-automated file download remains subject to this Policy.**

I take the wording to mean that:

* you may use the IDs data to create new datasets containing further elements of tweets' content/metadata, in accordance with any terms and conditions imposed by the tools you use to extract the data, for your own use
* you may publish quantitative analyses and datavizes of the new datasets or small amounts of the additional tweet content/metadata to illustrate qualitative analyses and narratives, as well as descriptions of the methods and tools you used to collect the fuller data from the IDs 
* you may redistribute or archive copies of the bare tweet IDs data in any way you wish
* but you **may not** share or re-publish the derived datasets containing additional tweet content/metadata

Acknowledgment of the source of the Tweet IDs data would be much appreciated!