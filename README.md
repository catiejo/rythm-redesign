# \<rythm-redesign\>

A side project recreating elements of Rythm's website (www.rythm.co) using Polymer prototyping.

The final product can be viewed at: [rythm-1355.appspot.com](rythm-1355.appspot.com)

*HOWEVER* I encourage you to check the "demo" video located in the `screenshots` directory. Due to [an issue I filed](https://github.com/Polymer/polymer-cli/issues/292) with one of the elements I'm using in this prototype, I wasn't able to deploy the app with the same functionality included in this repository--most of the animatins are missing from the deployed version. If you'd like to build the app locally, however, it is fully functional. Simply follow the instructions below (starting with "Installing the Polymer CLI").

## My Process
I decided to do a one-week sprint to see how much I could learn about Rythm's website. This included looking at the existing website, mocking up a wireframe in Adobe Illustrator, and using Polymer to build the site as close to my original specs as I could.

### Scope 
Because of my time constraints, I chose to only implement a single page rather than the entire website. This page is also much more simplistic than the actual website, again because of the aforementioned time constraings. However, I also wanted to use this opportunity to apply some concepts I'd recently struggled with, including:
* CSS transitions
* Polymer (I'd explored Polymer prior to this project, but never got more than demos working)
* Vertical alignment (this didn't make it into the final prototype, but I learned how to do it along the way)
* How positioning works in CSS (the difference between relative and absolute positioning, for example)
* Animated page elements (I ended up using Polymer for this)

### Design Rationale
On Rythm's actual website, the landing page functions as a scrollable table of contents--each section of the landing page entices you toward a different part of the website (e.g. the product, the science, the jobs, etc.). While this is really effective, I chose to take a slightly different route, focusing on desiging for a first-time visitor to the site. My final page consists of three sections:

1. __Start with why.__ Tell her why she cares about the product (for example, finding a good night's sleep).
2. __Explain what it is.__ Now that she knows the need being met, briefly explain how the product meets those needs.
3. __Gain credibility with endorsements.__ Rythm's gotten a lot of really great press, so I wanted to make sure those quotes were showcased.

Despite this change, I also wanted to preserve a lot of Rythm's original look and feel, so I tried to keep the following elements prevalent in my design:
* Immersive product photos as backgrounds
* Sans-serif font choices
* Beautiful, interactive elements (especially the animated app screens!)
* A soft, professional color palette

### Conclusions + Future Work
I learned a ton from this project, and there's still a lot I want to experiment with. Most notably, I didn't have enough time to make appearing/disappearing quotes. I have color-changing logos for each of the quote sources, but the endorsement quotes aren't currently displaying when you hover over their associated icons/ I know how to do this in javascript, but I want to challenge myself to see if I can make it work in CSS. I have started developing that in a separate branch, and will merge my changes back in when I get it working.

I would also like to do some more robust testing--I did manual testing for the methods in my polymer element, as well as page renderings at different sizes, but a full application would of course have a lot more exhaustive testing suite.

# If you'd like to build this project yourself...

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

## Viewing Your Application

```
$ polymer serve --open
```

## Building Your Application

```
$ polymer build
```

This will create a `build/` folder with `bundled/` and `unbundled/` sub-folders
containing a bundled (Vulcanized) and unbundled builds, both run through HTML,
CSS, and JS optimizers.

You can serve the built versions by giving `polymer serve` a folder to serve
from:

```
$ polymer serve build/bundled
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
