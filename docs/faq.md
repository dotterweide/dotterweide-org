# FAQ - frequently asked questions

## What is dotterweide

Dotterweide is an experimentation space with the purpose of developing an embeddable mini-IDE for Scala. Embeddable means, dotterweide
should be made available as a library that can be included in any other project or application, in order to enrich that application
with IDE-like components to facilitate Scala code editing. The "mini" indicates that the project aims to be concise, focusing on the main
properties of a development and editing environment, without becoming a huge project such as IntelliJ, NetBeans, Eclipse etc.

## Who is guiding the directions of the project

While the project was initiated by [Sciss](https://github.com/Sciss/) with [Mellite](https://github.com/Sciss/Mellite/) as the main
target application in mind, it is open for input from any interested party. Until some kind of team has been stablised, I reserve the
right to make decisions and steer the project. As soon as more collaborators are joining the project, we can discuss the best way
to establish a steering mechanism.

## What languages and platforms are targeted

As a starting point, the project wants to provide support for the most recent two major Scala versions. These are currently Scala 2.11 
and 2.12; as soon as 2.13 is released and stable, we may shift to focus on Scala 2.12 and 2.13. We can keep Scala 2.11 support as long as
it is useful (some projects require Scala 2.11, for example Scala Native).

Also as a starting point, desktop applications based on Java2D / AWT / Swing are targeted. By extension, JavaFX is supported as well. The
project does not target the web browser as a primary platform; nevertheless, if there is demand, we can try to abstract the editor API to
allow rendering both on the desktop and in the browser.

## In what kind of scenario can this project be employed

[Mellite](https://github.com/Sciss/Mellite/) is a computer music environment based on Scala. It comes with a very particular document
model which is a workspace embodied by a key-value store (database). Documents contain all sorts of objects, such as sound files,
timelines, breakpoint functions etc., as well as several objects produced from writing Scala code fragments. For this scenario, it should
be possible to embed dotterweide so that these Scala code fragments can be written and edited by the user in an IDE like fashion, that is
a comfortable editor with basic features such as syntax and semantic highlighting, auto-completion, hover-documentation, and so on. The
nature of Mellite implies that dotterweide can create an in-memory model of a project build, or it will have to create such model in
a temporary directory. It needs to be able to use the host application, Mellite, as part of the user's classpath, so that these code
fragments can call into the Mellite API. It is also reasonable to assume that we need a continuum from single-file code editor to
worksheet kind of functionality, and eventually the possibility to interlink multiple code fragments and add custom library dependencies.
In that way, it may resemble most the kind of enviroment that Scastie or ScalaFiddle represent.

## How can I participate

There is a [Gitter channel](https://gitter.im/dotterweide/dotterweide-org) to discuss everything. After introducing yourself, basically
just ping Hanns Holger Rutz at `contact <at> sciss.de`, providing your GitHub handle to be added to the project. Please note that we
will add a code-of-conduct that explains the basic rules of participating.

## What is the license of this project

We aim at a simple FLOSS license that balances the request for anyone editing the project to contribute back, while allowing it to be
linked as a library without much constraints on the hosting application. Thus LGPL v2.1+ is the most likely.

## What about the funny name

I wanted a name that was available as a GitHub organisation and that contains the acronym IDE. dotterweide is a German word denoting the
[yellow willow](https://en.wikipedia.org/wiki/Willow) tree. I also thought to choose a rather short name that is relatively easy to
pronounce for non-German speakers; the pronunciation is "dotter-why-de" ([Dotter](https://www.dict.cc/?s=Dotter),
[Weide](https://www.dict.cc/?s=Weide)). The "logo" was derived from a [public domain CC0 photography](https://www.maxpixel.net/Pollard-Deciduous-Pollarded-Golden-Willow-Willow-3276541).
