# biopics task

You are given a data set called <code>biopics.csv</code> containing information on biographical movies. Your task is to perform some data manipulations on the biopics data.

### Data Overview
The original biopics data are made available by the analytics website FiveThirtyEight. You will be working with a preprocessed version, available for you at <code>./data/biopics.csv</code>. It contains following the columns:

* <code>title</code> - the movie's title
* <code>country</code> - country of production
* <code>year_release</code> - the year the movie was released
* <code>box_office</code> - movie's earning at the box office, in US$
* <code>type_of_subject</code> - the occupation of the movie's subject or their reason for recognition
* <code>lead_actor_actress</code> - the name of the actor or actress who played the subject

Write a function named <code>process_data()</code> that takes no arguments. The function should load the biopics data (this has been implemented for you), perform data manipulations described below and return a pandas data frame with the manipulated data.

Clean up the biopics data:

><ul>
>    <li>Filter out duplicated rows</li>
>    <li>Rename the variable called <code>box_office</code> to <code> earnings</code></li>
>    <li>Filter out rows for which <code>earnings</code> are missing i.e. they are <code>NaN</code></li>
>    <li>Keep only movies released in the year 1990 or later</li>
>    <li>Convert types of <code>type_of_subject</code> and <code>country</code> to categorical</li>
>    <li>Create a new variable called <code>lead_actor_actress_known</code> that is <code>False</code> if <code>lead_actor_actress</code> is <code>NaN</code> and <code>True</code> otherwise</li>
>    <li>Update <code>earnings</code> such that they are expressed in millions of dollars, instead of dollars</li>
>    <li>Reorder the columns in the dataframe such that they're are in the following order: <code>title, year_release, earnings, country, type_of_subject, lead_actor_actress, lead_actor_actress_known</code></li>
>    <li>Sort the rows in descending order by <code>earnings</code></li>
></ul>

On top of the Python Standard Library, you can make use of any function from the <code>pandas</code> package.