# Music_genre_Multiclass_hackathon
Music has been an important part of our lives since time immemorial. Every artist has a signature, making music a subjective art. We have scales/metrics to measure the quality of music. But, is it possible to train a machine learning model to predict the genre and quality of the music?
About Dataset:

Training dataset: 17,996 rows with 17 columns 

Column details: artist name; track name; popularity; ‘danceability’; energy; key; loudness; mode; ‘speechiness’; ‘acousticness’; ‘instrumentalness’; liveness; valence; tempo; duration in milliseconds and time_signature. 

Target Variable: 'Class’ such as Rock, Indie, Alt, Pop, Metal, HipHop, Alt_Music, Blues, Acoustic/Folk, Instrumental, Country, Bollywood, 

Test dataset: 7,713 rows with 16 columns 

### Approach

The track name and artist name are high cardinal values. They are target encoded to decrease the cardinality trading the variance. 

Key, Mode and Time signature appears to be categorical data owing to their unique and discrete distribution. 

Finally, catboost classifier is used as it handles the categorical variables well and need not be encoded seperately.

The metric chosen is logloss.
