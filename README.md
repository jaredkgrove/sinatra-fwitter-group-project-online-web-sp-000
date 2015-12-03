# Fwitter Group Project

## Objectives

1. Build a full scale Sinatra application that uses:

+ A sqlite database
+ ActiveRecord
+ RESTful routes
+ Sessions
+ Login/Logout

## Overview

The goal of this project is to build Fwitter (aka Flation Twitter).

You'll be implementing Fwitter using multiple objects that interact, including separate classes for User and Tweet.
 
Just like with Twitter, a user should be able to take any actions (except sign-up), unless they are logged in. Once a user is logged in, they should be able to create, edit and delete their own tweets, as well as view all the tweets.

There are controller tests to make sure that you 

## Group Project Instructions

*Instructions for how to work on a Group Project with Learn*

### Some Hints on Working Together 

Working on a software project with another person is not something to be taken lightly. While you are a fantastic coder solo, software development is a collaborative activity. Just like anything else, there is skill in collaborating on code. In the end, collaborating with another person boils down to three different styles:

  - Pair - Pair the entire time working linearly together
  - Pass - 1 person does 1 requirement and then the next person does the next one
  - Parallel - work on different parts at the same time by agreeing on interfaces and stubs and meeting in the middle

Remember! The goal at The Flatiron School is not to do, it is to *learn*. Make sure you have worked in all three styles of collaboration. We want you to learn how the different styles works, and make sure that together you and your partner understand every part of the code.

## Instructions

### File Structure

```
├── CONTRIBUTING.md
├── Gemfile
├── Gemfile.lock
├── LICENSE.md
├── README.md
├── Rakefile
├── app
│   ├── controllers
│   │   └── application_controller.rb
│   ├── models
│   │   ├── tweet.rb
│   │   └── user.rb
│   └── views
│       ├── index.erb
│       ├── layout.erb
│       ├── tweets
│       │   ├── create_tweet.erb
│       │   ├── edit_tweet.erb
│       │   ├── show_tweet.erb
│       │   └── tweets.erb
│       └── users
│           ├── create_user.erb
│           └── login.erb
├── config
│   └── environment.rb
├── config.ru
├── db
│   ├── development.sqlite
│   ├── migrate
│   │   ├── 20151124191332_create_users.rb
│   │   └── 20151124191334_create_tweets.rb
│   ├── schema.rb
│   └── test.sqlite
└── spec
    ├── controllers
    │   └── application_controller_spec.rb
    └── spec_helper.rb
```

### Gemfile and environment.rb

This project is supported by Bundler and includes a `Gemfile`.

Run bundle install before getting started on the project.

As this project has quite a few files, an `environment.rb` is included that loads all the code in your project along with Bundler. You do not ever need to edit this file. When you see require_relative `../config/environment`, that is how your environment and code are loaded.

### Models

You'll need to create two models in `app/models`, one `User` model and one `Tweet`. Both classes should inherit from `ActiveRecord::Base`.

### Migrations

You'll need to create two migrations to create the users and the tweets table.

Users should have a username, email, and password.

Tweets should have content, and a user_id.

### Associations

You'll need to set up the relationship between users and tweets. Think about how the user interacts with the tweets, what belongs to who?


### Home Page

You'll need a controller action to load the home page. You'll want to create a view that will eventually link to both a login page and signup page.

### Create Tweet

You'll need to create two controller actions, one to load the create tweet form, and one to process the form submission. The tweet should be created and saved to the database.

### Show Tweet

You'll need to create a controller action that displays the information for a single tweet. 

### Edit Tweet

You'll need to create two controller actions to edit a tweet: one to load the form to edit, and one to actually update the tweet entry in the database.

You'll want to create an edit link on the tweet show page.

### Delete Tweet

You'll need to two controller actions, one to display a form to delete a tweet, and one to process the form submission. 

The delete form doesn't need to have any input fields, just a submit button.

### Sessions

In the controller, you'll want to enable sessions.

### Sign Up

You'll need to create two controller actions, one to display the user signup and one to process the form submission. The controller action that processes the form submission should create the user and save it to the database.

The signup action should also log the user in and add the `user_id` to the sessions hash.

Make sure you add the Signup link to the home page.

### Log In

You'll need two more controller actions to process logging in: one to display the form to log in and one to log add the `user_id` to the sessions hash.

### Log Out

You'll need to create a controller action to process logging out.   

