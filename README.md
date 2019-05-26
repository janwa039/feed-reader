
# Feed Reader Testing

This project demonstrates testing with [Jasmine](https://jasmine.github.io/).

The project code base is from Udacity which has contained a web-based application that reads RSS feeds and 
what was needed was to test this application using jasmine.

# Project Starter

[feed Reader](http://github.com/udacity/frontend-nanodegree-feedreader)

# How to Run Application

Run locally :

* clone or download or  the repository
* open index.html file in your browser
* Find the test results in small section at the bottom of the page  of your browser.

# About the tests

## Test Suite "The Menu"

Figured what classes where hidden or related to this test by inspecting the heml elements and css elements in the Chrome dev tools, I found the program show and hide the slide menu by toggling class 'menu-hidden' on he documnet body.

By default, the body should be with class menu-hidden. By using jQuery to select the body element and get the class with attr. So that the test should detect if the body tag contains 'menu-hidden' to check if the toggleClass function runs properly.

The click() event is used to check if the 'menu-hidden' class exists to ensure the function goes well.

## Test Suite "Initial Entries"

The loadFeed() is asynchronous so the test should use beforeEach() and done() to ensure the loadFeed() runs in the test.

Since .entry is an rendered element when feed successfully initialised, by checking if the .feed HTML after loading can see if the entries has been loaded properly.


By calling loadFeed(0, function(...)) the test load the first feed which contains initial entries for detection.
By calling loadFeed(1, function(...)) the test load the second feed which contains the second entry for detection.

After this, there is an expectation that  second feed content should be different from the first feed. So that by comparing the rendered HTML content, we can check if the program loads a different feed with the function instead the same one.

## Test Wuite "New Feed Selection"

There are more than one feed in the allFeeds. The loadFeed() function load specified feed with the index.
