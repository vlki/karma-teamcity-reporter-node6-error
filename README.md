# Karma + karma teamcity reporter error

Minimal example reproducing following error when using karma + karma teamcity reporter together.

```
Missing error handler on `socket`.
Error: EAGAIN: resource temporarily unavailable, write
```

[Full error output here](error_output.txt)


# Reproduce

```
git clone https://github.com/vlki/karma-teamcity-reporter-node6-error.git
cd karma-teamcity-reporter-node6-error
npm install
node_modules/.bin/karma start --reporters teamcity
```

* Then re-save the test.js file few times to trigger tests re-running
* Usually around 5th re-run the error occurs

# Notes

Error started showing after update to node 6.1.0. Error does not show up on node 5.11.0, but does show up on 6.0.0 and 6.1.0.

# Environment

Mac OS X 10.11.4
