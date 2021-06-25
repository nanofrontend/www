# www.nanofrontends.com

## Abstract
Micro-frontends are a strategy for splitting user interfaces up into separately deployable units. 
This gives teams great latitude to choose their own technologies and think in terms of self-contained programs. 

+ per page frontend approach has disadvantages: pages cannot be shared by teams
+ sub-frontends are hard to modalularize and the user must download and execute duplicate JavaScript. 

Nano-frontends are an alternative that give teams similar freedoms but provide opt-in optimisations to improve user experience.


Write your frontends as libraries that take:
+ a DOM element to render in 
+ a set of common dependencies to call (e.g. React)
+ allow a scaffold app to render the entire thing and inject the dependencies. 
+ Libraries can be published by writing artefacts to S3 and then monitoring for changes using SNS/SQS.

## What does a 'dependency injected' frontend look like?

First we need to specify a set of dependencies


## The scaffold app

This is a simple Node/Express/React app that routes from URLs to components that each instantiate nano-frontends. Nano-frontends are loaded via dynamic `import`. For instance, on the homepage:

The scaffolding app then 'makes the decision' as to where nano-frontends go in terms of both URL and page location.
This makes it easy for teams to discuss changes or contention, and also see the state of the frontend.

## Publishing workflow

If we want teams to be independent, they need to be able to release just by updating their own repositories.

Now we commit the code and run a build with e.g. CircleCI. 
There's a testbed that can run a full browser test of our component just by injecting the necessary dependencies - including mocked dependencies. This means we can do a11y and full 'clickability' testing without having to prepare API state.

Once completed, the build process compiles the code into a bundle. Note that the dependency file only exports types, so React / ReactDOM / jss aren't included in the final bundle.

Push this to S3 and we can trigger an SNS notification (e.g. `s3:ObjectCreated:Put`). This will update the 'scaffold app' that actually renders the nano-frontend.
