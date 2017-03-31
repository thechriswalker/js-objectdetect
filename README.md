# haar-detect

In-browser object detection. If you are server-side any opencv binding would be better, even if I made this node.js compatible.

This library base on code from https://github.com/mtschirs/js-objectdetect.

However for me that library did not provide what I wanted.

  - I did not want all the classifiers it provides (I want to train my own)
  - I wanted commonjs, and npm-able module structure.

So this repo contains 2 packages:

  - `haar-loader`: a webpack2 loader that convert XML haar cascades to JS modules.
  - `haar-detect`: uses the compiled cascades to detect objects in images/urls/files/blobs.

With both of them your project can load XML cascade files as javascript during the bundling and use the `haar-detect` module to perform client-side object detections.
