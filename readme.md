/*--------- SQLITE arquiteture example ---------*/
npm i sqlite3 sqlite --save (install sqlite)

create database folder in /src/ folder, create sqlite folder
in /src/database folder, create index.js in /src/database/sqlite folder

update /src/server.js, import database, execute database = database.db 
will be created

start use beekeeper, create table in beekeeper

create migrations in src/database/sqlite folder, create createUsers.js 
in /src/database/migrations folder, create index.js
in /src/database/migrations folder

update /src/server.js, update database to new database automated(migrationsRun)

update /src/controllers/UsersController.js, import sqliteConnection(database), 
change "create" to async, create database, create verifications,
create insert data(database.run)

npm i bcryptjs(password encryptor)

import hash(bcryptjs) in /src/controllers/UsersController.js,
create hashedPassword, update database.run

create async update(update function) in /src/controllers/UsersController.js

create usersRoutes.put in /src/routes/users.routes.js

import compare(compare password encrypted), update database.run in 
/src/controllers/UsersController.js

/*--------- SQL QUERY BUILDER ---------*/
npm install knex --save, npx knex init(create knexfile.js), 
update /src/knexfile.js

create knex folder in database folder, create index.js in knex folder

update knexfile.js(create migrations development), create migrations folder
in knex folder

npx knex migrate:make createNotes(create createNotes.js in folder defined
on knexfile.js), update /src/database/knex/migrations/createNotes.js

npx knex migrate:latest(optional: create a script in package.json
with that code)

npx knex migrate:make createTags(create createTags.js in folder defined
on knexfile.js)

npx knex migrate:make createLinks(create createLinks.js in folder defined
on knexfile.js)

update knexfile.js(create pool in module.exports)

create NotesController.js in /src/controllers folder

create notes.routes.js in /src/routes folder

update index.js in /src/routes folder(import notesRouter)

create methods create/show/delete/index in /src/controllers/NotesController.js

update notes.routes.js(add create/show/delete/index functions) in /src/routes/

create TagsController.js in /src/controllers folder

create tags.routes.js in /src/routes folder

update index.js in /src/routes folder(import tagsRouter)