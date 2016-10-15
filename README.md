# Welcome to Me - A personal website

Check it out at: https://agile-reef-73160.herokuapp.com/

The best part about creating a basic personal website is the fruitful plethora of resources available to you on the web! I decided to use Bootstrap (which has a lot of styling and shared components you can use), as well as node/ejs partials (templates so that you don't have to repeat a lot of code on your pages), and a few other things to help me get started. I always find that the toughest part about a website like this is coming up with reasonable content and then tackling it piece by piece. It won't look like amazing at first, so give yourself time to learn your way around the code before beautifying!!

Feel free to ask me questions as you go or just poke around and see what you like. Here are some notable things:

## Bootstrap Nav etc
If you're going to use Bootstrap, don't forget to add the script tag in your `<head>`, or the styles won't come in. Also, add it before the reference to your own css file. Mine is in `views/partials/header.ejs` which gets put into the head of every page. The [bootstrap nav](http://getbootstrap.com/components/#glyphicons) is easy to use and looks great. 

## Node Routing
[Node routing](http://expressjs.com/en/guide/routing.html) is how I switch between pages when clicking on the navigation tabs. My routes live in `index.js`. Don't forget to restart your server whenever you make any changes to the `index.js` server file, else nothing you do will be picked up when you're running locally.

## EJS Templates
If you don't want to rewrite the same code in multiple files (eg. a header, nav, or footer), templating is gonna be your best friend. EJS is a templating language (there are many) that looks pretty similar to normal html, but there are a few extra things you can do. I wrote a footer, header, and nav in `views/partials` and they get injected into my pages (in `views/pages`) by writing `<% include ../partials/header %>`. [Here](https://scotch.io/tutorials/use-ejs-to-template-your-node-application) is a tutorial I found helpful for ejs partials/templates to help with reusable code.

## Other helpful things
If you're looking for some boss fonts, check out [Google Fonts](https://fonts.google.com/), where you can browse around for some free ones and then just insert the script tag in your `<head>` of the ones that you like (mine lives in `views/partials/header.ejs`). 

If you're looking for some sweet colors to add to your website, [this](http://www.rapidtables.com/web/color/RGB_Color.htm) is a nice way to figure out the rgb and hex values. Finally, here is another icon service. Bootstrap provides a bunch of icons with glyphicons, but all my sweet social icons came from [FontAwesome](http://fortawesome.github.io/Font-Awesome/get-started/), which is a super easy to use and free service

## Git Commit
When you make some changes, remember to commit and push them up to master. Once you want to see the good stuff on heroku, do `git push heroku master` and then `heroku open` WOW EASY.

## Simple first steps
1. Go to `views/partials/header.ejs` and replace my name with yours so it appears in the title of tab.
2. Find some cool [Google Fonts](https://fonts.google.com/) and replace `Rubik` and `Open+Sans` with whatever you like best (also in `views/partials/header.ejs`) to import them, and change them in the css file (`public/stylesheets/main.css`) to see them on the different parts of the app. `jumbotron` is the big title on each page, and `body` is everything else.
3. Replace my bio with yours in `views/pages/index.ejs`. Maybe even insert a photo!
4. Add another project to my projects page! Just copy and paste the chunk of code within the `<div class="general-container projects-container">` tag and change the text/image!
5. Do you have Instagram? Facebook? Find the [FontAwesome icon of your choice](http://fontawesome.io/icons/) and add a link to whatever account you want in the contacts page (also maybe change the other links too lol)
6. Do you have hobbies? Maybe you're into photography? Add another tab to the nav! There are several steps here: (1) add another `.ejs` file to `views/pages`, (2) set up the route in `index.js` (3) add it to the `views/partials/nav.ejs` file (4) restart node (ctrl+c to kill it from your terminal, `heroku local web` to start it back up)

Good luck, ask for help, and google away!
