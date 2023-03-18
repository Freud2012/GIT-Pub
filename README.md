# GIT-Pub

🔴 *Remember to commit!*

****Setting up your "database"****
When setting up, you created a file called `drinks.js`in your `models`folder. For now, this will act as our "database".

**Inside `drinks.js`, paste the following data *as is***You may notice that the image url's are missing a certain something, but this is *intentional!* Do **not** directly edit any of the provided data inside your `drinks.js`file. We'll fix things programmatically!

`D`r
• Set up your 'database' so that it can be exported to your `server.js`and then be required by your `server.js`
• Set this 'database' to a variable called drinks in your `server.js`file
• Create a get route `/drinks`that will `res.send(drinks)`, which will display your drinks data as json in the browser🔴 *Remember to commit!*
****Setting up your index view****
• Instead of displaying json at your /drinks route, you should serve the `drinks_index.ejs`file you created that will display your drinks
**In `drinks_index.ejs`**
• Start with your HTML boilerplate
• Add an `<h1>`that describes the page, i.e. `Welcome to gitPub`
• Add a `<style>`tag so you can write some CSS *directly* inside your `html`file.
    ◦ See more info [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style)
    ◦ Wondering how you can connect a separate `.css`file? We'll learn about it later, or you can look at the Hungry for More section that will point you in the right direction to research!
• Add a `background-color`and text `color`to to `body`so that you can ensure your css is working correctly
    ◦ For example:

`<style type="text/css">
  body {
    color: blanchedalmond;
    background-color: steelblue;
  }
</style>`
• Change your `/drinks`route to `res.render`your `drinks_index.ejs`
• In your browser, go to `localhost:3000/drinks`to make sure you're rendering the `drinks_index.ejs`file!🔴 *Remember to commit!*
****Setting up your index view to show your drinks data****
**In your `drinks_index.ejs`, make it so that you can see:***
• The name of each drink as a list item inside an unordered list
• This list should be dynamically rendered by ejs based on your data from your 'database'
• You'll notice the drink names aren't properly capitalized! Let's fix that! Manipulate the data programatically to capitalize the first letter of their names🔴 *Remember to commit!*
****Setting up your show route****
**In `server.js`**
• Add a new get route for `/drinks/:id`
• For now, just make sure it works correctly by having the route `res.send(req.params.id)`
    ◦ So that when you go to `localhost:3000/drinks/whatever`, `whatever`should show up in the browser🔴 *Remember to commit!*
****Linking `drinks_index.ejs`to `drinks_show.ejs`**
**In `index.ejs`**
• Make each listed drink a link that will go to the route `/drinks/x`, where 'x' is the array position of the drink in the data array. This should be set dynamically with ejs!
• When you click the link, it show go to the show route and the index number corresponding to the drink's array position should be displayed🔴 *Remember to commit!*
****Rendering an individual drink in the show view****
**In `show.ejs`**
• Copy/paste your code from your `drinks_index.ejs`into your `drinks_show.ejs`
    ◦ surely, there must be a better way to not copy/paste; are you wondering if there is something in the hungry for more section about this?
• Change all your html code inside your `drinks_show.ejs`file's `<body>`so that:
    ◦ Your `h1`tag says "At foo bar"
    ◦ There's an `h2`tag that should display the name of the drink
    ◦ There's an image tag that should display the image of the drink
    ◦ There's an `h3`tag that should display the price of the drink
    ◦ Add an anchor tag with the text of back, that will take you back to your index.ejs view
**In `server.js`**
• Update the get route to render the `show`view with the drinks data
Oh no! If you check on the browser, the image is broken because in our database the image links don't have the `.png`ending, let's fix that programatically!
• Without going back to the `drinks.js`database file and editing it there, add on `.png`to the end of the drink's image data programatically
    ◦ *Thought question:* Where should you do this? server.js or show.ejs? Or does it not matter, i.e. will either one work?🔴 *Remember to commit!*
Our gitPub is missing some food, so let's add some!
1. Add a second 'database' by creating a `food.js`file in the `models`folder and use the following data:

1. List the food under your drinks list on the index ( food_index.js )
2. Make them clickable as well to go to their show page ( food_show.js )

🔴 *Remember to commit!*

### ****Hungry for More?****

1. Look into EJS partials and try to implement them in your app! Create a partial for the head, and include it in both your views. We'll have a morning exercise covering partials later in the unit, but if you'd like to look into it now, a nice walkthrough can be found [here (starts about 1/4 of the way down)](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)

2. Style your application with Bootstrap or any other CSS framework! Or really jazz up your app by adding some hand-rolled flourishes with css animations, jQuery and more!

3. Sign up for [Code Wars](https://www.codewars.com/) and try out a challenge (or a few!) in order to keep honing your JavaScript skills!

4. Learn about express static in order to learn how to link a css file to your app (we'll be covering it tomorrow, but if you're interested in looking into it now: [read those docs!](https://expressjs.com/en/starter/static-files.html)) Go ahead and dive right in!

****Style your app****

• Just use style tags for now!
• STRETCH: Add a little more flair to your gitPub app by styling it with a little bit of CSS. Doesn't have to be anything crazy, just make it so that it's not the default styling!

****Deliverables****

An express app that meets all the user stories outlined in the beginning of this markdown.
****Technical Requirements****

*Your app MUST run without syntax errors. If there are errors you can't solve, comment them out and leave a comment above explaining what is wrong*
