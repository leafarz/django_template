# django_template
Django template project

## Info
- Currently designed for Heroku deployment.

## Setting Up
1) In the root folder, create a virtual environment:
    ```
    python -m venv venv
    ```

2) Activate the virtual environment
    ```
    venv\Scripts\activate
    ```

3) Install the packages
    ```
    pip install -r requirements.txt
    ```

## Renaming the project
- In the src folder, input the following command:
    ```
    python manage.py rename django_template NEW_PROJECT_NAME
    ```

## Running
### Local Deployment
1) Create a .env file in django_template directory `(src/.env)`

    a) Build Configuration
      - Add and set BUILD_CONFIG environment variable to dev or prod in .env file.
        ```
        BUILD_CONFIG=dev
        ```
    b) Secret Key
      - Generate a secret key for django. Add and set it in .env file.
        ```
        SECRET_KEY=[secret_key_without_quotes]
        ```
2) Go to the src directory and configure migration
    ```
    cd src
    python manage.py makemigrations
    python manage.py migrate
    ```

3) Run the server:
    ```
    python manage.py runserver
    ```

## Deployment
### Heroku
   1) Create a Heroku app
   2) Make sure to set environment variables
   3) Upload
      - Project should be readily configured for deployment

## Tools used
- Python v3.8.2

## References
1) ([JustDjango](https://www.youtube.com/channel/UCRM1gWNTDx0SHIqUJygD-kQ)) [Creating a Django Boilerplate Project](https://www.youtube.com/playlist?list=PLLRM7ROnmA9FgFlqn-HHBz0LJ62qJBwSw)
