# Laravel Artisan Commands (Basic to Advanced)

Laravel provides a powerful command-line interface (CLI) called Artisan. Here's the complete list of Artisan commands with descriptions.

---

## **1. Application Environment Commands**
```bash
php artisan about                # Display information about your application
php artisan env                  # Display the current environment
php artisan serve                # Start the development server
```

---

## **2. Make Commands**

### **a. Creating Models**
```bash
php artisan make:model ModelName             # Create a model
php artisan make:model ModelName -m          # Create a model with a migration
php artisan make:model ModelName -mf         # Create a model with a migration and factory
php artisan make:model ModelName -msc        # Create a model with a migration, seeder, and controller
php artisan make:model ModelName --all       # Create a model with all related resources
```

### **b. Creating Controllers**
```bash
php artisan make:controller ControllerName                     # Create a controller
php artisan make:controller ControllerName --api               # Create an API controller
php artisan make:controller ControllerName --invokable         # Create a single-action controller
php artisan make:controller ControllerName --resource          # Create a resource controller
php artisan make:controller ControllerName --model=ModelName   # Create a controller for a specific model
```

### **c. Creating Migrations**
```bash
php artisan make:migration migration_name                      # Create a migration
php artisan make:migration migration_name --create=table_name  # Create a migration for creating a table
php artisan make:migration migration_name --table=table_name   # Create a migration for modifying a table
```

### **d. Creating Seeders and Factories**
```bash
php artisan make:seeder SeederName                             # Create a seeder
php artisan make:factory FactoryName                          # Create a factory
php artisan make:factory FactoryName --model=ModelName         # Create a factory for a specific model
```

### **e. Creating Middleware**
```bash
php artisan make:middleware MiddlewareName                     # Create middleware
```

### **f. Creating Requests**
```bash
php artisan make:request RequestName                           # Create a form request
```

### **g. Creating Commands**
```bash
php artisan make:command CommandName                           # Create a custom Artisan command
```

### **h. Creating Policies**
```bash
php artisan make:policy PolicyName                             # Create a policy
php artisan make:policy PolicyName --model=ModelName           # Create a policy for a specific model
```

### **i. Creating Other Files**
```bash
php artisan make:event EventName                               # Create an event
php artisan make:listener ListenerName                         # Create a listener
php artisan make:job JobName                                   # Create a job
php artisan make:notification NotificationName                 # Create a notification
php artisan make:rule RuleName                                 # Create a custom validation rule
php artisan make:mail MailName                                 # Create a mail class
```

---

## **3. Database Commands**

### **a. Running Migrations**
```bash
php artisan migrate                                  # Run all migrations
php artisan migrate:fresh                            # Drop all tables and re-run all migrations
php artisan migrate:refresh                         # Rollback & re-run all migrations
php artisan migrate:rollback                        # Rollback the last batch of migrations
php artisan migrate:status                          # Show the status of each migration
```

### **b. Running Seeders**
```bash
php artisan db:seed                                 # Seed the database
php artisan db:seed --class=SeederName              # Run a specific seeder
```

### **c. Database Backup and Reset**
```bash
php artisan db:wipe                                 # Drop all tables, views, and types
```

---

## **4. Route Commands**
```bash
php artisan route:list                              # List all registered routes
php artisan route:cache                             # Cache the routes
php artisan route:clear                             # Clear the route cache
```

---

## **5. Config Commands**
```bash
php artisan config:cache                           # Cache the configuration
php artisan config:clear                           # Clear the configuration cache
```

---

## **6. Cache Commands**
```bash
php artisan cache:clear                            # Clear the application cache
php artisan cache:forget key                       # Remove a specific key from the cache
php artisan cache:table                            # Create the cache database table
```

---

## **7. View Commands**
```bash
php artisan view:cache                             # Compile all views
php artisan view:clear                             # Clear the compiled views
```

---

## **8. Queue Commands**
```bash
php artisan queue:table                            # Create a jobs table
php artisan queue:work                             # Process the next job on the queue
php artisan queue:retry                            # Retry a failed queue job
php artisan queue:failed                           # List all failed queue jobs
php artisan queue:failed-table                     # Create the failed jobs database table
php artisan queue:flush                            # Flush all failed jobs
php artisan queue:restart                          # Restart queue workers
```

---

## **9. Event and Listener Commands**
```bash
php artisan event:generate                         # Generate event and listener classes
```

---

## **10. Storage Commands**
```bash
php artisan storage:link                           # Create a symbolic link from "public/storage" to "storage/app/public"
```

---

## **11. Testing Commands**
```bash
php artisan test                                   # Run tests
php artisan test --group=groupName                 # Run a specific group of tests
php artisan dusk                                  # Run Dusk tests (for browser testing)
```

---

## **12. Package Commands**
```bash
php artisan vendor:publish                         # Publish assets/configs/views from packages
php artisan vendor:publish --tag=tagName           # Publish specific tag resources
```

---

## **13. Advanced Optimization Commands**
```bash
php artisan optimize                               # Cache routes, config, and views
php artisan optimize:clear                         # Clear all cached files
```

---

## **14. Miscellaneous Commands**
```bash
php artisan inspire                                # Display an inspirational quote
php artisan package:discover                       # Discover and register packages
```

---

## **15. Custom Commands**
You can create your own Artisan commands using:
```bash
php artisan make:command CommandName
```
Example of running a custom command:
```bash
php artisan command:name
```

---

**Note:** For more information about any command, use the `--help` option:
```bash
php artisan command_name --help
```
