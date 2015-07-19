## Synopsis

InlineVideo.js is intended to allow users on an iphone to play videos inline in the safari browser, circumventing the default fullscreen behavior.
This description should match descriptions added for package managers (Gemspec, package.json, etc.)

## Code Example

Simply include the library in your scripts. And then...

Code as usual, when you embed a video element in your page be sure to include the "playsinline" attribute, InlineVideo.js will automatically detect video elements with this attribute and replace them with the InlineVideo.js player if your users are on an iPhone.

```html
<video width="320" height="240" controls playsinline webkit-playsinline>
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.ogg" type="video/ogg">
</video>
```

InlineVideo.js works by detecting videos that should play inline for users on an iPhone, then transforming the video elements into canvas elements. InlineVideo.js draws each frame of the video to this canvas element instead of playing the video, that way IOS never tries to go into "full screen native player mode."

## Motivation

This project was started because I believe developers should have to freedom to choose if their videos are meant to play full screen or not. I understand the reasoning behind apples choices for the iphone, but sometimes a design or interactive experience calls for an inline video and iPhone users shouldn't be left out. Also, with the introduction of IOS 8 and webGL enabled by default, you would think we'd be able to use video textures...

## Installation

Make sure you include jQuery and the InlineVideo.js file in your scripts:

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
<script src="js/inline-video-player.js"></script>
```

## API Reference

Depending on the size of the project, if it is small and simple enough the reference docs can be added to the README. For medium size to larger projects it is important to at least provide a link to where the API reference docs live.

## Tests

Describe and show how to run the tests with code examples.

## Contributors

Contributors are always welcome. This library is nowhere near finished, I'd love the help of the community to make this video player a reality.

There's some important conversation happening here: [Chromium developers forum](https://code.google.com/p/chromium/issues/detail?id=395206)

Also there are a couple of example uses of inline video being used in the wild:

[KRPano Cloud Demo](http://krpano.com/krpanocloud/video/airpano/index.html)
[takeyourdose.com](http://www.takeyourdose.com/en)

If you'd like to get involved message me, submit a pull request or issue.

## License

The MIT License (MIT)

Copyright (c) 2015 Mike Newell

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.