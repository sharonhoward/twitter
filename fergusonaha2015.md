Notes on FergusonAHA2015 data files
========================

At the 2015 American Historical Association Annual Meeting a special panel session was held on [Understanding Ferguson: Race, Power, Protest, and the Past](https://aha.confex.com/aha/2015/webprogram/Session12609.html).

This dataset consists of tweets containing **ferguson** in all [archived tweets from the conerence](http://thebroadside.org/tw-archives/index.php?archive=AHA2015) (at 11/1/2015). This includes the 'official' panel hashtag #FergusonAHA (~1100 tweets), but there were significant numbers of tweets from/around the conference activity that did not use the hashtag so I opted for a more expansive query. However, I did not check whether any tweets contain non-relevant uses of the word - I'm afraid you'll have to do that for yourself!

The data
--------

* There are two files: fergusonAHA2015.sql and fergusonAHA2015.tsv (the same data in alternate formats)
* Number of tweets: 1415

Most of the field names follow the terminology used in the [Twitter search API](https://dev.twitter.com/rest/reference/get/search/tweets) itself:

* *id_str* - the ID of the tweet
* *created_at* - the tweet's timestamp
* *user_screen_name* - the tweeter's @username (can change)
* *user_id_str* - the tweeter's ID (permanent)
* *user_name* - the tweeter's 'nice' display name (can change)
* *user_profile_image_url* - the url for the tweeter's profile image (can change)
* *text* - the body of the tweet (any emojis have been stripped)
* *source* - the app or site used to send the tweet ('web' means twitter.com)
* *iso_language_code* - 2 letter code for the language of the tweet
* *in_reply_to_user_id_str* - if the tweet is a @reply this is the ID of the tweeter replied to
* *in_reply_to_status_id_str* - the ID of the tweet replied to
* *in_reply_to_screen_name* - the username of the tweeter replied to

The following are derived from the API but in a much simplified form:

* *rts* - is it a Twitter RT? 1 = yes (can be used to distinguish Twitter RTs from manual RTs, if you have any wish to do so)
* *entities_hashtags_text* - all the hashtags in the body of the text, separated by || 

Please note that one piece of information not included is **geo** coordinates, which I don't archive (but probably should...). In fact, there is far, far more metadata available through the API than I actually collect. If you know how to work with APIs (or are willing to learn!) and you need elements of the data I don't include (such as the geo data), you should be able to use *id_str* (for tweets) and *user_id_str* (for tweeters) to retrieve anything you want. The API documentation can be found [here](https://dev.twitter.com/rest/public). In particular you might want to read the documentation on [GET statuses/lookup](https://dev.twitter.com/rest/reference/get/statuses/lookup).



Background on tweet archiving 
---------------------

The data collection method uses bespoke PHP scripts and a MySQL database to fetch tweets from the Twitter search API, automated with cron jobs. It is a generally reliable method I've been using for some years (its main limitation, of course is the crude nature of any hashtag/keyword search). 

For this archive, I collected tweets containing the hashtags #AHA2015 or #AHA15 from several months before the conference began (and will continue archiving for a couple of months afterwards). I did not know of the Ferguson panel and hashtag until after the conference had begun, at which point I added #FergusonAHA to the data collection to ensure capture of tweets that didn't also have the main conference hashtag. 

During the conference tweets were collected every few minutes at busy periods to avoid missing data, and I also ran scripts retrospectively to fill a few known gaps resulting from technical problems, and to catch up the Ferguson tweets I'd missed. 


**Sharon Howard** (@sharon_howard)

11 January 2015