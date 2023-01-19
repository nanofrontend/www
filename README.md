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



# [www.microfrontend.org](https://www.microfrontend.org/)





## Current Technologies at 2021

+ Single Page Application (SPA)
+ Progressive Web App (PWA)
+ Application as a Stream (AaaS)
    + native javascript  
    + json based communication
    
    

+ [nanofrontends](http://www.nanofrontends.com/)


## The Stack

How your stack looks will depend on how you want to render your application. Here is a comprehensive discussion about that, but in a nutshell:

### Client-side rendering(CSR); SPA; JSON APIs 
This is perhaps the most popular approach. It's great for building interactive web applications. But be aware of its downsides and steps to mitigate them. This is the approach I took, so we will talk about it in a lot of detail.

### Hybrid CSR; Both client-side and server-side rendering(SSR) 
With this approach, you still build your SPA. But when a user requests your app, for example, the homepage, you render the homepage's component into its static HTML in your server and serve it to the user. Then at the user's browser, hydration will happen so the whole thing becomes the intended SPA.

### Downsides
But there are downsides too. 
Apart from the extra maintenance costs, we will have to download the same payload twice—First, the HTML, and second, its Javascript counterpart for the 'hydration' which will exert significant work on the browser's main thread. 
This prolongs the 'First time to interactive', and hence diminishes the benefits gained from a faster 'First meaningful paint'.

### Examples
The technologies that are adopted for this approach are NextJs, NuxtJs, and GatsbyJs.



### Turbolinks
https://github.com/turbolinks/turbolinks
Turbolinks® makes navigating your web application faster. Get the performance benefits of a single-page application without the added complexity of a client-side JavaScript framework. Use HTML to render your views on the server side and link to pages as usual. When you follow a link, Turbolinks automatically fetches the page, swaps in its <body>, and merges its <head>, all without incurring the cost of a full page load.




### Phoenix LiveView
https://github.com/phoenixframework/phoenix_live_view

Phoenix LiveView enables rich, real-time user experiences with server-rendered HTML.

After you [install Elixir](https://elixir-lang.org/install.html)
in your machine, you can create your first LiveView app in two
steps:

    $ mix archive.install hex phx_new
    $ mix phx.new demo --live

#### Features

* Use a declarative model to render HTML on the server over WebSockets with optional LongPolling fallback

* Smart templating and change tracking - after connected, LiveView sends only what changed to the client, skipping the template markup and reducing the payload

* Live form validation with file upload support

* A rich integration API with the client with `phx-click`, `phx-focus`, `phx-blur`, `phx-submit`, etc. `phx-hook` is included for the cases where you have to write JavaScript

* Code reuse via components, which break templates, state, and event handling into reusable bits, which is essential in large applications

* Live navigation to enrich links and redirects to only load the minimum amount of content as users navigate between pages

* A latency simulator so you can emulate how slow clients will interact with your application

* Testing tools that allow you to write a confident test suite without the complexity of running a whole browser alongside your tests


# AaaS - Application as a Stream

AaaS is supported by WebStream.

+ WebStream is an library part of wapka's ecosystem for web-development

## How WebStream work's?

Load any media on website without reload page, now stream each website without reload.
Over modularity each website can talk to another without barrier...

    
### Supported media

Ładowanie mediów tekstowych, kodu aplikacji, filmów, głosu, itp.

+ html
+ txt
+ markdown
+ mp3
+ wav
+ js
+ php
+ python


# why?
    
Because we can improve our stack without clouds

+ [more about limitations of CLOUDS](CLOUDS.md)

    
## The Stack

How your stack looks will depend on how you want to render your application. Here is a comprehensive discussion about that, but in a nutshell:

    Client-side rendering(CSR); SPA; JSON APIs —
    This is perhaps the most popular approach. It's great for building interactive web applications. But be aware of its downsides and steps to mitigate them. This is the approach I took, so we will talk about it in a lot of detail.

    Hybrid CSR; Both client-side and server-side rendering(SSR) —
    With this approach, you still build your SPA. But when a user requests your app, for example, the homepage, you render the homepage's component into its static HTML in your server and serve it to the user. Then at the user's browser, hydration will happen so the whole thing becomes the intended SPA.

The main benefits of this approach are that you get good SEO and users can see your stuff sooner (faster 'First Meaningful Paint').

But there are downsides too. Apart from the extra maintenance costs, we will have to download the same payload twice—First, the HTML, and second, its Javascript counterpart for the 'hydration' which will exert significant work on the browser's main thread. This prolongs the 'First time to interactive', and hence diminishes the benefits gained from a faster 'First meaningful paint'.

The technologies that are adopted for this approach are NextJs, NuxtJs, and GatsbyJs.


---
### Single SPA


Najprostszy sposób, aby zacząć: możemy użyć okna postMessage() do komunikacji między aplikacjami.
   
Jest to framework do komponowania ze sobą aplikacji frontendowych. Jeśli chcesz rozpocząć prawdziwy projekt, wybierz ten poniżej:

Mikrofrontend pozwala nam łączyć kilka aplikacji napisanych nawet w różnych frameworkach
Frameworki są tylko narzędziem, najważniejsza natomiast dla nas jest możliwość podzielenia aplikacji funkcjonalnie i przydzielenia tych części zespołom.

https://single-spa.js.org
    
    

### Frint

To kolejny framework do komponowania ze sobą aplikacji frontendowych. Bardziej elastyczny niż Single SPA, ale nowszy i mniej popularny:

https://frint.js.org

    
    
### WebComponents - Komponenty webowe

Nie jest to framework, ale funkcja przeglądarki i być może przyszłość Internetu. Oto artykuł na ten temat:

https://www.webcomponents.org/introduction
    
    

### Taylor

Framework ten wykorzystuje inne podejście, tworząc stronę routingu na backendzie za pomocą node.js. Jeśli pomysł Ci się podoba, warto zobaczyć:

https://github.com/zalando/tailor
    



### Turbolinks
    
https://github.com/turbolinks/turbolinks
Turbolinks® makes navigating your web application faster. Get the performance benefits of a single-page application without the added complexity of a client-side JavaScript framework. Use HTML to render your views on the server side and link to pages as usual. When you follow a link, Turbolinks automatically fetches the page, swaps in its <body>, and merges its <head>, all without incurring the cost of a full page load.




### Phoenix LiveView

https://github.com/phoenixframework/phoenix_live_view

Phoenix LiveView enables rich, real-time user experiences with server-rendered HTML.

After you [install Elixir](https://elixir-lang.org/install.html)
in your machine, you can create your first LiveView app in two
steps:

    $ mix archive.install hex phx_new
    $ mix phx.new demo --live
    

    
## More
+ [How to create a better front-end developer experience](https://developers.redhat.com/articles/2021/06/01/how-create-better-front-end-developer-experience)    

    
    
    
---
+ [edit](https://github.com/nanofrontends/www/edit/main/README.md)
+ [git](https://github.com/nanofrontends/www)
```
https://github.com/nanofrontends/www.git
```

