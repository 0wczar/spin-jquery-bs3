# SPIN HTML/CSS - now is free!
![image](https://user-images.githubusercontent.com/2330394/62898026-d0d47d80-bd54-11e9-852e-df8213ea1ea9.png)
### Intro
SPIN Admin/Dashboard Theme with a minimalist design and innovative Dark UI will let you build an amazing and powerful application with great UI. Perfectly designed for large scale applications, with detailed step by step documentation.
It is built based on the latest standards and recommendations. It is powered by Bootstrap framework 3.x, which is currently one of the most popular framework in the world.

## Installation
1. Make sure you have Ruby installed (Ruby DevKit on Windows also), Jekyll gem, Bundler gem (`gem install bundler`),  Node, Bower and Gulp
2. Clone this repository `git clone https://github.com/0wczar/spin.jekyll.git`
3. In the terminal navigate to the cloned repository directory
4. Run `npm install` to install NPM packages
5. Run `bower install` to install Bower packages
6. Run `gulp bower` to attach Bower packages to Jekyll
7. Run `bundler` to install required Gems
8. *(Option)* Run `gulp` to start Jekyll with HTML/JS/Styles watcher. To start watching ONLY HTML files run `gulp jekyll`


## Adding Bower Components
1. In the terminal navigate to project directory
2. Run `bower install <package-name> --save` for example `bower install jquery --save`. The Bower packages list can be found here - http://bower.io/search/
3. When the install is complete run `gulp bower` to attach the new library.


## Adding Plugins Less/Sass
1. The plugins Sass files should be placed in `/src/assets/scss/<plugin-name>`
2. The compiled css should be placed in `/src/assets/stylesheets/<plugin-name>.css`
3. This generated custom style should be linked in the `/src/_includes/head.html` for example ` <link rel="stylesheet" href="assets/stylesheets/select2-bootstrap.css">`


## Creating New Pages
1. New HTML pages should be added to `/src` folder for example `/src/new-page.html`
2. The new page should have the variables on the top required is `layout: default`. Other usable variables are: `bodyClasses` which adds appropriate classes to the body tag, `defaultContainer` which adds specific container to navbar and footer and `title` which is injected into head and can be used in the content via `{{ page.title }}`. Example: ![alt text](http://content.screencast.com/users/unskilled/folders/Jing/media/1571975c-ddf0-4013-8543-7fabd7a25cc9/2016-05-23_1527.png)
3. The added page should be linked in the sidebar like this: 
![alt text](http://content.screencast.com/users/unskilled/folders/Jing/media/8cc6b248-731d-422e-a123-13111a2ab57a/2016-05-24_1153.png "Sidebar Link Example") Example Link: `<li class="{% if page.url == "/default.html" %}active{% endif %}"><a href="/default.html"><span class="nav-label">Default</span></a></li>`
4. To acces this page you can use this url: `localhost:3000/new-page/`

## Vanilla Source (Full App Light)
1. In main folder enter in terminal `gulp build:vanilla`
2. Go to folder `cd /site`
3. Then `npm install`
4. Next `bower install`
5. Next `gulp build`
6. Ready source available in folder `/dist`

## Seed Source (Starter Dev) (_inludes/starter...)
1. In main folder enter in terminal `gulp build:seed`
2. Ready source available in folder `/starter` 

## GIT Reset
1. Go to folder with project ` cd /your_catalog`
2. Enter `git reset --hard origin/master`
3. Pull via Github Dekstop

## Faker New Options
1. Example: 25 - 07 - 2016 - 12:03 (12h) `<span data-faker="{{date.day}} {{date.monthDigit}} {{date.year}} {{date.time}}"></span>`
2. Example: Months: Jan, Feb, Mar, etc... `data-faker="[[date.monthShort]]"`
3. Examples: Days: Mon, Tue, Wed, etc... `data-faker="[[date.weekdayShort]]"`
4. Example: 1% - 100%: `<span data-faker="[[random.percentage]]"><span>`
5. Example: 0% - 100.0%: `<span data-faker="[[random.percentagePoint]]"><span>`
