# METEOR #22: THE BEST METEOR PACKAGES YOU MUST KNOW TO CODE FASTER THAN EVER

## CORE PACKAGES

You can take a look at all 120+ core packages available in the Meteor repository. Here are a few ones that may interest you.
* [appcache](https://atmospherejs.com/meteor/appcache) Stores the static parts of a Meteor application (the client side Javascript, HTML, CSS, and images) in the browser's application cache.
* [browser-policy](https://atmospherejs.com/meteor/browser-policy) Lets you set security-related policies that will be enforced by newer browsers. These policies help you prevent and mitigate common attacks like cross-site scripting and clickjacking.
* [check](https://atmospherejs.com/meteor/check) Lightweight package for argument checking and general pattern matching.
* [fastclick](https://atmospherejs.com/meteor/fastclick) A simple, easy-to-use library for eliminating the 300ms delay between a physical tap and the firing of a click event on mobile browsers.

## PACKAGES FOR TEMPLATES & STYLESHEETS

The Meteor community has built a lot of packages to make work easier with templates. Here are a few packages you should look at to increase your productivity.
* [raix:handlebar-helpers](https://atmospherejs.com/raix/handlebar-helpers) This package provides handy helpers and a simple way of using sessions and collections in the Meteor Spacebars template environment.
* [mquandalle:jade](https://atmospherejs.com/mquandalle/jade) Provides support for the Jade template engine as a Spacebars alternative and have some additional features like a else if component.
* [fourseven:scss](https://atmospherejs.com/fourseven/scss) This allows .scss and .sass files to work with Meteor (compile them through node-sass).
* [francocatena:compass](https://atmospherejs.com/francocatena/compass) Compass 0.13.alpha.4 packaged for Meteor. This package requires fourseven:scss to work.
* [dburles:spacebars-tohtml](https://atmospherejs.com/dburles/spacebars-tohtml) A simple helper function to assist with rendering spacebars to HTML. Works on both the server and the client. This is very useful for sending HTML emails.

## ROUTING PACKAGES & EXTENSIONS

One of the most key components of every project is the routing system. Iron router is considered as the official router for Meteor. It will help you build your first routes in a snap but you will sometimes want to implement additional features. Before doing so, take a look at the packages below.
* [iron:router](https://atmospherejs.com/iron/router) Routing specifically designed for Meteor. A router that works on the server and the browser, designed specifically for Meteor.
* [zimme:iron-router-auth](https://atmospherejs.com/zimme/iron-router-auth) Extends the iron-router package, allowing you to quickly lock routes down to authenticated users. It also provides the ability to auto-redirect back to the previous route on a successful login.
* [martino:iron-router-i18n](https://atmospherejs.com/martino/iron-router-i18n) Add i18n support for the popular Iron Router package.
* [zimme:iron-router-active](https://atmospherejs.com/zimme/iron-router-active) Active route/path template helpers for Iron Router.
* [multiply:iron-router-progress](https://atmospherejs.com/multiply/iron-router-progress) A little package that implements a simple progress bar (using nProgress), when loading different routes (check examples here).
* [manuelschoebel:wait-on-lib](https://atmospherejs.com/manuelschoebel/wait-on-lib) Use Iron-Router waitOn to load external javascript libraries.

## OPTIMIZE YOUR APPLICATION WITH THESE PACKAGES

Trying to scale and optimize your Meteor application? We recommend that you take a look at Meteor Bulletproof, a resource that will help you build faster apps. Meanwhile, here are a few packages we use in our projects to make them more efficient.
* [meteorhacks:fast-render](https://atmospherejs.com/meteorhacks/fast-render) Fast Render can improve the initial load time of your app, giving you 2-10 times faster initial page loads. It provides the same effect as Server Side Rendering (SSR), but still sends data over the wire to avoid breaking one of Meteor’s core principles.
* [meteorhacks:unblock](https://atmospherejs.com/meteorhacks/unblock) Provide this.unblock functionality to publications.
* [meteorhacks:subs-manager](https://atmospherejs.com/meteorhacks/subs-manager) Subscriptions Manager for Meteor. Subscriptions Manager caches your subscriptions and runs all the subscriptions that have been cached when a route is changed. This means that when switching between routes, the user will no longer have to wait. Also, Meteor won't need to re-send data that's already in the client.

## PACKAGES FOR COLLECTIONS & PUBLICATIONS/SUBSCRIPTIONS

Collections are Meteor's way of storing persistent data. They can be accessed from both the server and the client and update themselves automatically. You can find multiple packages below that provides additional features to manage and play with them.
* [aldeed:collection2](https://atmospherejs.com/aldeed/collection2) A Meteor package that extends Mongo.Collection to provide support for specifying a schema and then validating against that schema when inserting and updating.
* [dburles:collection-helpers](https://atmospherejs.com/dburles/collection-helpers) Collection helpers automatically sets up a transformation on your collections allowing for simple models, with an interface similar to template helpers.
* [mrt:collection-api](https://atmospherejs.com/mrt/collection-api) Allows you to easily perform CRUD operations on Meteor Collections over HTTP/HTTPS from outside of the Meteor client or server environment (or how to build an API in a few minutes).
* [percolate:paginated-subscription](https://atmospherejs.com/percolate/paginated-subscription) Adds pagination to Meteor's standard subscriptions.
* [cfs:standard-packages](https://atmospherejs.com/cfs/standard-packages) CollectionFS is a smart package for Meteor that provides a complete file management solution including uploading, downloading, storage, synchronization, manipulation, and copying. It supports several storage adapters for saving to the local filesystem, GridFS, or S3, and additional storage adapters can be created.
* [matb33:collection-hooks](https://atmospherejs.com/matb33/collection-hooks) Extends Mongo.Collection with before/after hooks for insert, update, remove, find, and findOne. Works across both client, server or a mix. Also works when a client initiates a collection method and the server runs the hook, all while respecting the collection validators (allow/deny).
* [reywood:publish-composite](https://atmospherejs.com/reywood/publish-composite) Meteor.publishComposite(...) provides a flexible way to publish a set of related documents from various collections using a reactive join. This makes it easy to publish a whole tree of documents at once. The published collections are reactive and will update when additions/changes/deletions are made.
* [dburles:factory](https://atmospherejs.com/dburles/factory) Meteor package for creating test data or generating fixtures.

## PACKAGES FOR YOUR FORMS

Forms are among the most used components of every website. The packages below will help you build and validate your forms faster.
* [aldeed:autoform](https://atmospherejs.com/aldeed/autoform) A smart package for Meteor that adds UI components and helpers to easily create basic forms with automatic insert and update events, and automatic reactive validation.
* [templates:forms](https://atmospherejs.com/templates/forms) Build production-ready, reactive forms in minutes. Even complex workflows can be achieved with just a few lines of code. A light-weight alternative to AutoForm based around reusable components.
* [copleykj:mesosphere](https://atmospherejs.com/copleykj/mesosphere) A dual client/server side form data validation, transformation, and aggregation package for Meteor.
* [matteodem:easy-search](https://atmospherejs.com/matteodem/easy-search) Easy-to-use search with Blaze Components (includes Elastic Search Support).
* [mizzao:autocomplete](https://atmospherejs.com/mizzao/autocomplete) Client/server autocompletion designed for Meteor's collections and reactivity. Looking for a more minimalistic autocompletion package? Check this one.

## PACKAGES FOR MOBILE DEVELOPMENT

August 2014, Meteor released a stunning feature: the ability to compile your application, thanks to Cordova, to iOS and Android devices. With isomorphic always in mind, a lot of useful packages for mobile development have emerged.
* [meteoric:ionic](https://atmospherejs.com/meteoric/ionic) This is an attempt at real Ionic and Meteor integration. This is not just Ionic's CSS framework wrapped in a Meteor package. It aims to be a complete port of Ionic’s Angular directives to Meteor Blaze templates. Also, check the complementary packages Ionic-SASS and Ionicons-SASS.

## TESTING PACKAGES

There was a time where testing a Meteor application was kind of hard. But now, with Velocity, you can integrate several testing frameworks like mocha, cucumber or jasmine and run reactive tests in a snap.
* [velocity:core](https://atmospherejs.com/velocity/core) A reactive test-runner for Meteor. Integrates easily with Jasmine, Cucumber, Mocha, CasperJs and Nightwatch (read more).
* [velocity:html-reporter](https://atmospherejs.com/velocity/html-reporter) HTML reporter for Meteor's Velocity testing framework.
* [sanjo:jasmine](https://atmospherejs.com/sanjo/jasmine) Easily write and run Jasmine tests for all your Meteor code.
* [mike:mocha](https://atmospherejs.com/mike/mocha) This meteor package allows you to easily and safely run mocha tests within Meteor.
* [xolvio:cucumber](https://atmospherejs.com/xolvio/cucumber) Gherkin sytax testing for Meteor using Cucumber.js, served as a Velocity test framework.
* [clinical:nightwatch](https://atmospherejs.com/clinical/nightwatch) Ultra-easy acceptance testing for your Meteor app with Selenium and Nightwatch.
* [nblazer:casperjs](https://atmospherejs.com/nblazer/casperjs) CasperJS end to end test integration for meteor using velocity.
* [anti:gagarin](https://atmospherejs.com/anti/gagarin) Gagarin is a tool you can use in your tests to run Meteor apps in a sandboxed environment. It's useful when you need more refined control over the meteor processes and test fancy things, e.g. the behavior of your app on server restarts or when you have multiple app instances writing to the same database.

## PACKAGES FOR SEO/SMO


## SEO and SMO are important marketing aspects. You need to configure your application to make them return the things you want search engines and social medias to see/display.
* [manuelschoebel:ms-seo](https://atmospherejs.com/manuelschoebel/ms-seo) A SEO helper package for Meteor (read more in this article).
* [gadicohen:sitemaps](https://atmospherejs.com/gadicohen/sitemaps) Create valid and dynamic sitemaps using your own functions.

## ACCOUNTS & ROLE PACKAGES.

Building an account system with Meteor is straightforward. You probably know the core package accounts-password but here are a few extensions that will provide to your app additional features.
* [alanning:roles](https://atmospherejs.com/alanning/roles) An authorization package for Meteor - compatible with built-in accounts package. Lets you attach permissions to a user which you can then check against later when deciding whether to grant access to Meteor methods or publish data.
* [artwells:accounts-guest](https://atmospherejs.com/artwells/accounts-guest) Automatically add visitor as anonymous guest with userId. Each non-logged in visitor gets a userId, accessible via Accounts and Meteor.userId().
* [mizzao:user-status](https://atmospherejs.com/mizzao/user-status) Keeps track of user connection data, such as IP addresses, user agents, and client-side activity, and tracks this information in Meteor.users as well as some other objects. This allows you to easily see users that are online, for applications such as rendering the users box below showing online users in green and idle users in orange.
* [useraccounts:core](https://atmospherejs.com/useraccounts/core) User Accounts is a suite of packages for the Meteor.js platform. It provides highly customizable user accounts UI templates for many different front-end frameworks. At the moment it includes forms for sign in, sign up, forgot password, reset password, change password, enroll account, and link or remove of many 3rd party services. (also, check his themes)
* [joshowens:accounts-entry](https://atmospherejs.com/joshowens/accounts-entry) accounts-entry is a meteorite package that relies on Iron Router and provides an alternative interface to accounts-ui, with whole pages for sign up and sign in.

## DEPLOYMENT AND MONITORING PACKAGES

We wrote last year a tutorial on how to deploy a Meteor application on Ubuntu and how to use MUP to easily configure your server. You will find below additional packages to test and monitor your app so as to be sure that everything is running well.
Meteor Up: Meteor Up (MUP for short) is a command line tool that allows you to initialize/configure your Debian/Ubuntu and Open Solaris server and to deploy your Meteor application with a single line. It's not a meteor package and it can be installed with npm install -g mup.
Meteor Load Test: A load testing tool for Meteor applications that utilizes the Grinder to manage agents.
* [meteorhacks:kadira](https://atmospherejs.com/meteorhacks/kadira) Integrate your Meteor application with Kadira for performance monitoring.
* [percolate:server-info](https://atmospherejs.com/percolate/server-info) A Meteor package for querying an application for diagnostics information. sets up a route (By default at /info) that returns a json object containing useful debugging data.
* [mrt:server-stats](https://atmospherejs.com/mrt/server-stats) A Meteor package to grab system stats (cpu, memory, load, versions, hostname) from the server.

## PACKAGES FOR THIRD-PARTIES PLATFORMS

If you are trying to integrate a third-party service with your application, chances are that someone has already built a package for that. That's why it's important that you check Atmosphere so as to avoid reinventing the wheel.
* [datariot:ganalytics](https://atmospherejs.com/datariot/ganalytics) Log page views and events to Google Analytics.
* [obvio171:disqus](https://atmospherejs.com/obvio171/disqus) Disqus package for Meteor. Add {{>disqus}} to template. Be happy.
* [limemakers:paypal](https://atmospherejs.com/limemakers/paypal) Meteor Package for easy Paypal payment processing.
* [mrgalaxy:stripe](https://atmospherejs.com/mrgalaxy/stripe) Stripe.js and Node-Stripe brought to Meteor.
* [cunneen:mailgun](https://atmospherejs.com/cunneen/mailgun) A meteorite package for sending emails easily using Mailgun.

## ADMINISTRATION PACKAGES

A few awesome packages we use to generate an administration quickly.
* [houston:admin](https://atmospherejs.com/houston/admin) Houston is a zero-config Meteor Admin, modeled after Django Admin, intended as a simple way for developers to give end-users (or themselves) an easy way to view and manipulate their app's data.
* [yogiben:admin](https://atmospherejs.com/yogiben/admin) A complete admin dashboard solution for meteor built off the iron-router, roles and autoform packages and frontend from the open source admin dashboard template, Admin LTE.
* [tail:core](https://atmospherejs.com/tail/core) A super cool analytics package for Meteor.

## SECURITY PACKAGES

If you read Sacha Greif's article about Security, here are a some packages that will help you to enhance your app and go further.
* [matteodem:easy-security](https://atmospherejs.com/matteodem/easy-security) Protection against harmful attacks by rate limiting remote method calls.
* [ongoworks:security](https://atmospherejs.com/ongoworks/security) A Meteor package that provides a simple, logical, plain language API for defining write security on your MongoDB collections. Wraps the core allow/deny security.

## DEBUGGING PACKAGES

The following packages will help you debug your Meteor application and make your life easier.
* [msavin:mongoinspector](https://atmospherejs.com/msavin/mongoinspector) Meteor package for visualizing your collections in the browser.

## METEOR BOILERPLATES

When starting a new project, you need to think about the way you will organize your application. If you are an experienced Meteor developer, you probably have your own ready-to-start Meteor repository or are using one of the boilerplates below.
Meteor Boilerplate (Differential): A starting point for Meteor applications. Includes iron-router, Bootstrap 3, Font Awesome, LESS and more.
Another Meteor Boilerplate (Matteo Dem): This boilerplate is here to give you a starting point for your meteor projects, with a console tool to ease up some tasks. Essential atmosphere packages are included to give you features like routing and collection schemas out-of-the-box.
Meteoric Boilerplate: A Boilerplate for Meteor using Meteor Ionic as base. If you would like to build mobile application with Meteor, Cordova & Ionic, that's a good way to start a project in a snap and save time.

## MISCELLANEOUS PACKAGES

To conclude this long list, here are some packages you should look at.
* [tap:i18n](https://atmospherejs.com/tap/i18n) tap-i18n is a Meteor package that provides a comprehensive i18n solution for Meteor apps and packages, with the goal of standardizing the way package developers internationalize their packages (used by Telescope and more).
* [ryw:blog](https://atmospherejs.com/ryw/blog) Gives you a basic, out-of-the-box blog at /blog.
* [percolate:synced-cron](https://atmospherejs.com/percolate/synced-cron) A simple cron system for Meteor. It supports syncronizing jobs between multiple processes. In other words, if you add a job that runs every hour and your deployment consists of multiple app servers, only one of the app servers will execute the job each time (whichever tries first).
* [sacha:spin](https://atmospherejs.com/sacha/spin) A Meteor package wrapper for Spin.js via Npm.depends(). Allows you to add and configure spinner in your template with {{> spinner}}.
* [template:tabs](https://atmospherejs.com/template/tabs) Reactive tabbed interfaces compatible with routing.
* [dandv:http-more](https://atmospherejs.com/dandv/http-more) Make HTTP calls to remote servers, passing any extra options to the underlying backend.
* [anti:fake](https://atmospherejs.com/anti/fake) Random text and joyful names generator.
