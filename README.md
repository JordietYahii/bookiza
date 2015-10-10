# Bookiza

Cook your book like a pizza. Quick, beautiful and *everywhere*. 

The best place to start on Bookiza is our [Official Handbook](https://bubbl.in/cover/official-handbook-by-marvin-danig).


## Support
Superbooks written using Bookiza are [supported](https://bubbl.in/support) on every major device, tablet and desktop. Even HDTVs! All it needs is a modern browser.

Our current build yields best experience on iPads(iOS 7+) and Android 5.0+ tablets because, well, both mobiles & desktops (and TVs) aren't ideal an ideal situation for book readers.

## What is Bookiza?

Bookiza is an Open Source Book Writing Framework that is designed to *simplify* book-writing for you. *Publish* crazily beautiful, responsive and scalable books on the web using only the basic building-blocks: i.e. HTML, CSS and JavaScript (Yes, we got JS inside e-books!). 

Also, contrary to what a section of developers try to force on you, our books look like books too. Not some dumbass website or a silly hyperlink to a petty file that people need to download before they can read.

Check out our ![demo book](http://bubbl.in/cover/the-solar-system-by-marvin-danig) on your iPad, for example.

## Why a framework and not an editor?
We built Bookiza because we wanted to write books — all kinds of books — like we write our apps. Use our existing development toolchain to mint books using a project paradigm for our manuscript. It is as efficient as it can possibly get. 

```
$ bookiza new MY-AWESOME-BOOK-NAME 24           # Gives a project with 24 blank pages in `manuscript/`.
```

The open your project in your favorite editor and write away! Once you're ready:

```
$ bookiza push
$ bookiza publish
```
We wanted Bookiza to be lightweight and obsessive about book design, performance and flexibility. A framework that left behind old-school ebooks (closed models driven by arcane lobbyists!) modeled around files, lifeless artifacts, and focus instead on a future where web and books are single unified resource. Easy to access and mobile and tablets make for an ideal story .

It's important to realize that Bookiza is not a replacement for frameworks used for building mobile web apps. There are a lot
of great solutions that work well for websites, like [jQuery Mobile](http://jquerymobile.com/).

Bookiza is also not a good solution if you need to support older generation devices. Our compatibility *starts* at iOS 6 and Android 4.1. We will never support versions earlier than those. This is a framework for the future. Learn more: [Where does the Bookiza Framework fit in?](http://Bookizaframework.com/blog/where-does-the-Bookiza-framework-fit-in/)

## Quick Start

To start using Bookiza, you have two options: copy over the built JS and CSS files, or
use the `Bookiza` tool ([Bookiza-cli](https://github.com/driftyco/Bookiza-cli)) which can be installed through npm: _(You may need to prefix the command with `sudo` depending on your OS and setup.)_

```bash
$ npm install -g Bookiza
```

Then, you can start a new Bookiza project by running:

```bash
$ Bookiza start myproject
```

### Manual Start

- Download the latest **stable** release from:
  * The `release` folder of this repository
  * Bookiza CDN: [Latest Release](http://code.Bookizaframework.com/)
  * Using bower: `bower install Bookiza`
  * For [Meteor](https://www.meteor.com/) applications: `meteor add driftyco:Bookiza` 
- Download the **bleeding edge just-from-master release** from:
  * Bookiza CDN: [Nightly Build](http://code.Bookizaframework.com/#nightly)
  * Using bower: `bower install driftyco/Bookiza-bower#master`

Once you have a release, use `js/Bookiza.js`, `js/Bookiza-angular.js`, and `css/Bookiza.css`.

For most cases, you'll need AngularJS as well.  This is bundled in `js/angular/` and `js/angular-ui-router/`.


## Demos

 - [Bookiza Codepen.io Demos](http://codepen.io/Bookiza/public-list)


## Community

* Follow [@Bookizaframework on Twitter](https://twitter.com/Bookizaframework)
* Subscribe to the [Bookiza Newsletter](http://Bookizaframework.com/subscribe/)
* Have a question that's not a feature request or bug report? [Discuss on the Bookiza Forum](http://forum.Bookizaframework.com/)
* Read our [Blog](http://Bookizaframework.com/blog/)
* Have a feature request or find a bug? [Submit an issue](http://Bookizaframework.com/submit-issue/)


## Authors

Originally created by [Marvin Danig](http://twitter.com/marvindanig), Bookiza has seen hundreds of great [contributors](https://github.com/bookiza/bookiza/graphs/contributors) from around the world, including Bubblin Team Members [Veronica](http://bubbl.in/veronica), [Mike Hartington](http://twitter.com/mhartington), and [Tim Lancina](http://twitter.com/dopernicus).

## Development

* `npm install && npm install -g gulp protractor` to setup
* (if you wish to run end-to-end tests): `webdriver-manager update --chrome` to install the webdriver.
* `gulp` or `gulp build` to build
* `gulp docs` to generate docs (read Documentation below for how to test docs locally).
* `gulp build --release` to build with minification & strip debugs
* `gulp watch` to watch and rebuild on change
* `gulp karma` to test one-time
* `gulp karma-watch` to test and re-run on source change
* `gulp snapshot` to test e2e tests locally (run `gulp demos` first to generate e2e tests). Be sure to run `./node_modules/.bin/webdriver-manager update --chrome` to first install the chrome webdriver dependency.

### Documentation

* Documentation is generated into `dist/Bookiza-site`.  To test documentation properly, follow these steps:
  1. Clone Bookiza-site into `./dist/Bookiza-site`
    - `git clone git@github.com:driftyco/Bookiza-site dist/Bookiza-site`
  2. Start jekyll, telling it to rebuild whenever the site changes
    - `cd dist/Bookiza-site && jekyll serve -w`
  3. Go back to project root and build the docs
    - `gulp docs [--doc-version=(versionName|nightly)]`
  4. Open localhost:4000 and see your changes! Re-run `gulp docs` again whenever you change something, and jekyll will update the site

### Demos / Kitchen Sink

* The demo site is generated into `dist/Bookiza-demo`. To test the demos, follow these steps:
  1. Run `gulp demos [--demo-version=(versionName|nightly)]`
  2. Start an http server from `dist/Bookiza-demo`:
    - `cd dist/Bookiza-demo && python -m SimpleHTTPServer`
  3. Navigate to `http://localhost:8000/{versionName|nightly}` and use the demos
  4. Run `gulp demos` again whenever you change the demos

### Commit Conventions

* Uses these [commit conventions](http://github.com/ajoslin/conventional-changelog)

### Pushing New Release of Bookiza

- Almost all of the logic for releasing Bookiza is done on the Travis server
- To push a new release:
  1. Update package.json version to new version
  2. Generate changelog with `gulp changelog`
  3. Go through the changelog, and fix any mistakes or clarify any unclear commit messages
  4. Commit package.json and CHANGELOG.md and push to master
- Travis will detect that this commit changed the version in package.json and push out all necessary for this new release (tags, release files, site config, ...)

## LICENSE

Bookiza is licensed under the MIT Open Source license. For more information, see the LICENSE file in this repository.