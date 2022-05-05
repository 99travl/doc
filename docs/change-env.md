# Configure different environments

When working with multiple environments
(like dev, integration, prod,...) we 
need to make sure that our code is going
to react to the different environments.
So we use special features of the 
framework we're using, telling him to
pick certain config files based on the
environment.

Let's say we've two environments: 
- _dev_ for local dev 
- _prod_ for production

We will create two config files for 
each or them, with a same radical but 
different endings:
- `application.yml` is the common one,
- `application-dev.yml` is for the 
`dev` env,
- `application-prod.yml` is for the
`prod` env,

Then we'll adjust the data there and
tell the app who to pick when in which
environment.

With IntelliJ or VSCode, we could also
define variable for these files.

It's common usage to leave it as simple
as possible, for it to be ran simply by
new members.