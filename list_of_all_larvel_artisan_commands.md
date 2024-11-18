### **Popular Laravel Artisan Commands**

| **Command**                              | **Description**                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------|
| `php artisan list`                       | Lists all available Artisan commands.                                                          |
| `php artisan help <command>`             | Displays help for a specific command.                                                          |
| **Application Commands**                 |                                                                                                 |
| `php artisan serve`                      | Starts the Laravel development server at `http://localhost:8000`.                              |
| `php artisan down`                       | Puts the application into maintenance mode.                                                    |
| `php artisan up`                         | Brings the application out of maintenance mode.                                                |
| **Database Commands**                    |                                                                                                 |
| `php artisan migrate`                    | Runs all outstanding database migrations.                                                      |
| `php artisan migrate:rollback`           | Rolls back the last batch of migrations.                                                       |
| `php artisan migrate:refresh`            | Rolls back all migrations and re-runs them.                                                    |
| `php artisan migrate:reset`              | Rolls back all migrations.                                                                     |
| `php artisan db:seed`                    | Runs database seeders to populate tables with sample data.                                      |
| `php artisan make:seeder <name>`         | Creates a new database seeder file.                                                            |
| `php artisan db:wipe`                    | Deletes all tables, views, and types in the database.                                          |
| **Make Commands**                        |                                                                                                 |
| `php artisan make:model <name>`          | Creates a new Eloquent model.                                                                  |
| `php artisan make:controller <name>`     | Creates a new controller.                                                                      |
| `php artisan make:migration <name>`      | Creates a new migration file.                                                                  |
| `php artisan make:middleware <name>`     | Creates a new middleware class.                                                                |
| `php artisan make:seeder <name>`         | Creates a new database seeder file.                                                            |
| `php artisan make:request <name>`        | Creates a new form request class.                                                              |
| `php artisan make:factory <name>`        | Creates a new model factory.                                                                   |
| `php artisan make:command <name>`        | Creates a new Artisan command.                                                                 |
| **Cache and Config Commands**            |                                                                                                 |
| `php artisan config:cache`               | Caches the configuration files for faster performance.                                         |
| `php artisan config:clear`               | Clears the configuration cache.                                                                |
| `php artisan route:cache`                | Caches the application routes for faster route resolution.                                     |
| `php artisan route:clear`                | Clears the route cache.                                                                        |
| `php artisan cache:clear`                | Clears the application cache.                                                                  |
| **Queue Commands**                       |                                                                                                 |
| `php artisan queue:work`                 | Starts processing queued jobs.                                                                 |
| `php artisan queue:restart`              | Restarts queue workers gracefully.                                                             |
| `php artisan queue:table`                | Creates a migration for the jobs database table.                                               |
| **Event and Listener Commands**          |                                                                                                 |
| `php artisan make:event <name>`          | Creates a new event class.                                                                     |
| `php artisan make:listener <name>`       | Creates a new listener class.                                                                  |
| **Testing Commands**                     |                                                                                                 |
| `php artisan test`                       | Runs the application’s tests.                                                                 |
| **Route and View Commands**              |                                                                                                 |
| `php artisan route:list`                 | Displays all registered routes.                                                                |
| `php artisan view:clear`                 | Clears compiled view files.                                                                    |

