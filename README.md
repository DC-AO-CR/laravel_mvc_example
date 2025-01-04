# Laravel MVC example

This is a simple example of using the MVC framework in Laravel.

The project show a list of students through a web page (http://localhost/overview) or through a RESTful JSON call (http://localhost/students).

There are no students in the database, so the web page and call will be empty, and you'll have to add the students first by hand through a database management tool.

## How do I run this project?

You will need to do the following steps to get this project up and running:
* Clone the project to a local directory.
* Use the command `./vendor/bin/sail up` in a terminal to get the project up and running.
* Use the command `./vendor/bin/sail artisan migrate` in a terminal to build the tables of the database.

## Which commands were used to create the files?

The advantage of using Laravel is that it's a MVC framework in which the content of each file may be different but the structure remains the same. For example, all models go into the Models folder and all extend the Model class. We could create each Model file on our own, but we can also use the Artisan console of Laravel to generate a Model for us.

Most files in this project were first generated with the Artisan console and got their content added afterwards.

### How can we generate the Student migration?

We can generate a `migration` with the Artisan console through the Sail container.

`./vendor/bin/sail artisan make:migration create_student_table`

This command created the following file: [database/2024_11_13_134137_create_student_table.php](database/migrations/2024_11_13_134137_create_student_table.php).

### How can we generate the Student model?

We can generate a `model` with the Artisan console through the Sail container.

* `./vendor/bin/sail artisan make:model Student`

This command created the following file: [app/Models/Student.php](/app/Models/Student.php).

### How can we generate the Student controller?

We can generate a `controller` with the Artisan console through the Sail container.

`./vendor/bin/sail artisan make:controller StudentController`

This created the following file file: [app/Http/Controllers/StudentController.php](app/Http/Controllers/StudentController.php).

### How can we add a GET route to the method in the controller?

We put a route in the `web` to be reachable by an URL in the web app.

We added the GET route in the following file: [routes/web.php](routes/web.php)

### How can we generate the Student view?

We can generate a `view` with the Artisan console through the Sail container.

* `./vendor/bin/sail artisan make:view overview`

This created the following file file: [resources/views/overview.blade.php](resources/views/overview.blade.php).
