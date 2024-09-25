PleaseWait.js
===========
A simple library to show your users a beautiful splash page while your application loads.

Documentation and Demo
---------------------
Documentation and demo can be found [here](http://pathgather.github.io/please-wait/).

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [API](#api)
- [Customization](#customization)
- [Browser Compatibility](#browser-compatibility)
- [Contributing](#contributing)
- [Changelog](#changelog)

## Installation

You can install PleaseWait.js using npm:

```bash
npm install please-wait
```

## Usage

After installing the package, you can import and use it in your JavaScript file:

```javascript
import pleaseWait from 'please-wait';

const loading_screen = pleaseWait({
  logo: "path/to/your/logo.png",
  backgroundColor: '#f46d3b',
  loadingHtml: "<p class='loading-message'>A loading message.</p>"
});

// Later, when your application is ready:
loading_screen.finish();
```

## API

- `pleaseWait(options)`: Initialize the loading screen
- `loading_screen.finish()`: Hide the loading screen
- `loading_screen.updateOption(option, value)`: Update a single option
- `loading_screen.updateOptions(options)`: Update multiple options

## Customization

PleaseWait.js offers several customization options:

- `backgroundColor`: Set the background color of the loading screen
- `logo`: Path to your logo image
- `loadingHtml`: Custom HTML for the loading message
- `template`: Custom HTML template for the entire loading screen

Example:

```javascript
pleaseWait({
  logo: "images/logo.png",
  backgroundColor: '#000000',
  loadingHtml: "<div class='sk-spinner sk-spinner-wave'><div class='sk-rect1'></div><div class='sk-rect2'></div><div class='sk-rect3'></div><div class='sk-rect4'></div><div class='sk-rect5'></div></div>",
  template: `
    <div class="pg-loading-inner">
      <div class="pg-loading-center-outer">
        <div class="pg-loading-center-middle">
          <h1 class="pg-loading-logo-header">
            <img class="pg-loading-logo"></img>
          </h1>
          <div class="pg-loading-html"></div>
        </div>
      </div>
    </div>
  `
});
```

## Browser Compatibility

PleaseWait.js is compatible with modern browsers including:

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

We welcome contributions to PleaseWait.js! Please follow these steps:

1. Fork the repository
2. Create a new branch: `git checkout -b feature-branch-name`
3. Make your changes and commit them: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-branch-name`
5. Submit a pull request

## Changelog

### v0.0.5
- Initial public release

About Pathgather
---------------------
Pathgather is an NYC-based startup building a platform that dramatically accelerates learning for enterprises by bringing employees, training content, and existing enterprise systems into one engaging platform.

Every Friday, we work on open-source software (our own or other projects). Want to join our always growing team? Peruse our [current opportunities](http://www.pathgather.com/jobs/) or reach out to us at <tech@pathgather.com>!
