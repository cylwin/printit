fs = require 'fs'
{exec} = require 'child_process'

task 'tests', 'run tests', ->
  console.log 'Run tests with...'
  command = 'node tests.js'
  exec command, (err, stdout, stderr) ->
    console.log stdout
    if err
      console.log "Running tests caught exception: \n" + err
      process.exit 1
    else
      process.exit 0

task 'build', '', ->
  console.log 'Compile main file...'
  command = 'coffee -cb main.coffee'
  exec command, (err, stdout, stderr) ->
    if err
      console.log 'Running coffee-script compiler caught exception: \n' + err
    else
      console.log 'Compilation succeeded.'

    console.log stdout
