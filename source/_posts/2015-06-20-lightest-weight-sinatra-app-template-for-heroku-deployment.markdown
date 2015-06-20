---
layout: post
title: "Lightest Weight Sinatra App Template for Heroku  Deployment"
date: 2015-06-20 17:39:17 +0900
comments: true
categories: [Ruby, Sinatra, Heroku]
---

I prefer use Sinatra to make simple web app rather than Ruby on Rails. And I like using Heroku when I wanna check simply how its going on.

So I made a simplest Sinatra app to deploy the app as soon as possible. You can clone the reporitory and deploy it soon.

[Lightest Sinatra App for Heroku](https://github.com/totzYuta/lightest-sinatra-app-for-heroku)

I made two versions, one is using database by PostgreSQL, and another is not using one. If you do not have to use database on Heroku, please checkout `light` branch.

If you want to use database, please use master branch and do not forget runnning command below to add PostgreSQL addon for heroku. 

```
$ heroku addons:create heroku-postgresql
```

And please edit migrate file to change the scheme of the table, or just remake the migration file. After finishing to edit the migration file, please run command below:

```
$ heroku run rake db:migrate
```

Please let you see README file for detailed usage. 

If you find any bug or ideas, shoot me a message to my twitter account ([@totzyuta](https://twitter.com/totzyuta)) or create an issue on the [repository page](https://github.com/totzYuta/lightest-sinatra-app-for-heroku).

Thank you. 
