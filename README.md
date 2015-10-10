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

## Why a framework, not a word processor?
We built Bookiza because we wanted to write books — all kinds of books — like we write our apps. Use our existing development toolchain to mint books using the project paradigm of software. It is as efficient as it can get! 

```
$ bookiza new MY-AWESOME-BOOK-NAME 24           # Gives a project with 24 blank pages in `manuscript/`.
$ bookiza server                  # Open http://localhost:6000 on your browser!
```

Open your project in your favorite editor and just write away! Once ready, simply:

```
$ bookiza push
$ bookiza publish
```

Bookiza is lightweight and *obsessive* about quick turnarounds. It optimizes towards design and performance and gives writers and comics designer a flexibility they haven't had for years. A framework that decidely leaves behind the old-school model of download-your-ebook-as-lifeless-artifacts (driven by an even older lobby group that wants physical books to remain on top!) and focus instead on a future where web and books are a unified resource that is easy to access, search and consumer anywhere.

** NOTE: Bookiza is not a framework for mobile or web development. 

Bookiza is also not a good solution if you need to write short-form essays (1-2 pages or so). We do not support books with less than 6 pages on our substrate platform [Bubblin Superbooks](https://bubbl.in). 

[Where does the Bookiza Framework fit in?]()

## Quick Start


```bash
$ npm install -g bookiza
```

Then, you can start a new Bookiza project by running:

```bash
$ bookiza new MY-AWESOME-BOOK-NAME 60
$ bookiza server
```
Open `http://localhost:6000` on your browser to see your freshly minted book!


## Library
Books created via Bookiza can be published directly to [Bubblin](https://bubbl.in) - our substrate platform for superbook readers. Bubblin is fully integrated with [Stripe Connect](https://stripe.com/connect) and supports payments in multiple countries. 

Find a selection of *exclusive* and [handpicked books](https://bubbl.in/books) brought to you by our community of futurists. 
 

## Community

* Follow [@bookiza on Twitter](https://twitter.com/bookiza)
* Have a question that's not a feature request or bug report? [Discuss on the Bookiza Forum](http://forum.Bookizaframework.com/)
* Read the [Bubblin Blog](http://medium.com/)
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