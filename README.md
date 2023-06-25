## Hello ☃️

I'm Spencer. I sometimes make stuff.

Most of my professional experience is working as a software engineer building full-stack web applications, but I also have a wide range of skills beyond that. Here you will find a list of professional/hobbyist projects that I've contributed to or authored.

## Professional Roles

### [PayNow](https://paynow.gg) (April 2022 - June 2023)

<img src="https://github.com/SpencerTorres/spencertorres/assets/28887171/9820fb6e-8a7e-48a4-845d-35ce50333196" width=500px>


PayNow is a service that fully facilitates hosting an online store and accepting payments for game servers. It integrates multiple pay-in providers and a pay-out provider to build a tax compliant merchant of record (MoR) service supporting
multiple currencies. As the lead engineer, I was responsible for designing and building the entire project from scratch.

The frontend is React with TypeScript, and uses Tailwind for styling. Most of the frontend work was handled by the very talented [Lukas Moucka](https://github.com/m0uka).
The backend is written in Go and has 15+ microservice components that use event-driven architecture to communicate.
Other tools used on this project include: Postgres, NATS, Redis, ClickHouse, Protobuf, Grafana, OpenTelemetry, Kubernetes, GitLab CI, and a lot more.

This is by far the most challening project I've contributed to due to its scope and responsibilities.

### [Rusticated](https://rusticated.com) (April 2018 - `+inf`)
<img src="https://github.com/SpencerTorres/spencertorres/assets/28887171/c8c0a1c0-8f81-4279-a312-8df470251351" width=500px>

Rusticated is a network of servers for the game [Rust](https://rust.facepunch.com).
Rusticated has over 3 million unique players, so they need a lot of unique software to support monitoring server health as well as player data and moderation.
I started doing work for Rusticated back in April 2018 and have authored the majority of their systems.
It started with a simple website and then grew into a large collection of specialized web applications for maintaining operations.
I don't do it full time anymore, but sometimes I get pinged to answer questions about old systems.

The frontend is a regular React application, and the backend is mostly Node.JS with a few Go/C# components here and there.
Other tools used include: Postgres, Redis, ElasticSearch, RabbitMQ, and a ton of other stuff.

I also had the chance to write a highly optimized database for storing heatmap data.
Originally we were storing thousands of events per second in ElasticSearch to generate heatmaps, but it was taking over 26 seconds to aggregate the data. This was unacceptable considering we wanted this data to be updated in real-time.
I decided to solve this by writing a custom solution in Go. Data persists to disk, and upon startup gets loaded into memory using an efficient data structure. All data points can quickly be queiried by a range of time.
I also designed a special binary protocol for returning this data to the browser in a compact format. Overall this solution reduced latency by 99.6%, and decreased the data transfer to browser clients.
This is just one of the many fascinating problems that I've had to tackle while working at Rusticated.

### [Florida Blue](https://floridablue.com) (June 2019 - May 2021)
Blue Cross Blue Shield of Florida, a health insurance provider.
My team was responsible for handling the millions of claims that fail to process automatically.

Our main project was a React SPA backed by dozens of Java + OracleDB components.
I had the chance to introduce some "newer" technologies such as Node.JS, Redis, Go, and GitLab CI.

Not everything was new though. I had some very unique experiences modernizing code that was older than I was.
I also had to build some features that targeted Internet Explorer 7. Writing JavaScript that was ES3 compatible was a fun and interesting challenge.

### Freelance (2017 - June 2019)

During this time I completed various small projects for different companies, mostly in the gaming space.
Usually involved full-stack application development with React/Node.JS.

## Hobbyist Projects

### [BioShock: Infinite in VR](https://steamcommunity.com/sharedfiles/filedetails/?id=2952477736) (2023)

[<img src="https://img.youtube.com/vi/-QKq8XJSEFk/maxresdefault.jpg" width=500px>](https://youtu.be/-QKq8XJSEFk)

I re-created a level from the game BioShock: Infinite inside SteamVR Home. A more detailed overview can be found [here](https://steamcommunity.com/sharedfiles/filedetails?id=2953264938).

This project has been a wonderful creative exercise and technical challenge. I've been able to improve my skills with 3D graphics modeling/texturing/animating and gain experience with reverse engineering file formats.
I also had a chance to work with capturing and stitching HDR panoramas, and game audio/music production.

SteamVR Home uses lua for scripting, but it's hard to organize large projects with lua. I wanted to be able to write complex game systems without the burden of maintaining a lua codebase, so I decided to use a TypeScript transpiler called [TypeScriptToLua](https://github.com/TypeScriptToLua/TypeScriptToLua).
This gave me the ability to write type-safe game scripts in TypeScript and have it automatically the correct lua code.
This involved reading the lua documentation and writing TypeScript declarations for all the types.
So far it has worked without much difficulty and has made scripting incredibly easy. The game logic is far more strucutred in TypeScript than it would be if I had to write plain lua.

### Other (2019 - Present)

I am always tinkering. Here's an example of some stuff I've tinkered with recently:

- A system for monitoring vehicle telemetry via the OBD-2 port using an OpenXC unit. Also integrated a Lidar sensor over UART/Serial for detecting vehicle distance. Built with Go, C++, OpenXC.
- A simple graphics pipeline using Vulkan. Built with C++.
- Multiplayer Jigsaw Puzzle browser game. Built with Pixi JS, Node.JS and socket.io.
- A bunch of other small projects/researched topics.

### [SpencerTorres.com](https://SpencerTorres.com]) (2018)
<img src="https://github.com/SpencerTorres/spencertorres/assets/28887171/e08bc69f-155b-4609-9f8b-92e59515cb21" width=500px>

My personal website, which is somewhat abandoned. Built with React and uses the Oatload project for loading blog posts.

### [Oatload.com](https://oatload.com) (2018)
<img src="https://github.com/SpencerTorres/spencertorres/assets/28887171/2bf87d92-cb06-493b-81ce-ac5d72f84c3b" width=500px>

I built a service for hosting simple blog posts that can be displayed anywhere on the internet.
It's basically a JSON API that you can call from anywhere. Clients can take the text data and render it on the page as Markdown, HTML, or whatever other format they choose.
The service offered the ability to have multiple members, an audit log, and metrics for page views.

Built with React, Redux, Node.JS, Redis, ElasticSearch, and Cassandra (for some poorly chosen reason).
Somehow still runs even though I haven't touched the server in years.

### [Valve Developer Union](https:///valvedev.info) (2017)
<img src="https://github.com/SpencerTorres/spencertorres/assets/28887171/c609645d-a69c-4958-b892-1f239c15759e" width=500px>

A collection of community guides that preserve niche knowledge about Quake and Source engine modding.
The site was fairly popular given it's niche set of topics.

I built the original application with React, Node.JS, Redis, and MongoDB.
Since 2019 this has been converted and preserved with handcrafted HTML/CSS by [mariteaux](http://mariteaux.somnolescent.net).

### Other (2018 and prior)

Some projects don't exist online anymore but were fantastic for learning:

- [Playertick](https://playertick.com) (2018) - A service for growing gaming communities and browsing game servers. This service was able to discover and ping 50,000 game servers in less than a minute using Steam's UDP server protocol. Learned about distributed queuing, and deciphering/wrapping a UDP protocol. Built with Node.JS, Redis, Postgres, and RabbitMQ.
- [CoinCount.info](https://github.com/SpencerTorres/coincount.info) (2018) - Back when cryptocurrenies were increasing in popularity, I made a website that tracked the value of a portfolio. The portfilio would be defined in the query URL and it would show a chart and whatnot. Built with React.
- **Pastecat (2017)** - An application that lets you share your clipboard anywhere. Made a web application and mobile application proof of concept. Built with React/React Native, Redux, Node.JS and Cassandra (still don't remember why I chose that DB, probably because I saw Discord was using it)
- **Picture Game (2017)** - A website where people can upload an image to convert it into a puzzle. Tile by tile people would have to guess what the image was. Built with React, Node.JS and AWS S3 for image hosting.
- **Fizzul (2016)** - A social media style application where users can upload images that expire. Images would expire if users don't keep pushing the button to keep them active. Built with React, Redux, Node.JS, and Redis.
- **INIfy (2015)** - A project for easily re-configuring `.ini` files for games based on a known format. Originally built with Java, but then turned into a web application with Node.JS and MySQL. This was the project that made me ditch Java desktop apps in favor of learning web application development.
- **3D Game Engine (2014)** - A 3D game engine I built from scratch using Java and LWJGL. Learned all about 3D graphics programming with OpenGL + GLSL, object oriented programming, entity-component systems, physics simulations, and linear algebra + vector mathematics.
- **Random Java Desktop apps (2013)** - I used to make random Java desktop applications. I wasn't even using any new libraries, it was just a bunch of Swing framework UI. Learned about reading/writing files, strict typing, and what "programming" is.

## Open Source Contributions

My open source contributions can be seen by checking my GitHub repositories. Most of them are npm modules, but I have also contributed to the RabbitMQ library for Go.
