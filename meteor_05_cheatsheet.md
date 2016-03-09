# METEOR #5: COMPLETE CHEATSHEET

## METEOR CORE
```
Anywhere: Meteor.isClient
Anywhere: Meteor.isServer
Anywhere: Meteor.startup(func)
Anywhere: Meteor.absoluteUrl([path], [options])
Anywhere: Meteor.settings
Anywhere: Meteor.release
```

## PUBLISH AND SUBSCRIBE
```
Server: Meteor.publish(name, func)
  this.userId
  this.added(collection, id, fields)
  this.changed(collection, id, fields)
  this.removed(collection, id)
  this.ready()
  this.onStop(func)
  this.error(error)
  this.stop()
  this.connection

Client: Meteor.subscribe(name [, arg1, arg2, …][, callbacks])
```

## METHODS
```
Anywhere: Meteor.methods(methods)
  this.userId
  this.setUserId  # only server side
  this.isSimulation
  this.unblock()
  this.connection  # only server side

Anywhere: new Meteor.Error(error, reason, details)
Anywhere: Meteor.call(name, param1, param2, … [, asyncCallback])
Anywhere: Meteor.apply(name, params[, options][, asyncCallback])  # options: wait, onResultReceived
```

## SERVER CONNECTIONS
```
Client: Meteor.status()
Client: Meteor.reconnect()
Client: Meteor.disconnect()
Server: Meteor.onConnection(callback)
Anywhere: DDP.connect(url)
```

## COLLECTIONS
```
Anywhere: new Meteor.Collection(name, [options])  # options: connection, idGeneration, transform
Anywhere: collection.find(selector, [options])  # options: sort, skip, limit, fields, reactive, transform
Anywhere: collection.findOne(selector, [options])  # options: sort, skip, fields, reactive, transform
Anywhere: collection.insert(doc, [callback])
Anywhere: collection.update(selector, modifier, [options], [callback])  # options: multi, upsert
Anywhere: collection.upsert(selector, modifier, [options], [callback])  # options: multi
Anywhere: collection.remove(selector, [callback])
Anywhere: collection.allow(options)  # options: insert, update, remove, fetch, transform
Anywhere: collection.deny(options)  # options: insert, update, remove, fetch, transform
Anywhere: cursor.forEach(callback, [thisArg])
Anywhere: cursor.map(callback, [thisArg])
Anywhere: cursor.fetch()
Anywhere: cursor.count()
Anywhere: cursor.rewind()
Anywhere: cursor.observe(callbacks)  # callbacks: added(At), changed(At), removed(At), movedTo
Anywhere: cursor.observeChanges(callbacks)  # callbacks: added(Before), changed, removed, movedBefore
Anywhere:  new Meteor.Collection.ObjectID(hexString)
```

## SESSION
```
Client: Session.set(key, value)
Client: Session.setDefault(key, value)
Client: Session.get(key)
Client: Session.equals(key, value)
```

## ACCOUNTS
```
Anywhere but publish functions: Meteor.user()
Anywhere but publish functions: Meteor.userId()
Anywhere: Meteor.users
Client: Meteor.loggingIn()
Client: Meteor.logout([callback])
Client: Meteor.logoutOtherClients([callback])
Client: Meteor.loginWithPassword(user, password, [callback])
Client: Meteor.loginWithExternalService([options], [callback])  # options: requestPermissions, requestOfflineToken, forceApprovalPrompt
Template: {{currentUser}}
Template: {{loggingIn}}
Anywhere: Accounts.config(options)  # options: sendVerificationEmail, forbidClientAccountCreation, restrictCreationByEmailDomain, loginExpirationInDays
Client: Accounts.ui.config(options)  # options: requestPermissions, requestOfflineToken, passwordSignupFields
Server: Accounts.validateNewUser(func)
Server: Accounts.onCreateUser(func)
Server: Accounts.validateLoginAttempt(func)
Server: Accounts.onLogin(func)
Server: Accounts.onLoginFailu(func)
```

## PASSWORDS
```
Anywhere: Accounts.createUser(options, [callback])  # options: username, email, password, profile
Client: Accounts.changePassword(oldPassword, newPassword, [callback])
Client: Accounts.forgotPassword(options, [callback])  # options: email
Client: Accounts.resetPassword(token, newPassword, [callback])
Server: Accounts.setPassword(userId, newPassword)
Client: Accounts.verifyEmail(token, [callback])
Server: Accounts.sendResetPasswordEmail(userId, [email])
Server: Accounts.sendEnrollmentEmail(userId, [email])
Server: Accounts.sendVerificationEmail(userId, [email])
Anywhere: Accounts.emailTemplates


TEMPLATES:

Client: Template.myTemplate([data])

Client: Template.myTemplate.events(eventMap)
# events: click, dblclick, focus, blur, change, mouseenter, mouseleave, mousedown, mouseup, keydown, keypress, keyup
# eventMap attributes: type, target, currentTarget, which
# eventMap methods: stopPropagation(), stopImmediatePropagation(), preventDefault(), isPropagationStopped(), isImmediatePropagationStopped(), isDefaultPrevented()

Client: Template.myTemplate.helpers(helpers)

Client: Template.myTemplate.rendered = function ( ) { ... }

Client: Template.myTemplate.created = function ( ) { ... }

Client: Template.myTemplate.destroyed = function ( ) { ... }

Client: Template instances.
  this.findAll(selector)
  this.find(selector)
  this.firstNode
  this.lastNode
  this.data

Client: UI.registerHelper(name, function)
Client: UI.body
Client: UI.render(Template.myTemplate)
Client: UI.renderWithData(Template.myTemplate, data)
Client: UI.insert(instantiatedComponent, parentNode[, nextNode])


MATCH:

Anywhere: check(value, pattern)
Anywhere: Match.test(value, pattern)
# patterns: Match.Any, String, Number, Boolean, undefined, null, Match.Integer, [pattern],
# {key1: pattern1, key2: pattern2, ...}, Match.ObjectIncluding({key1: pattern1, key2: pattern2, ...}),
# Object, Match.Optional(pattern), Match.OneOf(pattern1, pattern2, ...),
# Any constructor function (eg, Date), Match.Where(condition)
```

## TIMERS
```
Anywhere: Meteor.setTimeout(func, delay)
Anywhere: Meteor.setInterval(func, delay)
Anywhere: Meteor.clearTimeout(id)
Anywhere: Meteor.clearInterval(id)
```

## DEPS
```
Client: Deps.autorun(runFunc)
Client: Deps.flush()
Client: Deps.nonreactive(func)
Client: Deps.active
Client: Deps.currentComputation
Client: Deps.onInvalidate(callback)
Client: Deps.afterFlush(callback)

Deps.Computation  # Computation objects
  Client: computation.stop()
  Client: computation.invalidate()
  Client: computation.onInvalidate(callback)
  Client: computation.stopped
  Client: computation.invalidated
  Client: computation.firstRun

Deps.Dependency  # Dependency objects
  Client: dependency.changed()
  Client: dependency.depend([fromComputation])
  Client: dependency.hasDependents()
```

## EJSON
```
Anywhere: EJSON.parse(str)
Anywhere: EJSON.stringify(val, [options])  # options: indent, canonical
Anywhere: EJSON.fromJSONValue(val)
Anywhere: EJSON.toJSONValue(val)
Anywhere: EJSON.equals(a, b, [options])  # options: keyOrderSensitive
Anywhere: EJSON.clone(val)
Anywhere: EJSON.newBinary(size)
Anywhere: EJSON.isBinary(x)
Anywhere: EJSON.addType(name, factory)
  instance.clone()
  instance.equals(other)
  instance.typeName()
  instance.toJSONValue()
```

## HTTP
```
Anywhere: HTTP.call(method, url [, options] [, asyncCallback])  # options: content, data, query, params, auth, headers, timeout, followRedirects
Anywhere: HTTP.get(url, [options], [asyncCallback])
Anywhere: HTTP.post(url, [options], [asyncCallback])
Anywhere: HTTP.put(url, [options], [asyncCallback])
Anywhere: HTTP.del(url, [options], [asyncCallback])
```

## EMAIL
```
Anywhere: Email.send(options)  # options: from, to, cc, bcc, replyTo, subject, text, html, headers
```

## ASSETS
```
Server: Assets.getText(assetPath, [asyncCallback])
Server: Assets.getBinary(assetPath, [asyncCallback])
```

## COMMANDS
```
$ kill -9 `ps ax | grep node | grep meteor | awk '{print $1}'`  # to kill meteor

$ meteor help
$ meteor run [--port] [--production] [--raw-logs] [--settings] [--release] [--program]
$ meteor create [--release <release>] <name> [--example] [--list]
$ meteor update [--release <release>]
$ meteor add <package> [package] [package..]
$ meteor remove <package> [package] [package..]
$ meteor list [--using]
$ meteor bundle <output_file.tar.gz> [--debug]
$ meteor mongo [--url] [site]
$ meteor reset
$ meteor deploy <site> [--settings settings.json] [--debug] [--delete] [--star]
$ meteor logs <site>
$ meteor authorized <site> [--list] [--add <username>] [--remove <username>]
$ meteor claim <site>
$ meteor login [--email]
$ meteor logout
$ meteor whoami
$ meteor test-packages [--release <release>] [--port] [--deploy] [--production] [--settings] [package...]
```
