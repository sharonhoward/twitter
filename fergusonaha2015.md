Notes on FergusonAHA2015 data files
========================

At the 2015 American Historical Association Annual Meeting a special panel session was held on [Understanding Ferguson: Race, Power, Protest, and the Past](https://aha.confex.com/aha/2015/webprogram/Session12609.html).

This dataset consists of tweets containing **ferguson** in all [archived tweets from the conerence](http://thebroadside.org/tw-archives/index.php?archive=AHA2015) (at 11/1/2015). This includes the 'official' conference panel hashtag #FergusonAHA (~1100 tweets), but I decided it might be useful to try to include tweets from/around the conference activity that did not use the hashtag. (I did not check whether any tweets contain non-relevant uses of the word - I'm afraid you'll have to do that for yourself!)

* fergusonAHA2015.sql and fergusonAHA2015.tsv contain the same data in alternate formats.

Most of the fieldnames follow the terminology used in the [Twitter search API](https://dev.twitter.com/rest/reference/get/search/tweets) itself:

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

(You can get more info about all these from the Twitter API documentation.)

The following are derived from the API but in a much simplified form:

* *rts* - is it a Twitter RT? 1 = yes (can be used to distinguish Twitter RTs from manual RTs, if you have any wish to do so)
* *entities_hashtags_text* - all the hashtags in the body of the text, separated by || 

Please note that one piece of information not included is **geo** coordinates. Sorry if you were hoping for that, but I don't archive it.

Sharon Howard @sharon_howard
11 January 2015