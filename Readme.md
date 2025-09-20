# **ReVerse Enterprise Setup**

## **Environment configuration**

1. Copy .env.example to .env:  
   cp .env.example .env

2. Replace the development SECRET\_KEY with a unique 32+ character value.  
3. Update DATABASE\_URL and other connection strings so they point to the  
   services you plan to use (PostgreSQL, Redis, etc.).

If a .env file is not supplied the application will fall back to the  
development defaults that ship with the repository. These values are only meant  
for local development.

## **Running main\_enterprise.py**

After your environment variables are configured you can start the API with:

uvicorn src.reverse.main\_enterprise:app \--reload

The module can be imported without a configured .env file, but the explicit  
configuration described above should be provided before running the service in  
any shared environment.