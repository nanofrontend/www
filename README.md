# [www.nanofrontend.com](http://www.nanofrontend.com)

## menu

+ [Human-Centric Solutions - WETWARE.DEV: DigitalTwin](http://www.wetware.dev)
+ [Architecture-Centric Solutions - MODWARE.ORG: Modular Foundation for Design Pattern](https://www.modware.org)
+ [Agent-Centric Solutions - TeleOperator.org: agent services Gaiann.com, Edi.Chat, do.camera, sub.actor](http://www.TeleOperator.org)
+ [Interface-Centric Solutions - nanoFrontend.com: Modular/Atomized Streamed Interface for media audio, video, textware.org, WebStream.dev](http://www.nanofrontend.com)
+ [Service-Centric Solutions - SaaSisKing.com: Software Requirements](http://www.SaaSisKing.com)
+ [Software-Centric Solutions - text.to.software - Modular Network of Code by Dialogware](http://text.to.software)
+ [Infrastructure-Centric Solutions - ModDevOps.com: Operations, Domains, DNS, CDN, Dynapsys](http://www.ModDevOps.com)
+ [Security-Centric Solutions - CyberPolygon.org: Incidents Detection, Prevention, Monitoring](http://www.cyberpolygon.org)


+ [SDLC: softreck.dev](http://leadership.run/SDLC)


## Two strategies from frontside perspecitve

### Decompozition
- Microfrontend: Breaks down monolithic frontend into smaller, independent applications.
- Nanofrontend: Takes granularity to the extreme, treating individual components as separate entities.

### Decoupling
- Headless: Separates frontend from backend, allowing flexibility and content management.
- Frontendless: focuses on minimizing the traditional frontend layer, while Headless emphasizes decoupling frontend and backend.


## Headless:
In the context of web development, a headless architecture refers to separating the frontend (presentation layer) from the backend (content management and business logic).

### Characteristics:
- The frontend communicates with the backend via APIs.
- Allows flexibility in choosing frontend technologies (e.g., React, Angular, Vue.js).
- Ideal for building decoupled systems, such as single-page applications (SPAs) or mobile apps.
- Enables content management through a headless CMS.

### Example:
Using a headless CMS like Contentful or Strapi with a React frontend.



## MicroFrontend
Microfrontends apply the concept of microservices to the browser side. They break down a monolithic frontend application into smaller, independent front-end applications.

### Characteristics:
- Each frontend application can be standalone, independently developed, and deployed.
- Components can be shared across microfrontends.
- Can be managed via NPM, Git, or other tools.

### Implementation Approaches:
- Route Dispatch: Dynamically load microfrontends based on routes.
- iFrame Containers: Embed microfrontends within iframes.
- Web Components: Use native web components for integration.

### Example:
Building a complex application by combining multiple smaller front-end applications.



## NanoFrontend:
A more granular approach than microfrontends, where individual components are treated as nanofrontends.

### Characteristics:

- Extremely fine-grained separation of concerns.
- Each component is independently deployable.
- Often used in scenarios where extreme isolation is required.


## Example:

Breaking down a large application into tiny, reusable components (e.g., buttons, forms).



## FrontendLess

The term "frontendless" refers to an architectural approach where the traditional frontend layer of a web application is either minimized or eliminated altogether:
- Frontendless implies that there is little to no dedicated frontend code responsible for rendering the user interface (UI) in the traditional sense.
- Instead of relying on a monolithic frontend, frontendless architectures distribute UI-related responsibilities across other layers or services.

Frontendless architectures aim to streamline UI development by distributing responsibilities across various layers, services, or components. Whether it's SSR, microfrontends, or web components, the goal is to achieve flexibility, maintainability, and scalability while minimizing the traditional frontend footprint. 🚀


### Server-Side Rendering (SSR):
- In SSR, the server generates HTML content dynamically and sends it to the client.
- The client receives pre-rendered HTML, which reduces the need for extensive client-side JavaScript.
- While not entirely frontendless, SSR minimizes the client-side codebase.
  
### API-First or Headless Architectures:
- Similar to headless architectures, where the frontend is decoupled from the backend.
- APIs serve as the primary means of communication between the client and the server.
- The client (frontend) consumes data via APIs and handles UI rendering.
  
### Client-Side Rendering (CSR) with Microfrontends:
- Divide the frontend into smaller, independently deployable microfrontends.
- Each microfrontend handles a specific part of the UI.
- The overall application remains lightweight and modular.
  
### Web Components:
- Use native web components (custom elements) to create reusable UI elements.
- These components can be shared across different projects.
- Encourages a frontendless mindset by focusing on component-based development.

### Benefits:
- Reduced Complexity: By minimizing frontend code, maintenance becomes simpler.
- Scalability: Microfrontends and web components allow for scalable UI development.
- Flexibility: Choose technologies and frameworks independently for different parts of the UI.

### Challenges:
- Initial Learning Curve: Adapting to a frontendless approach may require a shift in mindset.
- Integration: Ensuring seamless communication between microfrontends or components.
- Tooling and Infrastructure: Setting up build pipelines and deployment processes.




## Modular/Atomized Streamed Interface

### Modular Interfacing
- Definition: Modular interfacing refers to connecting different components or systems in a modular fashion, allowing them to communicate seamlessly.
- Example: In the context of music production and synthesis, modular interfacing involves connecting a modular synthesizer (such as a Eurorack system) to a computer-based digital audio workstation (DAW).
- Challenges: One challenge is bridging the gap between Control Voltage (CV) signals (used in modular synths) and audio signals (used in DAWs).
- DC-Coupled Audio Interfaces: To facilitate CV communication, you'll need a DC-coupled audio interface. These interfaces allow both audio and CV signals to flow between your modular system and your DAW.
- Expert Sleepers ES-8 and ES-9: The Expert Sleepers ES-8 and ES-9 are popular DC-coupled audio interface modules that connect via USB and serve as the audio engine for your DAW. They provide inputs and outputs for CV signals, making them ideal for integrating modular and digital environments.
  
### Types of Modular Interface Design
- Bus Modular Architecture:
    - In this design, elements connect to a common bus or base element through the same type of interface.
    - Example: Using a 4-Port USB hub as the base element to connect various USB peripherals.
- GPIO Ports on Raspberry Pi Zero W:
    - Another example of modular interfacing is connecting different sensors to the GPIO (General Purpose Input/Output) ports on a Raspberry Pi Zero W.
    - Each sensor communicates with the base element (Raspberry Pi) via a specific interface.
      
### Optimizing Digital Streaming
- While not directly related to modular synthesis, optimizing digital streaming interfaces is crucial for high-quality audio.
- Purpose-designed components, such as optical fiber interfaces, enhance functionality, flexibility, and audio quality when streaming digital content from computers to DACs or integrated amps.
  
In summary, modular interfacing involves creating flexible connections between components, whether in music synthesis, general electronics, or digital streaming. Whether you're patching CV signals, connecting sensors, or optimizing audio streaming, the key is adaptability and efficient communication. 🎛️🔌🎶





## Frontendless vs Headless architectures:

### Frontendless:
A Frontendless architecture minimizes or eliminates the traditional frontend layer of a web application.
- Characteristics:
    - Reduced Frontend Footprint: In a Frontendless approach, the UI rendering responsibilities are distributed across other layers or services.
    - Examples:
        - Server-Side Rendering (SSR): Pre-rendering HTML on the server side and sending it to the client.
        - Web Components: Creating reusable UI elements using native web components.
        - Microfrontends: Breaking down the frontend into independently deployable microfrontends.
- Benefits:
    - Simplicity: Maintenance becomes simpler with fewer frontend components.
    - Scalability: Modular approaches allow for scalable UI development.
    - Flexibility: Choose technologies independently for different parts of the UI.
      
### Headless:
A Headless architecture decouples the frontend (presentation layer) from the backend (content management and business logic).
- Characteristics:
    - API-First Approach: Communication between frontend and backend occurs via APIs.
    - Advantages:
        - Scalability: Ideal for building decoupled systems (e.g., single-page applications).
        - Content Management: Enables using a headless CMS.
        - Resource Efficiency: Doesn't require resources for rendering graphical elements.
- Examples of Headless CMS:
    - Contentful, Strapi, or Prismic.
    - Frameworks: React, Angular, or Vue.js.
      
### Comparison:
Frontendless focuses on minimizing the traditional frontend layer, while Headless emphasizes decoupling frontend and backend.
- Use Cases:
    - Choose Frontendless for extreme simplicity and modular UI development.
    - Opt for Headless when scalability, content management, and resource efficiency are critical.
      




## Microfrontends vs NanoFrontends



### Microfrontends

Microfrontends to architektura projektowania stron internetowych i aplikacji webowych, która polega na podziale frontendu na mniejsze, niezależnie rozwijane i wdrażane fragmenty. Każdy microfrontend może być odpowiedzialny za określoną funkcjonalność lub sekcję aplikacji i jest opracowywany przez odrębny zespół. Ta koncepcja jest rozszerzeniem idei mikrousług na warstwę frontową, umożliwiając większą skalowalność, prostotę zarządzania i możliwość wykorzystania różnych technologii oraz frameworków przez poszczególne zespoły. 

### Nanofrontends

Nanofrontends służy dalszego podziału koncepcji microfrontends na jeszcze mniejsze, bardziej zatomizowane jednostki.
Nanofrontends skupia się na bardzo szczegółowych, wyspecjalizowanych/atomowych aspektach aplikacji, potencjalnie umożliwiając jeszcze większą niezależność w rozwoju.
Na przykład, oddzielne jednostki zarządzające bardzo małymi, ponownie wykorzystywalnymi komponentami interfejsu użytkownika, takimi jak przyciski, ikony, pola tekstowe itp. 

Rodzi to wyzwania organizacyjne i techniczne, zwiększając złożoność zarządzania zależnościami, komunikacją między komponentami i spójnością doświadczenia użytkownika.
Korzyści z jeszcze bardziej zatomizowanej architektury niż microfrontends są dopiero dostzregalne w kontekście reużywalnośći, reusabuility w architektyurzy hipermodularnej.







# [microfrontend](https://www.microfrontend.org/)





### Abstract

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


![1/cover.png](https://logo.nanoservices.pl/1/cover.png)

[About nanoservices](https://www.nanoservices.pl/)

## Hashtags:
+ SOA Service Oriented Architecture
+ Atomisation
+ Modularity
+ nanofrontends


# Nanoservices

## What are nanoservices?

While they are smaller, flexible, more isolated, and functionally focused, there are still unknowns on:
+ Compatibility with emerging tech
+ Exponential scaling
+ Nanoservices are designed to perform a single function, whose output is exposed through a specific API endpoint (command).
+ Nanoservices are considered smaller siblings of microservices. 
+ Nanoservices are fully discoverable among each other.
Each one can link with other services to perform additional actions and extend functionality.


## By design, nanoservices are:
+ Self-contained
+ Reusable
+ Less complex than microservices
+ Supported by distinct function files for each


## Efficiency of nanoservices
Nanoservices are considered more efficient than microservices, particularly due to:
+ Ease of initial setup
+ Reduced latency among services

Each nanoservices function code can be executed on-demand without the use of dedicated containers or servers to host every individual service.


## Architecture
https://vmblog.com/archive/2020/02/25/an-introduction-to-serverless-architecture.aspx

## The way of development

Monolith - Microservices - Nanoservices

More Reusability from code side and business logic
With microservices are coming microfrontends
With nanoservices are comming nanofrontends


## Example Code

	test
	
The illustration below highlights an interesting use-case of how the BBC website uses 1,000s of nanoservices to render dynamic web pages.
Each service functions to feed into a specific component of the webpage, such as:
+ Generating a headline
+ Sourcing weather data
+ Updating a match score	


## The Difference Between APIs and Microservices

https://www.scalyr.com/blog/api-vs-microservices/

https://wisdomplexus.com/blogs/nanoservices-vs-microservices/

Here are the main differences between APIs and microservices:

+ An API is a contract that provides guidance for a consumer to use the underlying service.
+ A microservice is an architectural design that separates portions of a (usually monolithic) application into small, self-containing services.
    

# Microservices and Nanoservices

As a result, there are conflicting schools of thought around how and when to use microservices.
First, the mere nature of nanoservices poses the question as to whether they are secured from attack vectors when used extensively in an application.
Some also consider nanoservices to be an anti-pattern due to their fragmented functionality. This is known to cause maintenance overhead to exceed the value of the framework’s benefits.

Certain use cases highlight that, without thorough due-diligence and efficient planning, random expansion of services may end up making the framework as big and cumbersome as a monolithic architecture.

As nanoservices are still in their infancy, conservative and large organizations usually avoid them (for now), mostly due to the framework’s uncertain support for scalability. 
For those who adopt it, one best practice of using the framework is:
Avoid nanoservices if its use complicates the system that it’s meant to simplify.

## When to use microservices

Compared to nanoservices, microservices are an established and well-known design approach that can operate with a wide range of technologies.

That means microservices have a plethora of resources and groups to support learning or maturity microservices strategy.
Microservices are usually a good fit for:
+ An agile development process
+ Situations where development teams are functionally or geographically distributed
+ Creating a minimum viable product (MVP) that you will extend functionally over time, not all at once


With that in mind, it is equally important to note that microservices are not suited for every application type. 

https://www.bmc.com/blogs/microservice-vs-nanoservice

# SOA

SOA, or service-oriented architecture, defines a way to make software components reusable and interoperable via service interfaces. Services use common interface standards and an architectural pattern so they can be rapidly incorporated into new applications.  
This removes tasks from the application developer who previously redeveloped or duplicated existing functionality or had to know how to connect or provide interoperability with existing functions.

Each service in an SOA embodies the code and data required to execute a complete, discrete business function (e.g. checking a customer’s credit, calculating a monthly loan payment, or processing a mortgage application). 
The service interfaces provide loose coupling, meaning they can be called with little or no knowledge of how the service is implemented underneath, reducing the dependencies between applications. 

This interface is a service contract between the service provider and service consumer. Applications behind the service interface can be written in Java, Microsoft .Net, Cobol or any other programming language, supplied as packaged software applications by a vendor (e.g., SAP), 
SaaS applications (e.g., Salesforce CRM), or obtained as open source applications.  Service interfaces are frequently defined using Web Service Definition Language (WSDL) which is a standard tag structure based on xml (extensible markup language).  

The services are exposed using standard network protocols—such as SOAP (simple object access protocol)/HTTP or Restful HTTP (JSON/HTTP)—to send requests to read or change data. Service governance controls the lifecycle for development and at the appropriate stage the services are published in a registry that enables developers to quickly find them and reuse them to assemble new applications or business processes.


## Benefits of SOA

Compared to the architectures that preceded it, SOA offered significant benefits to the enterprise:

### Greater business agility; 

faster time to market: Reusability is key.  The efficiency of assembling applications from reusable services - i.e. building blocks, rather than rewriting and reintegrating with every new development project, enables developers to build applications much more quickly in response to new business opportunities. The service oriented architectural approach supports scenarios for application integration, data integration, and service orchestration style automation of business processes or workflows.  This speeds software design and software development by enabling developers to spend dramatically less time integrating and much more time focusing on delivering and improving their applications. 
    
### Ability to leverage legacy functionality in new markets: 
A well-crafted SOA enables developers to easily take functionality ‘locked’ in one computing platform or environment and extend it to new environments and markets. For example, many companies have used SOA to expose functionality from mainframe-based financial systems to new web applications, enabling their customers to serve themselves to processes and information previously accessible only through direct interaction with the company’s employees or business partners.

### Improved collaboration between business and IT: 

In an SOA, services can be defined in business terms (e.g., ‘generate insurance quote’ or ‘calculate capital equipment ROI’). This enables business analysts to work more effectively with developers on important insights—such as the scope of a business process defined using services or the business implications of changing a process—that can lead to a better result.


### SOA and microservices

## SOA vs. microservices

Experts have filled a few thousand print and digital pages comparing SOA and microservices, and defining the subtleties of their relationship to one another. For the purposes of this article, the chief differences between the two are the coupling of components and scope of use:

SOA is an integration architectural style and an enterprise-wide concept. It enables existing applications to be exposed over loosely-coupled interfaces, each corresponding to a business function, that enables applications in one part of an extended enterprise to reuse functionality in other applications.

Microservices architecture is an application architectural style and an application-scoped concept. It enables the internals of a single application to be broken up into small pieces that can be independently changed, scaled, and administered. It does not define how applications talk to one another—for that we are back to the enterprise scope of the service interfaces provided by SOA.


## Architecture

Microservices architecture emerged and gained steam with the rises of virtualization, cloud computing, Agile development practices, and DevOps. Most of the advantages of microservices in these contexts arise from the decoupling of the components, which simplifies and improves the following:


### Developer agility and productivity

Microservices enable developers to incorporate new technologies to one part of the application without affecting the rest of the application. Any component can be modified, tested, and deployed independently of the others, which speeds iteration cycles.


### Scalability

Microservices can take maximum advantage of cloud scalability—any component can be scaled independently of the others for the fastest possible response to workload demands and the most efficient use of computing resources.


### Resilience

Again, thanks to decoupling, the failure of one microservice does not impact the others. And each microservice can perform to its own availability requirements without staking the other components or the entire application to greatest common availability requirements.





---

## Tom Sapletta
+ [Kontakt na linkedin](https://www.linkedin.com/in/tom-sapletta-com/)
+ [Blog Tom Sapletta ' Embedded System Software & Hardware Developer, Germany Essen](https://tom.sapletta.pl/)
+ [Firma Softreck - Leadership Through Software Development](https://softreck.pl/)

---


## Inne tematy:

+ [Zaplanuj Biznes](https://www.zaplanujbiznes.pl/)
+ [Dlaczego warto robić biznes w Niemczech? dlaczego.de](https://www.dlaczego.de)
+ [Dlaczeo warto i jak zostać rezydentem niemieckim? rezydent.de](https://www.rezydent.de)
+ [Jak zostać nierezydentem polskim? nierezydent.pl](https://www.nierezydent.pl/)


---

+ [edit](https://github.com/nanoservices-pl/www/edit/main/README.md)

```
https://github.com/nanoservices-pl/www.git
```
    
    
    
---
+ [edit](https://github.com/nanofrontends/www/edit/main/README.md)
+ [git](https://github.com/nanofrontends/www)
```
https://github.com/nanofrontends/www.git
```

