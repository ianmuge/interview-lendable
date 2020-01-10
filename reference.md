# Purpose

This project is a test project for the candidates at Lendable. Whatever you see in the assignment doesn't necessarily represent how we work or what we do; for example, some things in this test are even misconfigured purposefully. Your solution will represent your abilities and approach as a candidate: we might treat your application as you treat the assingment; do your best to impress.

## Scenario

We have an existing website that we run on EC2 instances using Apache HTTPD. It runs fairly well but we need to copy all sources to the servers every time and manually configuring Apache; all of which is very time consuming. Not to mention the cost of running these EC2 instances.

In search of a solution we found nginx and we'd been reading a lot lately about Docker. As a first try, we created this project for the Docker image where we have the website added as a Git submodule to the project, so that we can clone the solution onto every EC2 instance, then we can run `docker build` and run to host the project.

That was the idea anyway, but we can't make it work! Whenever we try to run `docker run <image_id> -dit -v /home/ec2-user/tech-test/www:/www -p 80:80` the container just exists.

## Task

Your assignment is to make the project work. For that you need to have at least a basic understanding of Git, but more experience working with Docker and Nginx. The goal is to have the website up & running on port 80 to handle public traffic.

Ideally, you submit some automation code where the above process can be replicated onto as many EC2 servers as we see fit. This might involve redesigning the build & deployment process, which is perfectly allowable; use your discretion here.

For bonus points you can write up your findings and recommendations.

## Notes

* You might want to document what you do and why (per the mantra of "the commentary is more important than the result").
* Although we encourage you to consult online sources, you must complete this exercise yourself and demonstrate a solid depth of indepenent understanding to us during a follow-up face-to-face interview.
* Please create a _private_ repo on GitHub and share the end result as a repository.