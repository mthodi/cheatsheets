
Create Controllers
---
php artisan make:controller ControllerName
//create with CRUD resources i.e CRUD methods
php artisan make:controller --resource ControllerName

Working with Controllers
==========================
//passing data
Route::get('/url/{param}', 'ControllerName@methodName')

//RESTFul controller
//creates urls for INDEX, CREATE, SHOW, UPDATE, DESTROY and their
//corresponding HTTP methods
Route::resource("url", 'ControllerName');

//see routes with
php artisan route:list 


Working with Views
=====================
//passing data to Views

//controller
public function show($id){
	return view('post')->with('id', $id);
}

// OR as an array
return view('greeting', ['name' => 'James']);

//view file
<h3>Post {{$id}}</h3>

//multiple parameters
1) chain the with statements
2) passing a key value arrays

Working with Blade Templating Engine
======================================

In the master layout, you use @yield("NAME")
In the inheriting page you use:

@extends('masterLayout')
 @section("NAME")
 	HTML and JS for the page
 @endsection

 Working with Databases
 =========================

 php artisan migrate //run migration

 php artisan make:migration create_name_table --create="table_name"

//rollback the recent migrate
 php artisan migrate:rollback 

 //add column to table...create new migration for it
 php artisan make:migration add_col_to_table --table="table_name"

 //create seeder
 php artisan make:seeder SeederName

 //create factory
 php artisan make:factory FactoryName --model="ModelName"

 Working with Raw Queries
 ==========================
//inserting data
 DB::insert('INSERT INTO table_name(col1,col2) values(?,?)', ["val1", "val2"]);

//selecting data
 $results = DB::select('SELECT * FROM table_name WHERE col=?', [val]); 
 where $results is an array of objects. Each object is a record.
 Access
 ------
 foreach($results as $r){ do somthing with $r}


//updating data
$updated = DB:update('UPDATE table_name set col = "New Val" WHERE some_col=?', [val]);
$updated is the primary key (ID) of the updated record

//deleting data
DB::delete('DELETE FROM table_name WHERE col=?', [val]);
returns the key of the row that was deleted.

Working with Eloquent ORM
===========================
//create model
php artisan make:model

//create model and migrations

Setting up Vue.Js
==================

npm install
npm run watch
npm run dev