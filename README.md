# 7375-final

## Video and Report

[Video](https://www.youtube.com/watch?v=glCA0Id72eE)
[Report](./REPORT.pdf)

## How to run the code

Environment File

```
# Create a .env file
# Paste the code from .example.env
# Then add all the secrets

SECRET_KEY=[a random password]
SQLALCHEMY_DATABASE_URI=[sqlite:///path/to/your/database.db]
UPLOAD_URL=[langfuse upload url]

OPENAI_API_KEY=[open ai api key]

REDIS_URI=[if you are using MacOS, then it would be redis://localhost:6379]

PINECONE_API_KEY=[Pinecone api key]
PINECONE_ENV_NAME=[Pinecone location]
PINECONE_INDEX_NAME=[Pinecone index name]

LANGFUSE_PUBLIC_KEY=[you can leave it as blank]
LANGFUSE_SECRET_KEY=[you can leave it as blank]
```

Install [Redis](https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/)

```
# If you are using MacOS
brew install redis

# Start Redis
redis-server
```

Create a new terminal window, go to project's folder, then

```
# Install dependencies, you can have an overview of what packages are needed by going to Pipfile
pipenv install

# Create a virtual environment
pipenv shell

# Initialize the database
flask --app app.web init-db
```

Create a new terminal window

```
# Go to client folder
cd client

# Install npm packages
npm install

# Build client files
npm run build

# Open the virtual environment
pipenv shell

# Run Python server
inv dev
```

Create a new terminal window

```
# Open the virtual environment
pipenv shell

# Run Python server
inv devworker
```

P.S. How to clean all the data?

```
flask --app app.web init-db
```

## Contact me

yin.qian@northeasten.edu

I would like NOT to share the project on public platforms.
