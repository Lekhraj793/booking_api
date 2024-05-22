# booking_api

## Project Setup

To set up the project, follow the steps below:

1. Clone the Repository: Clone this repository to your local machine:

```bash
git clone https://github.com/Lekhraj793/booking_api.git
```


2. Install Dependencies: Navigate to the project directory and install PHP dependencies using Composer:
```bash
composer install --ignore-platform-reqs
```

```bash
composer dump-autoload
```

3. Database Setup: Rename .env.example file. Create the mysql database. Change DB_DATABASE, DB_USERNAME and DB_PASSWORD witht the actual values.

4. Run Migrations and Seeders: Run database migrations and seeders to set up the database schema and populate initial data:

```bash
php artisan migrate
```

5. Install Laravel Passport: Install Laravel Passport for API authentication:

```bash
php artisan passport:install --no-interaction
```

6. To create a personal access client, you can use the following command:

Notice: If you do not create it, you will get the error that "Personal access client not found. Please create one."

```bash
php artisan passport:client --personal

```

7. Seed the database to get some dummy data

```bash
php artisan db:seed 
```

8. Generate the application key.

```bash
php artisan key:generate 
```

This command will seed two tables: User table and Healthcare professional table

9. Start the Laravel development server

```bash
php artisan serve
```

10. Do the testing through postman. Collection can be found in root directory.


## Usage

- **POST /api/register: Register a new user.**

- **POST /api/login: Log in with user credentials and obtain an access token**

- **GET /api/healthcare-professionals: Retrieve a list of all available healthcare professionals.**

- **POST /api/book-appointment: Book an appointment with a healthcare professional.**

- **GET /api/user/appointments: View all appointments for a user.**

- **DELETE /api/cancel-appointment/{appointmentId}: Cancel an appointment by its ID.**

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
