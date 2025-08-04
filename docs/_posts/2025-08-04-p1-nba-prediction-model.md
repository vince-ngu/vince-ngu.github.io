---
layout: post
title: "Project 1: NBA Betting Model"
author: Vince Nguyen
date: 2025-08-04
---

## About

Ever since I was a kid, basketball has been ingrained into my life in some way, shape, or form. From shooting in the backyard with a deflated ball and a hoop I begged my parents to buy off Craigslist in 5th grade to buying last-minute nosebleed seats ($25!) to see Curry face off against LeBron in college, basketball has always been important to me. Despite this, there was one thing that I wasn't involved in that took the sports world by storm in 2018 after the Professional and Amateur Sports Protection Act (PASPA) was foregone by the Supreme Court: sports betting.

"Look at this parlay I just made," my friends would tell me as they showed me a list of what seemed to be, in my mind, some _terrible_ sports takes on their phone. Jayson Tatum scoring more than 25.5 against the No.1 Defensive Rating team in the NBA? Give me a break. Brooke Lopez grabbing over 6 boards against a team full of bigs? Sorry Brooke, you're not really the center you used to be. All these parlays being build around "feasible" numbers and predictions based on "hunches" lead me to a lingering question: can't you reliably predict these plays based on the statistics? The NBA is extremely meticulous when keeping track of stats for players, so much so that some of the statistics are frustratingly obscure. You'll see on screen things like "Only Player to Score 30+ Points While Coming Off an Ankle Sprain After 3 Weeks" (Okay, it's not *that* bad but you get the picture).

Come post-grad, I'm furiously applying for jobs in the tech market. I landed an interview for an internship at a startup that focuses on beating the market when it comes to sports betting. Without going too much into detail, they use their proprietery models to predict which bets were worth taking and which were too risky to build your parlay around. While I made it to the final round, my journey decided that I was to take another route (I was rejected). Slightly down, yet inspired, I decided to take my own step towards something similar with this personal project. I was going to build my own rudimentary sports betting model to help me beat the market.

## Finding the Correct Model

It's been a few years since I've taken my undergraduate introductory statistics and probabilities course, so I decided to go back and read up on simpler models that I could intially use to get my feet off the ground. I remember using Simple and Mulitple Linear Regressions in my statistics course and did more review there. It seemed easy enough, right?

My initial plan was to find a dependent variable (Y), like the amount of points predicted to score, based off an independent variable (X), like a player's average Points Per Game (PPG) against the team they're supposed to play against. A textbook Simple Linear Regression. It wasn't until I was cleaning data when I realized that a team *only* plays against another team 2-4 times **per season**. That's not nearly enough data to accurately create a model that predicts a player's PPG. Quite frankly, that felt like I didn't have any data at all. Furthermore, I took a step back and realized that there were way more variables I had to take into account for my model to be *remotely* accurate. Things like their Field Gold Percentage (FGP), Minutes Per Game (MPG), if they were previously injured, their current scoring streak (Have they been on a hot streak within the past 5 games?), rest days, home or away, etc. These different considerations lead me to realize that I need to move to a Multiple Linear Regression Model so that I can use multiple independent variables to find my dependent variable.