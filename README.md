# Asynchronous Tasks with FastAPI and Celery

Example of how to handle background processes with FastAPI, Celery, and Docker.

### Quick Start

Spin up the containers:

```
$ docker-compose up -d --build
```

Open your browser to [http://localhost:8004](http://localhost:8004)




tips:
#### FastAPI Background Tasks

- Running machine learning models
- Sending confirmation emails
- Scraping and crawling
- Analyzing data
- Processing images
- Generating reports

For example:

```
from fastapi import BackgroundTasks

def send_email(email, message):
    pass

@app.get("/")
async def ping(background_tasks: BackgroundTasks):
    background_tasks.add_task(send_email, "email@address.com", "Hi!")
    return {"message": "pong!"}
```

#### Celery

- CPU intensive tasks
- Task queue: a task queue to manage the tasks and workers
