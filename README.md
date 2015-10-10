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

## Features

  - Available everywhere, naturally hosted on Bubblin or on your own site. (Via a [spine_url](https://bubblin.github.io/))
  - Responsive by default
  - Beautiful flexible typography, @font-faces and a plethora of [templates]() to choose from
  - Easier to maintain, no reflow headaches!
  - Multi-Language & multi-platform 
  - Full Cover 
  - CDN compatibility 
  - Full-bleed Magazine Imagery
  - In-page JavaScript programming
  - Any content, any mode: WebGL, Latex, Katex, Markdown or plain old HTML.
  - Supported on all major devices and browsers
      Searchable & Indexable
      Comics & Animation support: white, sepia, night


## The library
Books created via Bookiza can be published directly on [Bubblin](https://bubbl.in) - our substrate platform for book lovers. Or  host it on your own website! Bubblin comes feature packed and pre-integrated with [Stripe Connect](https://stripe.com/connect). 

Find a selection of *exclusive* and [handpicked books](https://bubbl.in/books) brought to you by our community of futurists. 
 

## Community

* Follow [@bookiza on Twitter](https://twitter.com/bookiza)
* Have a question that's not a feature request or bug report? [Discuss on the Bookiza Forum](http://forum.Bookizaframework.com/)
* Read the [Bubblin Blog](http://medium.com/)
* Have a feature request or find a bug? [Submit an issue](http://Bookizaframework.com/submit-issue/)


## Authors

Originally created by [Marvin Danig](http://twitter.com/marvindanig), Bookiza has seen hundreds of [contributions](https://github.com/bookiza/bookiza/graphs/contributors) from around the world, including major ones from [Veronica](http://bubbl.in/veronica) and [Dave](https://bubbl.in/).

## Development


### Documentation


### Demos / Kitchen Sink


### Commit Conventions


### Pushing New Release of Bookiza


## LICENSE

Bookiza is licensed under the MIT Open Source license. For more information, see the LICENSE file in this repository.