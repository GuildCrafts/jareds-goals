---
authors:
  - deadlyicon
issueNumber: 000
teamSize: 2
---

# Beginner Web App Architecture

## Challenge Rating

This goal will likely be within your ZPD if you...

- know beginner vanilla JavaScript
- feel comfortable with callbacks
- do not know how a web server works
- do not know what "rendering a template" means
- do not feel comfortable in express


## Description

This Goal is designed to introduce Web Application Concepts to you gradually over a series of stages.

This is goal is not designed to be fully completed the first time through. It is written expecting that you'll come back to this goal and do it faster and get father as you level up.

- Stage 1: just serving static assets
- Stage 2: serving dynamically rendered templates
- Stage 3: using layouts and partials
- Stage 4: renering data in a template
- Stage 5: using forms to submit data to the server
- Stage 6: tracking your visitors using cookies

__YOU MUST__:

  - __complete all the specs of each stage before moving on__
  - __get a code review after you complete each stage__


### Setup

0. Create a new repo
0. Copy this file into `README.md`
0. Make your first commit and push it up to Github

### Stage 1

In stage 1 were going to create a set of static files and then serve them with an super simple HTTP server called `serve`.


#### Learning Objectives

As you're completing Stage 1 make sure you're learning…

- how pages link to assets like stylsheets and images
- how relative paths work vs. absolute paths
- how to convert a relative path to an absolute path
- how the path in a url can map to a path on the unix filesystem
- how to use `The Chrome Developer Tools, Network tab` to inspect and debug the subsequent HTTP requests an html page makes to load associates assets
- that `index.html` is a special file name

#### Walkthrough

First install `serve`. Like this:

```sh
npm install -g serve
```

Next create the following files:

```
./public/assets/style.css
./public/assets/team.jpg
./public/assets/logo.png
./public/team.html
./public/about/index.html
./public/about/positions.html
```

You're welcome to use any images of any type but to make things easier here are two good ones:

- [team.jpg](https://www.natcom.org/uploadedImages/CommunicationCurrents_Articles/Volume_7/Oetzel_McDermott_pic_2.jpg)
- [logo.png](http://www.hut90.com/retool/assets/img/Logo_Humble_Bundle.png)

_Pro Tip: try using `curl IMAGE_URL > ./public/assets/team.jpg`_

Start the server by running this command

```sh
serve .
```

Now when you visit http://localhost:3000/ in your browser you should see a list of all of the files you just created within `./public`

These are the three pages you need to build:

- http://localhost:3000/team.html
- http://localhost:3000/about
- http://localhost:3000/about/positions.html

See the specs below for what you need to do.

#### Specs

You can move on to Stage 2 when…

  - you visit http://localhost:3000/team.html and see…
    - [ ] the words "Our Team" in red with a dark drop shadow
    - [ ] the logo image
    - [ ] the team image
  - you visit http://localhost:3000/about and see…
    - [ ] the words "About Page" in red with a dark drop shadow
    - [ ] the logo image
  - you visit http://localhost:3000/about/positions.html and see…
    - [ ] the words "About Position" in red with a dark drop shadow
    - [ ] the logo image


### Stage 2

In stage two we're going to move away from `serve` and build a simple `express` server that does the same thing. It will serve any static files within `./public`


### Learning Objectives

As you're completing Stage 2 make sure you're learning…

- how to setup a simple express server
- how to start an express server on any port you want
- how to to configure express to serve any files from a specifc directory
- how to run code after your express server has started


### Walkthrough

create your `package.json` file by running `npm init -y`

install `express` with the command `npm install --save express`

create the file `./app.js`

In this file you need to create an `express` server that serves static assets from the `./public` directory.

Google around to learn how to do this. Try reading some express tutorials. Try googling "Serving static files in Express". You should be able to do this in about 6-10 lines.


#### Specs

You can move on to Stage 3 when…

  - [ ] running `npm start` starts your express server
  - [ ] your express server starts on port 3000
  - [ ] when your express server starts, it prints "http://localhost:3000"
  - [ ] all of the specs from Stage 1 are still met


### Stage 3


In Stage 3 we're going to move our pages from static files into `express` routes and `ejs` templates

#### Learning Objectives

As you're completing Stage 3 make sure you're learning…

- how to define or register an `express` route
- how to respond to an HTTP request within `express`
- how to render a template in `express`

#### Walkthrough

Install ejs `npm install --save ejs`

Create a `./views` directory

Move the following files like so

```
./public/team.html -> ./views/team.ejs
./public/about/index.html -> ./views/about/index.ejs
./public/about/positions.html -> ./views/about/positions.ejs
```

Make sure you've removed the following files:

```
./public/team.html
./public/about/index.html
./public/about/positions.html
```

Create three `express` routes. One for each of our three pages.

#### Specs

You can move on to Stage 4 when…

- [ ] re-confirm all specs from Stage 1 & 2 are still met

#### Resources


### Stage 4

#### Learning Objectives

As you're completing Stage 4 make sure you're learning…

- the `ejs` syntax



------

more TBD

----

## Context

_Why is this goal important? How is it useful? What questions will it raise?_

## Specifications

_List of specifications (specs) for the completed goal. These are declarative sentences (statements) describing a feature of the final product._

- [ ] Spec one.
- [ ] Spec two.
- [ ] Spec three.
- [ ] The artifact produced is properly licensed, preferably with the [MIT license][mit-license].

## Quality Rubric

_What are some appropriate quality objectives for this goal? These are statements about the internal characteristics of the product that demonstrate fine design and craftspersonship, not its external features._

- Quality rubric one: point value
- Quality rubric two: point value
- Quality rubric three: point value

## Resources

_Include any resources (articles, books, tutorials, tools, videos, etc.) that are helpful for learners working on this goal._

[mit-license]: https://opensource.org/licenses/MIT


