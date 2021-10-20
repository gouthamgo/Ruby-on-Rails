# Make a CRUD App 

- Lets list out all the steps to make a CRUD APP using rails 

- Example here is making a books app

```
rails new bookapp --skip-git

rails generate migration create_books

Then go to the db and make a table you wanna create

rails db:create # create a database

rails db:migrate # looks through the folder and run the migrations

go to ---> rails db and .schema to check what you created 

  gem 'pry-rails' # You almost always want this.


Make seed data in the seed db file

rails db:seed ---> seed the data

Controllers-

$ touch app/controllers/books_controller.rb
mkdir app/views/books
touch app/views/books/{index,new,edit,show}.html.erb







```


