## Sinatra versus Rails Exploration

### Setup:

First, clone down the Rails project:

```terminal
git clone https://github.com/turingschool/job-tracker.git rails_project
```

And then clone down the Sinatra project:

```terminal
git clone https://github.com/turingschool/bike-share.git sinatra_project
```
Now cd into each project, run `bundle` on each project, and you're ready to go. We will only be looking at the code base and not interacting with the app. If you wanted to run the server and interact with the app, you would need to create your database, migrate your migrations, etc.

### Exercise:

1. Take a look at this stripped down Sinatra app and this stripped down Rails app. How are they different and how are they similar? Identify 5 differences, and for each one describe 1-2 implications. What effect does that difference have for each framework? If you don't know exactly, draw on your knowledge and experience and make some educated guesses/inferences. Also, practice your research skills to look into the differences.
  - differences: rails app has multiple controllers, sintara app only one.(for the rails app - the Application_controller connects the others and that is the one you run.) Rails has helpers and mailers folders under app, sinatra does not.(Helper files are specific for views code in the application helper is included in all views. Mailer files are for email?) Rails has a bin folder with what looks like set up/config type files, sinatra does not.(bin contains "binstubs" which are wrappers around gem executables like 'bundle' which makes a gem run in the right environment in the app) In the spec folder, rails has a rails_helper file.(rails_helper is for specs which do depend on Rails - require it in your your specs - not spec_helper.). Rails has a vendor folder(holds code that you do not write.)

2. Consulting blogs and commentary you find online, identify 3 similarities between Rails and Sinatra.
  -they both use the MVC model
  -both use ActiveRecord
  -both use rspec for tests

3. Consulting blogs and commentary you find online, identify 3 things that distinguish Rails, advantages.
  -does much of the CRUD work for you
  -huge community to get answers/tutorials from
  -accommodates changes easier
  
4. In your Rails project, what does the `routes.rb` file inside of the `/config` directory do? What does this correlate to in our Sinatra app?
  -it defines the resources (erb files) needed for the various paths - similar to part of the controller file in sinatra
  
5. We teach Sinatra by adding some structures that Sinatra doesn’t need, but help you make the transition between Sinatra and Rails. What does a stripped down implementation of Sinatra look like, and what are the pieces we’ve added for educational purposes?
  -ActiveRecord - looks like a base sinatra app does not require activerecord.
  -loading a csv with data 
