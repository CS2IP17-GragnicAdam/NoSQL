1. `db.movies.find({duration:{$gte:180}})`
2. `db.movies.find({title_year:{$gte:2015}})`
   `db.movies.find({title_year:{$gte:2015}}).count()`
3. `db.movies.find({title_year:{$gte:1980,$lte:1989}},{title_year:true,movie_title:true}).sort({title_year:1})`
4. `db.movies.find({genres:['Sci-Fi']})`
5. `db.movies.find({actors:{$elemMatch:{name:/Stone/i}}})`
6. `db.movies.find({title_year:{$gte:2015},imdb_score:{$gte:8}})`
7. `db.movies.find({gross:{$ne:''}},{gross:true,movie_title:true}).sort({gross:-1}).limit(10)`
8. `db.movies.find({gross:{$ne:''}},{gross:true,movie_title:true}).sort({gross:-1}).skip(10).limit(10)`
9. `db.movies.find({genres:{$all:['Comedy','Thriller','Sci-Fi']}})`
