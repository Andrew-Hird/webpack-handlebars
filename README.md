# Boilerplate: webpack & Handlebars

Phase 2 boilerplate project with:

 - Handlebars
 - tape
 - tape-run
 - tap-spec
 - webpack
 - webpack-dev-server


## Install

```
npm install
npm run dev
```
# webpack Handlebars Stories

User stories for client-side rendering practice.


## Install

Enter the commands below in your terminal to get started:

```shell
git clone https://github.com/[your-cohort]/boilerplate-webpack-handlebars
mv boilerplate-webpack-handlebars webpack-handlebars
cd webpack-handlebars
npm install
npm run dev
```

If you would like to push changes back to your own repository, you'll need to create an empty repository in your GitHub and [change](https://help.github.com/articles/changing-a-remote-s-url/) the `origin` remote to point to that repo:

```shell
git remote set-url origin https://github.com/YOUR-USERNAME/knex-relationships
```

Visit http://localhost:8080 in your browser. If all went well, you should see a list of wombles.


## MVP

_As a user, I want to see a header on the index page with the page's title and subtitle included so that I know which page I'm on._
 - You'll need to create a new Handlebars template in `src/templates` and `require` it from `src/index.js`.
 - Pass the template function an object with some data. For example:

```js
var headerTemplate = require('./templates/header.hbs')

var header = headerTemplate({
  title: 'Wombles',
  subtitle: 'They clean up'
})
```

_As a user, I want to see a footer on the index page with some copyright and contact details included so I know who to blame._
 - Create another template as above

_As a user, I want to see a sidebar with a list of links that I can populate so I can customise my page navigation._
 - Yet another template
 - For now, keep the links in a JavaScript object or array


## Try these next

_As a user, I want to see details for each womble when I click on their name (**without** being redirected to another page) so that I can find out more about them._
 - You'll need to add another property to the womble object, `details`
 - Womble names will need an event listener for the `click` event
 - You should append the details to the womble's `<li>` element in some way. You might like to try using partials: check out the [handlebars-loader](https://github.com/pcardune/handlebars-loader) docs for more detail, but it should resolve them automatically if you create a `./src/templates/partials/myPartial.hbs` file (for example).


## Stretch

_As a user, I'd like to switch to an 'About' page when I click the 'About' link (**without** a browser reload) so that I can learn more about the site._
 - This is getting into Single Page Application (SPA) territory. The goal is to replace/refresh the content using JavaScript.
 - You can re-use the header, footer, and sidebar templates: just change the data objects passed to them as required.
