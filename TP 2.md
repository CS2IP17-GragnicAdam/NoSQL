1. `db.movies.find()`
2. `db.movies.find({director_name:'James Cameron'})`
3. `db.movies.find({director_name:'James Cameron'},{director_name:true,movie_title:true})`
4. `db.movies.find({title_year:2016})`
5. 5043 films `db.movies.countDocuments()`
   dont 106 films sorti en 2016 `db.movies.countDocuments({title_year:2016})`
   Soit 0.02% des films `106 / 5043`
6. `db.movies.find().sort({movie_title:1})`
7. `db.movies.find({},{movie_title:true,title_year:true}).sort({movie_title:1}).limit(10)`
8. `db.movies.find({language:'English'})`
   `db.movies.find({language:'English'}).count()`
9. `db.movies.find({movie_title:/star/i})`
10. `db.movies.find({movie_title:/^My/i})`
11. `db.movies.find({movie_title:/river$/i})`
12. `db.movies.find({movie_title:/America/i}).count()`
