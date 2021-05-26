# Description of the dataset
The dataset that I used in part 3 of this assignment was a fake news article dataset.
I sourced this dataset from Kaggle which you can find at https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset. Through this link, you can download a folder containing a CSV of information on real news articles and a CSV of information on fake news articles.
This information includes:

   * The title of the article,
   * The text in the article,
   * The subject of the article,
   * The date the article was posted.

In my case, however, I was only concerned with the article titles as I could easily turn these into sentences and generate synthetic article titles.
I decided to use the fake news dataset over the real news dataset as I found this a more interesting task than generating real news.

This dataset contained 23,481 sentences and 37,429 words across these sentences. I calculated the average sentence length to be 14.732 words long.


# Appraisal of the generated sentences

You can find the generated sentences in the *'outputs'* folder. For each dataset I used, there is a file containing the raw generated sentences and then a cleaned version of these generated sentences.
This cleaning involves removing unneccessary spacing, removing the sentence boundaries and doing some capitalisation.

Upon inspecting the generated outputs, it is clear that they aren't very good and the limiations of using a bigram model are highlighted throughout. The sentences do not hold onto gramatical constructs and often the sentences radically change what they are talking about mid sentence.

When developing the algorithm to generate the sentences, I quickly realised that I would need to set a parameter to set the minimum length a generated sentence could be. This was because some of the output sentences were only a few words long and did not make sense. By setting the minimum sentence length to 4, I was able to cut out one word sentences among other flaws.

Despite these limitations, there are still some sentences that are somewhat comprehensive. These sentences generally tend to be the smaller length sentences as these are less complex in word structure, however, even some longer sentences appeared to be valid, an example of this is the cleaned sentence: 'Post-trump liberal heads explode! "chicken" [video]'.

Maybe if the number of words in the ngram was increased, this would help to create better sentences, but I forsee that even using trigram and 4-gram models, the approach will not be perfect. I don't think the approach of using ngrams is the best approach to sentence generation, however, it has proved an interesting experiment in highlighting the flaws and pro's of these models.
