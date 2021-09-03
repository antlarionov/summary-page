---
title: "Hello world"
date: 2021-08-10T21:52:00+03:00
draft: false
---
Here is my first post in this blog, and it's going to be about all this hugo stuff and problems, which I encountered 
during writing, deploying and tuning it.
The idea is to have personal blog page, where i can share my thought, strange moments in work and hard moments about DevOps stuff.
* 1st and foremost problem is with my hosting provider (Hostinger), where i've switched dns to new servers and only after 
some time decided to reset all my dns records. It worked fine only when I finally did it. 
* Another hard part was to choose right template for Hugo framework, that makes me feel fine. I mean no stupid design, 
maximal minimalistic.
* One more problem is that docker-compose is creating separated networks for each compose file you run. So I had to write it like 
    ```
    networks:
      default:
        external:
          name: external
    ```
    and also I had to create a new docker network which will share same net space between this website compose and the 
one that is responsible for proxying and ssl termination.


That's it for today. Cya! 
