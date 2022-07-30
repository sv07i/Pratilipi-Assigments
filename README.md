# Pratilipi-Assigments
Develop predict model which pratilipis (at least 5), each user is going to read later?


Intro

Collaborative Filtering is a technique which is widely used in recommendation systems and is rapidly advancing research area. The two most commonly used methods are memory-based and model-based.


Approch

In this project , I created model which are userd (User-Based Collaborative Filtering) and (Popularity Based Filtering ). The main idea behind UBCF is that people with similar characteristics share similar taste. For example, if you are interested in recommending a movie to our friend Suraj, suppose Suraj and I have seen many movies together and we rated them almost identically. It makes sense to think that in future as well we would continue to like similar movies and use this similarity metric to recommend movies.

Second approch is Popularity based work on popularity idea, for example in Hollywood there are so many movies but few are best and worth to watch. avatar, FF series, Marvels, DC are example of Poppularity based filtering.

1) Popularity Based Filtering

so we have two csv datasets meta and user interaction. first I try popularity based aproch.

On the basis read_percent column I create in feature called rating in dataset. next step I create total_rating in particular Story_id .
and secondly create avg rating based on num of rating. Now I Merge the this two new column on basis of the Story_id.


Now I based on condition on total_rating column I put only those row which has more then 100 rating with user and sort value on avg_rating.


So at the end I get top most rated story_id which will I predict to user .


2)  User-Based Collaborative Filtering

The method identifies users that are similar to the queried user and estimate the desired rating to be the weighted average of the ratings of these similar users.

We would be doing the recommendation’s on Pratilipi datasets. The programming language used is python and the data analysis work is mostly done using pandas library. IDE used is jupyter notebook.

So before starting I would like to give the list of libraries used :

Pandas
Numpy
sklearn
 

for this approch I use read_percent to predict user interest.

for this I use story_id and read_percent on this i apply groupby function so gate famous story_id

now I use pivot_table on user_id , story_id, read_percent and check the Cosine Similarity.

This pivot_table shape is (2457 ,2457)


And at the last I create function to predict user interest.




At last!!!! We did it. We have our own recommendation system.




