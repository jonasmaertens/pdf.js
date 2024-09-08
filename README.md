# PDF.js 

[PDF.js](https://mozilla.github.io/pdf.js/) is a Portable Document Format (PDF) viewer that is built with HTML5.

This fork of pdf.js includes [PR #18681](https://github.com/mozilla/pdf.js/pull/18681) to use manifest v3 for the Chrome extension and modified changes from [this fork](https://github.com/belinghy/pdf.js) to include a hover preview feature for document links.

#### Chrome

+ Build Your Own - Get the code as explained below and issue `npx gulp chromium`. Then open
Chrome, go to `Tools > Extension` and load the (unpackaged) extension from the
directory `build/chromium`.

## Getting the Code

To get a local copy of the current code, clone it using git:

    $ git clone <this-repo>
    $ cd pdf.js

Next, install Node.js via the [official package](https://nodejs.org) or via
[nvm](https://github.com/creationix/nvm). If everything worked out, install
all dependencies for PDF.js:

    $ npm install

> [!NOTE]
> On MacOS M1/M2 you may see some `node-gyp`-related errors when running `npm install`. This is because one of our dependencies, `"canvas"`, does not provide pre-built binaries for this platform and instead `npm` will try to build it from source. Please make sure to first install the necessary native dependencies using `brew`: https://github.com/Automattic/node-canvas#compiling.
