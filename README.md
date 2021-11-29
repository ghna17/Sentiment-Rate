# Sentiment-Rate
Automated Sentiment Analysis
Sentiment analysis is the process of reading some text and determining the author's feelings (positive or negative) toward the subject on which they are writing. For example, consider the following two film reviews:
• It almost feels as if the movie is more interested in entertaining itself than in amusing us.
• A positively thrilling combination of ethnography and all the intrigue, betrayal, deceit and murder of a Shakespearean tragedy or a juicy soap opera
It is pretty clear to us as human readers that the first review expresses a negative sentiment while the second one expresses a positive sentiment. The task then for automated sentiment analysis is to write a computer
program that takes a piece of text and determines if that string is expressing a positive or negative sentiment.

While this might sound like a daunting task, there is a relatively clever way to do it if we have a large data set with words that have a known sentiment somehow already attached to them. As it turns out, there are lots and
lots of such data sets. In fact, every review site on the Internet is one:
• "5 stars: Loved it!"
• "0 stars: Absolutely pathetic!"

The basic idea then is that these reviews can be used to associate a positive sentiment ("5 stars") with the words "Loved" and "it" and a negative sentiment ("0 stars") with the words "Absolutely" and "pathetic". We'll get
more into exactly how it will work below. 

The Data Set
The data set that we will use to assign sentiments is based on movie reviews and is from real movie reviews posted at Rotten Tomatoes (https://www.rottentomatoes.com/). This data set was originally produced for a
Kaggle machine learning competition (https://www.kaggle.com/c/sentiment-analysis-on-moviereviews/overview) and has since been adapted for a similar assignment by Eric D. Manley and Timothy M.
Urness at Drake University. It is their data set that we are using. The data set has been broken into two pieces. One set we will use as training data to assign sentiments to
words in our sentiment analysis program. The other we will use as validation data to see how good our program does at figuring out the sentiment of a review. The training data set is stored in a file named
training.txt and the validation data is stored in a file named validation.txt. Both of the files have the same format but contain different reviews. 

Open the training.txt file. Each line in the file has two parts. The first part is a single number indicating the rating given by the reviewer. The second part is the text of the review, explaining what was good or bad about the film. 
• 4 is the highest rating in the training.txt file.
4 One of recent memory's most thoughtful films about art, ethics, and the cost of moral compromise.
• 0 is the lowest rating.
0 Analyze That is one of those crass, contrived sequels that not only fails on its own, but makes you second-guess your affection for the original.
