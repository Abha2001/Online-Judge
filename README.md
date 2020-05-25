![Django CI](https://github.com/himanshu272/Online-Judge/workflows/Django%20CI/badge.svg)

# Online-Judge
Port of the Online Judge in Python

## Working

Initially the user chooses a language in the code editor and starts to write the answer based on the coding question. When the user submits the answer, the answer passes to the server. In the server a task id is being created in the postgres sql and the job is being sent to the rabbit mq queue. Then celery picks up the job and executes it in a sandbox environment which is developed using C. This helps to increase security and prevents malicius code injection attacks on the platform. When the job finnishes execution the result is sent to the frontend using long polling. In this way the system verifies the users code, evaluate it and generates it ranking based on scores from other peers.

## Documentation to help with Celery
https://docs.celeryproject.org/en/stable/getting-started/next-steps.html#next-steps

## API Documentation

https://documenter.getpostman.com/view/7834053/Szmh1vuz?version=latest
