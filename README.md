Proposed Project Summary:

Background & Strategic Objectives
Book reviews posted online affect our intention to start reading a book, and sometimes have power influencing our own attitude towards books. This interesting phenomenon compelled us to further explore and analyze data patterns from book reviews. Obviously, there are countless number of book reviews over millions of books online. To clearly define the scope of this project, we have narrowed down the genres for our analysis to three distinctive and popular ones on goodreads.com with ample data that intrigued us the most -- Children, History, and Mystery1.

Before diving into the data, our initial hypothesis is that reviews of different book genres  and book authors tend to exhibit different types of characteristics. In addition, we are interested in identifying user persona segments based on the types of rating and review patterns they share in an attempt to uncover the differences in these patterns among their reviews in various genres.

Research Objectives
Our research objectives are mainly covered by the following three categories:

A. Reviews by genre:
What are the similarities and differences in book reviews across various genres? Does one genre tend to receive better reviews or higher ratings than others? What are the unique patterns in each genre’s review that stand out compared to other ones (i.e. word frequency, popular sentiment, etc.)? To accomplish this goal, we will be using libraries such as Scattertext to uncover words and phrases that are more characteristic of one genre than other ones.  

B. Reviews by user:
Judging from general sentiment of reviews, users could be classified as “likers” or “haters”. “Likers” are those who tend to leave more positive reviews, whereas “haters” tend to do the opposite. By grouping users who have posted reviews by id and calculating their average rating scores, we plan to identify those users who fall on either extreme ends of the spectrum. Intimately attached to this goal, is our aim to understand whether a rating given to a book aligns well with the wording used in the review text. For instance, some reviewers might give a glowing review to a book but also assign it 3 or 4 stars. (as opposed to a 5). We plan to use libraries such NLTK VADER and Textblob to calculate polarity scores and use those scores to compare against the ratings given.

C. Reviews by author:
Who is the best-rated author within each genre? What are the most salient review sentiments/word patterns received by each author? Which genre’s authors received better ratings than others?

Data Source Details:
The following papers are the main source of our data:
	Mengting Wan, Julian McAuley, "Item Recommendation on Monotonic Behavior Chains", in RecSys'18. [bibtex]
	Mengting Wan, Rishabh Misra, Ndapa Nakashole, Julian McAuley, "Fine-Grained Spoiler Detection from Large-Scale Review Corpora", in ACL'19. [bibtex]

Datasets Group 1 Mystery, Thriller & Crime
•	Name: goodreads_reviews_mystery_thriller_crime.json
o	Description: book reviews data extracted from mystery, thriller, and crime genres on goodreads.com, last updated in May 2019.
o	Size: 1.88 GB
o	Location: https://drive.google.com/uc?id=1ONpyuv0vrtd6iUEp0-zzkKqwpm3njEqi 
o	Format: json
Access Method: google drive download
•	Name: goodreads_books_mystery_thriller_crime.json
•	Description: book and author info extracted from mystery, thriller, and crime genres on goodreads.com, last updated in May 2019.
•	Size: 1.08 GB
•	Location: https://drive.google.com/uc?id=1ACGrQS0sX4-26D358G2i5pja1Y6CsGtz 
•	Format: json
Access Method: google drive download


Datasets Group 2 History & Biography
•	Name: goodreads_reviews_history_biography.json
o	Description: book reviews data extracted from history and biography genres on goodreads.com, last updated in May 2019.
o	Size: 2.24 GB
o	Location: https://drive.google.com/uc?id=1lDkTzM6zpYU-HGkVAQgsw0dBzik-Zde9 
o	Format: json
Access Method: google drive download
•	Name: goodreads_books_history_biography.json
o	Description: book and author info extracted from history and biography genres on goodreads.com, last updated in May 2019.
o	Size: 1.45 GB
o	Location: https://drive.google.com/uc?id=1roQnVtWxVE1tbiXyabrotdZyUY7FA82W 
o	Format: json
Access Method: google drive download
Datasets Group 3 Children’s Books
•	Name: goodreads_reviews_children.json
o	Description: book reviews data extracted from children books genre on goodreads.com, last updated in May 2019.
o	Size: 565.6 MB
o	Location: https://drive.google.com/uc?id=1908GDMdrhDN7sTaI_FelSHxbwcNM1EzR 
o	Format: json
Access Method: google drive download
•	Name: goodreads_reviews_children.json
o	Description: book and author info extracted from children books genre on goodreads.com, last updated in May 2019.
o	Size: 533 MB
o	Location: https://drive.google.com/uc?id=1R3wJPgyzEX9w6EI8_LmqLbpY4cIC9gw4
o	Format: json
Access Method: google drive download

Anticipated Data Manipulation
Initial processing of datasets will include extracting columns containing information needed from each reviews dataset to reduce the file size. Similarly, we will extract author and books identifiers from each books dataset to reduce the file size.
From the review datasets, we will extract records with either rating or review text, add a ‘genre’ column to link a book review to its genre, then merge with books datasets accordingly on the book ID key.
We anticipate calculating word frequency using map reduce and Scattertext library to identify frequently appearing words and phrases in each genre to perform sentiment analysis tasks. The results of the work will allow us to analyze salient sentiments patterns in comparison with rating patterns, categorized by genre, by user, and by author.

Interesting Visualization Details
•	Distribution of review ratings for different genres, users, and authors
•	Distribution of review text sentiment for different genres, users and authors
•	Distribution of review text readability index across genres 
•	Scatterplot of polarity scores and ratings
•	A Scattertext visualization that maps word frequency to its associated genre

Team Contributions
Our team will contribute joint effort on all major tasks. We have noted areas where each member will take a leading role according to the categories defined in the project guidelines.
•	Identifying initial research topic territory: Sophia
•	Data Sources: Manel
•	Data Manipulation & Analysis: collaborative efforts with equal participation
•	Visualization: ScatterText Visuals-Manel, Distributions-Sophia
•	Gender Identification for Authors & Review readability index: Manel
•	Final Report: collaborative effort with equal participation



Notes:
1.	Additional rationale on selecting these three genres: they are not too extremely different to have zero overlap in vocabulary used in the reviews. For instance, genres such as graphic novels and poetry will have details that are very specific to their unique genres.
