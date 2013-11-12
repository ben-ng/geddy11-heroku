Reproduction Steps
------------------

 1. `heroku create myapp`
 2. `git remote add heroku <heroku url>`
 3. `git push heroku master`
 4. `heroku addons:add heroku-postgresql:dev`
 5. `heroku pg:promote HEROKU_POSTGRES_<COLOR>_URL`
 6. `heroku run geddy jake db:init environment=production`

The Error
=========
ben@MILK ~/Documents/testapp (master)$ heroku run geddy jake db:init environment=production --trace
Running `geddy jake db:init environment=production --trace` attached to terminal... up, run.1656
Setting up DB support for postgres adapter, production environment...
Installing pg@2.5.x...
jake aborted.
Error: /bin/sh: npm: not found
    at api.fail (/app/node_modules/geddy/node_modules/jake/lib/api.js:326:18)
    at null.<anonymous> (/app/node_modules/geddy/node_modules/jake/lib/utils/index.js:134:9)
    at EventEmitter.emit (events.js:98:17)
    at ChildProcess.<anonymous> (/app/node_modules/geddy/node_modules/jake/lib/utils/index.js:210:20)
    at ChildProcess.EventEmitter.emit (events.js:98:17)
    at Process.ChildProcess._handle.onexit (child_process.js:789:12)

