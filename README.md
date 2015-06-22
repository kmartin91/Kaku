# Kaku
The next generation music client

# Build Status

[![Build Status](https://travis-ci.org/EragonJ/Kaku.svg?branch=master)](https://travis-ci.org/EragonJ/kaku)

# Let's talk !

We have a gitter chatting room and please feel free to join us and talk there :)

[![Join the chat at https://gitter.im/EragonJ/Kaku](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/EragonJ/Kaku?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Latest Screenshot

![Latest Screenshot](http://i.imgur.com/aPzU4ER.jpg)

# Setup environment

Because we use bower & npm to maintain our third party libraries, you have to make sure before doing anything, these needed stuffs are all installed already.

1. `bower install`
2. `npm install`
3. `npm install electron-prebuilt -g` - Install **electron** command

## Prerequistiques

**This is IMPORTANT, please read this**

In order to successfully make Kaku functional, you have to prepare all needed configs first. (Take Youtube API for example, in latest 3.0 API, you need your own API KEY to execute their API)  No matter you are in production or development environment, this is important and please make sure you already did this before building. [Follow the instruction to here to register your API key.](https://developers.google.com/youtube/v3/getting-started)

Please take a look at `config/`, you will notice there are some files named like `*.sample.json`, remember to update them with correct config and rename them to `*.production.json`, then everything should work as perfect !

## Make production build

We need to make sure all codes would be moved to the right place and generated the final entry point to reduce requests to load data, so you have to build first.

```bash
gulp build # without plaform argument, we will build Kaku based on your platform
```

or you can be more precise about which platform you are going to build like this :

```bash
gulp build --platform=mac # =linux, =windows, =win, =mac, =darwin are all valid
```

After that, you will get a solid application to run !

## How to develop

In order to speed up development pace, we won't do too much building tasks in this phase. All we do is to watch all folders and see what files are changed and trigger browser to reload.

But no matter how, please remember to run following command first to make sure we create all needed temporary files first.

```bash
gulp
```

After that, you need to open a terminal session and watch changes in files :

```bash
gulp watch
```

then run Kaku :

```bash
electron .
```

# TODO / Issues

Moved all todos and issues to https://github.com/EragonJ/Kaku/issues, so if your are interested with them, please go check it there !

# What tech we use ?

## Still in use

+ [Gulp](http://gulpjs.com/) - To build up our environment
+ [Electron](http://electron.atom.io) - Let us use web technology to build native app
+ [Bower](http://bower.io/) - To help us manage frontend resources
+ [Require.js](http://requirejs.org/) - To help me make codes more structure
+ [Bootstrap](http://getbootstrap.com/) - To boostrap the whole project including grid system ... etc
+ [FontAwesome](http://fortawesome.github.io/Font-Awesome/) - To make Kaku look nice
+ [jQuery](https://jquery.com/) - Bootstrap is based on jQuery
+ [React.js](http://reactjs.org/) - To help us break UI into small components
+ [Video.js](http://www.videojs.com/) - To help us control the player
+ [Babel](https://babeljs.io/) - To do some pre-transfrom process
+ [NPM](https://www.npmjs.org/) - To help us manage node modules resources
+ [Less](http://lesscss.org) - Make life better when writting CSS
+ [Pouchdb](http://pouchdb.com) - Our database to store trakcs
+ [Bootbox](http://bootboxjs.com) - To help us show dialogs based on Bootstrap
+ [Animate.css](https://daneden.github.io/animate.css/) - Animation matters
+ [Youtube-dl](https://github.com/rg3/youtube-dl/) - Download youtube tracks on the fly
+ ... still increasing :)

## Deprecated
+ [Compass / SASS](http://compass-style.org/) - To help us write CSS easily
+ [NW.js](http://nwjs.io/) - (Moved to Electron)
+ ... thanks for these old friends :)
