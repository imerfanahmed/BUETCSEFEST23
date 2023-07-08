# BUET CSE FEST 23 Hackathon

This is a Laravel application that showcases the implementation of  Sanctum authentication, and registration endpoints.

## Installation

To get started with the project, follow these steps:

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/imerfanahmed/BUETCSEFEST23
   ```

2. Navigate to the project directory:
   ```bash
   cd BUETCSEFEST23
   ```

3. Install the required dependencies using Composer:
   ```bash
   composer install
   ```

4. Create a copy of the `.env.example` file and rename it to `.env`:
   ```bash
   cp .env.example .env
   ```

5. Generate a new application key:
   ```bash
   php artisan key:generate
   ```

6. Configure the database connection in the `.env` file with your credentials:
   ```dotenv
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database
   DB_USERNAME=your_username
   DB_PASSWORD=your_password
   ```

7. Start the development server:
   ```bash
   php artisan serve
   ```

Now you should be able to access the application at `http://localhost:8000`.

## Authentication Endpoints

This project utilizes Laravel Sanctum for API authentication. The following endpoints are available:

- `POST /api/register`

  This endpoint allows users to register by providing their `name`, `email`, and `password` parameters. Upon successful registration, it returns a JSON response with an authentication token.

  Example Request:
  ```http
  POST /api/register HTTP/1.1
  Host: localhost:8000
  Content-Type: application/json

  {
    "name": "Erfan Ahmed Siam",
    "email": "erfan.siam98@gmail.com",
    "password": "password123"
  }
  ```

  Example Response:
  ```json
  {
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjBkMTczN2MwMmE5ZD..."
  }
  ```

- `POST /api/login`

  This endpoint accepts `email` and `password` parameters and returns a JSON response with an authentication token if the credentials are valid.

  Example Request:
  ```http
  POST /api/login HTTP/1.1
  Host: localhost:8000
  Content-Type: application/json

  {
    "email": "erfan.siam98@gmail.com",
    "password": "password123""
  }
  ```

  Example Response:
  ```json
  {
    "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6IjBkMTczN2MwMmE5ZD..."
  }
  ```

Please note that the authentication endpoints are just examples and can be customized to fit your specific application requirements.

## License

This project is open-source and available under the [MIT License](LICENSE). Feel free to modify and use it as per your needs.

## Contribution

Contributions are welcome! If you find any issues or have suggestions, please create a new issue or submit a pull request.
