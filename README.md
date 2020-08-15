# Simple PWA
## Simple Progressive Web App (PWA) template

### What is this?
Simple PWA is a Progressive Web App template that provides the minimum file structure needed to create a PWA. These files collectively represent a [reliable](https://web.dev/what-are-pwas/#reliable) and [installable](https://web.dev/what-are-pwas/#installable) web application. It's up to you to add functionality to make it [capable](https://web.dev/what-are-pwas/#capable).

Simple PWA is "offline-first", using a ["cache falling back to the network"](https://developers.google.com/web/ilt/pwa/caching-files-with-service-worker#cache_falling_back_to_the_network) caching strategy, which means any files specified in [`sw.js`](https://github.com/nikkifurls/simple-pwa/blob/master/sw.js#L10-L46) will be cached, and therefore, accessible offline. Non-cached requests (including non-GET requests, as they cannot be cached), will not be accessible offline, and instead, will ping the network or fail if there is no network available. In [`sw.js`](https://github.com/nikkifurls/simple-pwa/blob/master/sw.js), the value of [`cacheName`](https://github.com/nikkifurls/simple-pwa/blob/master/sw.js#L1) should be changed whenever the app is updated in order to force the cache to update from the network.

- `android-chrome-36x36.png` Favicon, Android Chrome M39+ with 0.75 screen density
- `android-chrome-48x48.png` Favicon, Android Chrome M39+ with 1.0 screen density
- `android-chrome-72x72.png` Favicon, Android Chrome M39+ with 1.5 screen density
- `android-chrome-96x96.png` Favicon, Android Chrome M39+ with 2.0 screen density
- `android-chrome-144x144.png` Favicon, Android Chrome M39+ with 3.0 screen density
- `android-chrome-192x192.png` Favicon, Android Chrome M39+ with 4.0 screen density
- `android-chrome-256x256.png` Favicon, Android Chrome M47+ Splash screen with 1.5 screen density
- `android-chrome-384x384.png` Favicon, Android Chrome M47+ Splash screen with 3.0 screen density
- `android-chrome-512x512.png` Favicon, Android Chrome M47+ Splash screen with 4.0 screen density
- `apple-touch-icon.png` Favicon, Apple default
- `apple-touch-icon-57x57.png` Apple iPhone, Non-retina with iOS6 or prior
- `apple-touch-icon-60x60.png` Apple iPhone, Non-retina with iOS7
- `apple-touch-icon-72x72.png` Apple iPad, Non-retina with iOS6 or prior
- `apple-touch-icon-76x76.png` Apple iPad, Non-retina with iOS7
- `apple-touch-icon-114x114.png` Apple iPhone, Retina with iOS6 or prior
- `apple-touch-icon-120x120.png` Apple iPhone, Retina with iOS7
- `apple-touch-icon-144x144.png` Apple iPad, Retina with iOS6 or prior
- `apple-touch-icon-152x152.png` Apple iPad, Retina with iOS7
- `apple-touch-icon-180x180.png` Apple iPhone 6 Plus with iOS8
- `browserconfig.xml` IE11 icon configuration file
- `favicon_config.json` RealFaviconGenerator configuration file
- `favicon.ico` Favicon, IE and fallback for other browsers
- `favicon.png` Favicon generation source image
- `favicon-16x16.png` Favicon, default
- `favicon-32x32.png` Favicon, Safari on Mac OS
- `index.html` Main HTML file
- `logo.png` Logo
- `main.js` Main Javascript file
- `manifest.json` Manifest file
- `maskable_icon.png` Favicon, [maskable](https://web.dev/maskable-icon)
- `mstile-70x70.png` Favicon, Windows 8 / IE11
- `mstile-144x144.png` Favicon, Windows 8 / IE10
- `mstile-150x150.png` Favicon, Windows 8 / IE11
- `mstile-310x150.png` Favicon, Windows 8 / IE11
- `mstile-310x310.png` Favicon, Windows 8 / IE11
- `README.md` Readme file
- `robots.txt` Robots file
- `safari-pinned-tab.svg` Favicon, Safari pinned tab
- `share.jpg` Social media sharing
- `sitemap.xml` Sitemap file
- `sw.js` Service worker file
- `style.css` Main CSS file

### How do I use it?

1. Clone the repository from [GitHub](https://github.com/nikkifurls/simple-pwa).
2. Create all favicon images using [RealFaviconGenerator](https://realfavicongenerator.net) and replace existing images with generated images.

	If you're able to install the CLI version of **RealFaviconGenerator**, `favicon_config.json` contains all settings to generate these images using the following command from the project's root directory. The `real-favicon` tool generates images from `favicon.png`, so replace `favicon.png` prior to running this command. The resulting `favicon_data.json` and `site.webmanifest` can be discarded:
	
	`real-favicon generate favicon_config.json favicon_data.json .`

3. Create new 650x650 maskable icon using [Maskable.app](https://maskable.app) and replace `maskable_icon.png`.
4. Create new black vector icon using [`Manytools' colorize images tool`](http://manytools.org/image/colorize-filter) and replace [`safari-pinned-tab.svg`](https://github.com/nikkifurls/simple-pwa/blob/master/safari-pinned-tab.svg).
5. Create new 1200x630 share image and replace `share.jpg`.
6. Build your PWA by adding HTML, CSS, and Javascript.

### Can I contribute?

YES! Contributions are welcome!