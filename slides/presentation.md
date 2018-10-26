title: Web Development for Dinosaurs
subtitle: An Introduction to Modern Web Development
speaker: John Cleaver
company: Factivity, Inc.
email: johnc@factivity.com
conference: PUG Challenge Americas 2018
class: animation-fade
layout: true

<!-- This slide will serve as the base layout for all your slides -->
.bottom-bar[
  {{subtitle}} - {{conference}}
]

---

class: impact

# {{title}}
## {{subtitle}}

---

name: Speaker Bio
class: center, middle

# Who Am I?

## {{speaker}}
### Development Team Lead at {{company}}

---

name: Company Bio

# {{company}}

Factivity is a world leader in touch-based Manufacturing Execution Systems.

---

name: Agenda

# Agenda

- Web History Timeline
--

- Modern Web Application Tools
--

- Application Demo

???

My goal here is not to go through *everything* that goes into a modern web application- that would be it's own multiday workshop. My goal here is to at least give you a vocabulary and a starting point to be able to do your own reaserch.

It's difficult to do research if you don't even have the words to describe what you're trying to learn.

---

class: impact

# A Timeline of Web Development

---

class: middle, center

background-image: url(https://upload.wikimedia.org/wikipedia/commons/e/e8/Webdevelopmenttimeline.png)

---

| Era       | Page Types       | Language                                                 | Styling & Layout                | Apps                                        |
| --------- | ---------------- | -------------------------------------------------------- | ------------------------------- | ------------------------------------------- |
| 1990-1994 | Static           | HTML                                                     | HTML Attributes                 | None                                        |
| 1994-2005 | Dynamic          | PHP, Perl, JSP, ASP, C via CGI                           | CSS, Some JS                    | Flash, Shockwave, ActiveX, Java Applets     |
| 2005-2010 | Dynamic          | Ruby / Rails, Python / Django, PHP / Cake, ASP.NET / MVC | CSS, Jquery, AJAX               | Flash, Shockwave, Java Applets, Silverlight |
| 2010-2018 | Dynamic, WebApps | + Javascript / Meteor, Express, Angular, React, Vue      | CSS Preprocessors, JQuery, AJAX | HTML5 + JS                                  |

---

class: impact

# How did you get in to web development?

???

Raise of hands of people who worked in Dreamweaver or Front page and did layout using tables

People who tried using CSS and then went back to using tables?

People who had a geocities or angelfire web site?

Perl, PHP, Speedscript?

Flash or Coldfusion?

My Story:

* Started writing web pages with Frontpage
* Geocities, MySpace- lol
* Helped various clubs in college as well as some internal sites

---

class: impact

# Modern Front End Web Developement

---
name: why

# Why get in to Web Dev Now?

---
template: why

* Javascript is maturing and stabilizing
--

* Language Specification Changes are slowing
--

* Modern JS looks a lot more like traditional programming

---

template: why

* Major Frameworks are > 5 years old and back by larger corporations like MS and Google
  * Even older "less cool" frameworks still exist with updates
--

* HTML and CSS are still the best cross-platform UI toolkit
--

* Write Once, Run Everywhere is actually somewhat feasible now

---

class: impact

## It is impossible to begin to learn that which one thinks one already knows.

Epictetus, Greek Philosopher

---

# What does a Modern Web App Look Like?

* Components instead of full pages
* Distinct line between front end and backend
* Sometimes no backend at all
  
???

In some cases, you'll load all data to the client via a JSON file and persist changes to HTML5 localstorage. In other cases, you'll be communicating with a REST API written in a language you don't know or care about.

Examples: JS App and mobile app connnected to REST service running on an OpenEdge appserver

---

class: impact

# Modern JS Toolchain

---

# Editor

* There are many good editors available for front end development
* There are plenty of plugins for older editors and IDEs as well

Feel free to use what you are familiar with or try something new.

Recommendations: MS Visual Studio Code, Jetbrains IntelliJ, Sublime Text 3

---

# HTML5 and CSS3

.row[
.col-6[
* More semantic tags
* Local Storage API
* Canvas
* Flexbox layout
]

.col-6[
* Grid layout
* Smooth, native animations (with GPU acceleration)
* Service Workers
* WebSockets
]
]

---

# CSS Preprocessor

* Allows for the use of more programming-like features
* Variables, functions, mixins
* Browser compatibility

Examples: Less (More CSS-like) or Sass (More Ruby-like)

I prefer Sass, but if you know CSS super well, Less is probably a better choice.

---

# Front End Framework

* Optional, but makes your life easier
* Often deals with responsive layout, consistent styling, browser differences, and more
* Usually available in Less or Sass to make customizing and theming easier

Examples: Bootstrap, Foundation, Bulma

---

# "Compiler" - Babel

* Babel is a Javascript transpiler
* It converts modern JS (ES6 and ES2015) into the more widely understood ES5
* It lets you use the latest language features before they are available in browsers
* Allows use of alternate languages that compile to JS like MS's Typescript

???

Remember how I said that JS is becoming more like traditional development? Here's where we start into that part.

---

# Why bother with ES6?

* Module includes
* Arrow Syntax (`=>`) makes some code more readable 
  * (Esp. if you are familiar with functional code or lambdas in Java and Python)
* More data structures
* You'll see a lot of example code using it

???

Imagine trying to use OpenEdge without Using statements. That's what life is like without Module includes.

Sidenote: A problem I ran into when I was learning is that I saw the arrow syntax in some examples, but I wasn't using ES6 and I had no idea how to look it up.

---

# "Linker" - Webpack

* Webpack packages your source into a real application
* Combines all asset files into 1
* "Minifies"

???

In C development, the linker takes all of the object code and combines it into an executable.

Why is minifying important? Each file requires an HTTP request. Each HTTP request has a decent amount of overhead, so it reduces the number of requests and also reduces the total amount of data by removing whitespace and duplication.

---

# Package Manager - NPM / Yarn

* The JS world leans more Unix-y, so you'll use the package manager a lot
* Lots of free, open-source packages out there
* Both install packages, manage dependencies, and run utility scripts
* Yarn is a newer one that solves some problems with NPM, but is compatible with NPM


???

Why use a backend package manager with for front end development? The community decided and it works quite nicely with webpack.

---

# Javascript Framework

* Helps to break down code into re-usable components (think User Controls)
* Helps managing state
* Makes building dyanmic sites easier

Examples: React (Facebook), Angular (Google), Vue (Alibaba)

???

I prefer Vue because I think its docs are well written.

A note on Angular- Look for Angular, not Angularjs. Google did a major re-write and the naming is confusing.

---

class: impact

# You don't need to start with everything all at once!

???

Good News for you! You don't need to start with everything all at once. 

One of the problems that I ran into when learning Javascript was that most of he documentation is written for someone who already knows javascript. I finally got in when I found a framework that had documentation written for someone that didn't have experience. 

The average level of documentation has been going up- with more stability you can get bigger ROI for docs.

---

name: oldschool

# Old School JS

---

template: oldschool

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Example</title>
* <script src="index.js"></script>
</head>
<body>
  <h1>Hello from HTML!</h1>
</body>
</html>
```
---

template: oldschool

```javascript
// index.js
console.log("Hello from JavaScript!");
```

???

The script tag refers to a JS file in the same directory.

This is all you need to have javascript in a website.

---

name: jslib

# Adding a JS Library

---

template: jslib

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Example</title>
  <link rel="stylesheet" href="index.css">
* <script src="moment.min.js"></script>
  <script src="index.js"></script>
</head>
<body>
  <h1>Hello from HTML!</h1>
</body>
</html>
```

---
template: jslib

```javascript
// index.js
console.log("Hello from JavaScript!");
*console.log(moment().startOf('day').fromNow());
```

???

Scripts must be listed in order of dependency, so if you use moment.js, that must be loaded first.

This approach is super easy, but has the downside of being tedious to keep track of dependencies and update them.

---
name: npm
# Using NPM

???

This requires you to use the command line. If you aren't familiar with your OS's command line (PowerShell or Bash), then now is a good time to learn.
---
template: npm

## Create a package.json

```cmd
npm init
```

???

Node will ask some questions about your project here. You just accept the defaults for now.

---
template: npm
## Install packages
```cmd
npm install moment --save
```

???

Momentjs is now installed in `node_modules`. If you are using version control (you should), this should be in your ignore file. npm can recreate it for you at any time. Momentjs has also been added to your project.json file.
---
template: npm
## Add it to your HTML
```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Example</title>
* <script src="node_modules/moment/min/moment.min.js"></script>
  <script src="index.js"></script>
</head>
<body>
  <h1>Hello from HTML!</h1>
</body>
</html>
```
---
template: npm
## Hand it to a Coworker

```cmd
git clone sweet-project
cd sweet-project
npm install
```

---

name: bundle

# Bundling with Webpack

???

So, that part was great, but there are definitely some downsides. 
* We have to dig through the node_modules folder to find the package that we want
* We have to manually include each JS package in our HTML- completely separated from where we are using it

---

template: bundle

* JS did not includeany notion of include / using / import
* JS Modules had to be loaded into a global variable
  * Naming conflicts, global-state problems, etc.
* Nodejs introduced the idea that JS could include other JS files

```javascript
var moment = require('moment');
```

---

template: bundle

## How do we use that with client-side JS?

* A module bundler can look at include statements and build a JS file that has all the required code
* Webpack is the most popular today
  * Use by React, Vue, etc

---
template: bundle

## Installing

```cmd
npm install webpack webpack-cli --save-dev
```

Installs both webpack, a command line interface for webpack, and saves those as Development dependencies.

???

NPM and webpack have the concept of a development installation and a production installation. When you're app is in production, you don't need all the same utilities installed.

You'll now see `devDependencies` in your package.json

---
template: bundle

## Webpack it up

```cmd
./node_modules/.bin/webpack index.js --mode=development
```

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Example</title>
* <script src="dist/main.js"></script>
</head>
<body>
  <h1>Hello from HTML!</h1>
</body>
</html>
```

---
template: bundle

```javascript
// webpack.config.js
module.exports = {
  mode: 'development',
  entry: './index.js',
  output: {
    filename: 'main.js',
    publicPath: 'dist'
  }
};
```

???

Allows you to avoid typing that command line argument all the time.

Most JS things have config in wither JS or JSON

---

name: babel
# Transpiling

???

Having set up webpack, we can now use some other tools, like a transpiler

---
template: babel

## Installing

```cmd
npm install @babel/core @babel/preset-env babel-loader --save-dev
```

---
template: babel

```javascript
// webpack.config.js
module.exports = {
...
  },
* module: {
*   rules: [
*     {
*       test: /\.js$/,
*       exclude: /node_modules/,
*       use: {
*         loader: 'babel-loader',
*         options: {
*           presets: ['@babel/preset-env']
          }
        }
      }
    ]
  }
};
```

???

This looks a little more complex, but usually you won't be writing this manually, either. The bable loader is a plugin for webpack that runs the input into babel before passing it to webpack to be put into the dist directory.

1. Look for JS code
2. Use bable
3. Use the babel preset

---

template: babel

## What does this buy us?

--

Newer Features!

--

Format Strings
```javascript
var name = "Bob", time = "today";
console.log(`Hello ${name}, how are you ${time}?`);
```

--

Newer Imports

```javascript
import moment from 'moment';
```

???

This doesn't really look different, but it's a lot more advanced. You can actually pull out only the things that you use.

---

name: npm-scripts
# NPM Scripts

---
template: npm-scripts

NPM can also be told to be a task runner (think Ant)

```json
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack --progress --mode=production",
    "watch": "webpack --progress --watch"
  },
```

```cmd
npm run build
```

???

Now we can use some easier aliases for these long commands and parameters.

The `--progress` param will show the status of the command as it runs.

The `--watch` option is like the "Build on Save" feature- it watches changes in the file system and then builds when there is one.

---

template: npm-scripts

## Built-in Web Server

```json
"server": "webpack-dev-server --open"
```

```cmd
npm run server
```

???

Now you'll see your site at localhost on a default port.

---

# Demo: Vue CLI and Vue Projects

---

# Further Reading

* [How I learned to Stop Worrying and Love the Javascript EcoSystem](https://hackernoon.com/how-i-stopped-worrying-and-learned-to-love-the-javascript-ecosystem-692c51030342)
* [Modern Frontend Developer in 2018](https://medium.com/tech-tajawal/modern-frontend-developer-in-2018-4c2072fa2b9c)
* [Vuejs Guide](https://vuejs.org/v2/guide/)
* [Bootstrap Docs]()
* [Sass Docs]()

---

# Wrap Up

- Web Development Timeline
--

- Modern Development Technologies
--

- Code Examples

---

.row[
.col-4.center[
  ### Slides

  ![Slides](https://i.imgur.com/2GDHetT.png)
]

.col-4.center[
  ### Web Site

  ![Web Site](https://i.imgur.com/kN648bp.png)
]

.col-4.center[
  ### Code

  ![Code](https://i.imgur.com/1jBNvzL.png)
]

]

.row[
  .col-12.center[
# {{speaker}}
##{{email}}

Don't forget to fill out the surveys in the conference app!
  ]
]

???

Don't forget to fill out the surveys in the conference app!