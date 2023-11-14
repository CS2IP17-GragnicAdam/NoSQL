1. `db.movies.find({title_year:{$ne:''}}).sort({title_year:1}).limit(1)`
   `db.movies.find({title_year:{$ne:''}}).sort({title_year:-1}).limit(1)`
2. `db.movies.find({gross:{$ne:''}}).sort({gross:1}).limit(1)`
3. `db.movies.find({title_year:''}).count()`
4. `db.movies.distinct('genres')`
   `db.movies.distinct('genres').length`
5. `db.movies.countDocuments() / (db.movies.distinct('director_name').length - 1)`
6. `db.movies.distinct('color',{color:{$nin:['Color','']}})`
7. `db.movies.find({director_name:'Clint Eastwood',actors:{$elemMatch:{name:"Clint Eastwood"}}})`
   `db.movies.find({$or:[{director_name:"Clint Eastwood"},{'actors.name':"Clint Eastwood"}]})`
   `db.movies.find({director_name:{$ne:'Clint Eastwood'},actors:{$elemMatch:{name:"Clint Eastwood"}}})`
