---
layout: post
title: "CLI Tool to Tweet from Terminal - twit"
date: 2014-09-24 15:28:09 +0900
comments: true
categories: 
---

## twit

I developed an application to tweet from terminal which I wanted (and actually as practice of Ruby).

Let me show the demo of it and how to install.


## How to Use 

You can tweet as you use a command in terminal.

```
$ twit "It is posted from terminal."
```


## How to Install

The repository of twit is here.

https://github.com/totzYuta/twit

You can start to use this application just four steps.


### 1. Clone the repository

First, clone this repository into your HOME path. (If you have much knowledge of linux, that's not a problem to clone into another place.)

```
$ git clone https://github.com/totzYuta/twit
```


### 2. Run setting file

Second, let you do setting of your twitter account. 

Anyway, let us enter the directory.

```
$ cd ./twit/
```

And run the setting file by ruby. (If you have not installed ruby, let you install it. I don't mention how to do it. Please google...)

```
$ ruby setting_twit.rb
```

After run the program, your default web browser will be automatically opened and the page will tell you to enter your Twitter ID and Password.

You can get the PIN code after login. Copy and paste that after the words "Please Enter Your PIN: "


### 3. Set the pathes

Set the pathes to make it available to use "twit" command anywhere.

Then, please set absolute path. Change "YOUR_USER_NAME" to your user name.

```
$ sudo ln -s /Users/YOUR_USER_NAME/twit/setting_twit.rb /usr/bin/
$ sudo ln -s /Users/YOUR_USER_NAME/twit/setting.rb /usr/bin/
$ sudo ln -s /Users/YOUR_USER_NAME/twit/twit /usr/bin/
```


### 4. Tweet!

Okay, that's it! You can Tweet from the terminal by 'twit' command!

```
$ twit "It's tweeted  from terminal"
```

```
♪ Tweeted
```


## Conclusion

If you notice any problem, please let me konw. You can send me a message on Twitter (@yutaTotz) or create an issue at the repository's page. 

Thanks!
