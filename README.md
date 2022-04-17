# ActixWeb Task Service

[![Stargazers][stars-shield]][stars-url]
[![Forks][forks-shield]][forks-url]
[![Contributors][contributors-shield]][contributors-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

This is a simple task management web service built with [Actix Web](https://actix.rs/) and [AWS DynamoDB](https://aws.amazon.com/dynamodb/).

Check out the documentation below to get started.

Feature request? Check the past discussions to see if it has been brought up previously. Otherwise, feel free to start a new discussion thread. All ideas are welcomed!

## Quick Start Guide

1. Clone the repo

```
git clone https://github.com/michaelradu/ActixWebTaskService.git
```

2. Add your aws_config to your environment variables
3. Build the project

```
cargo build
```

4. Run the project

```
sudo cargo run
```

5. Test its functionality with tools such as `postman`

## Usage

1. Create tasks

```
POST http://127.0.0.1/task
```

with the following body

```json
{
    "user_id": "randomuuid",
    "task_type": "Your_task_type",
    "source_file": "your_file"
}
```

2. Get tasks

```
GET http://127.0.0.1/task/taskid 
```

3. Start a task

```
PUT http://127.0.0.1/task/taskid/start
```

4. Pause a task

```
PUT http://127.0.0.1/task/taskid/pause
```

5. Complete a task

```
PUT http://127.0.0.1/task/taskid/complete
```

with the following body

```json
{
    "result_file": "your_file"
}
```

6. Fail a task

```
PUT http://127.0.0.1/task/taskid/fail
```

and more...

## Licence

[GPLv3](michaelradu/ActixWebTaskService/LICENSE) © [Michael Radu](https://www.mihairadu.cf)



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/michaelradu/ActixWebTaskService.svg?style=social
[contributors-url]: https://github.com/michaelradu/ActixWebTaskService/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/michaelradu/ActixWebTaskService.svg?style=social
[forks-url]: https://github.com/michaelradu/ActixWebTaskService/network/members
[stars-shield]: https://img.shields.io/github/stars/michaelradu/ActixWebTaskService.svg?style=social
[stars-url]: https://github.com/michaelradu/ActixWebTaskService/stargazers
[issues-shield]: https://img.shields.io/github/issues/michaelradu/ActixWebTaskService.svg?style=social
[issues-url]: https://github.com/michaelradu/ActixWebTaskService/issues
[license-shield]: https://img.shields.io/github/license/michaelradu/ActixWebTaskService.svg?style=social
[license-url]: https://github.com/michaelradu/ActixWebTaskService/blob/master/LICENSE