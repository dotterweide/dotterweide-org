# ecosystem

The purpose of this document is to gather existing open source tools, libraries, tutorials, prior art etc. that are relevant for creating
dotterweide. The repositories are sorted alphabetically.

## Ammonite

- [lihaoyi/Ammonite](https://github.com/lihaoyi/Ammonite/) is a powerful REPL for Scala, extending the standard REPL in many ways.

## ENSIME

The [ensime](https://github.com/ensime) project is creating editor-agnostic IDE support for Scala, with the main client being for
Emacs. It also has an implementation of an LSP client. The project is currently without maintainer.

## ScalaIDE

The [scala-ide](https://github.com/scala-ide) project is about creating a Scala plugin for Eclipse. The project is mostly abandoned now.

- [scala-ide/scala-ide](https://github.com/scala-ide/scala-ide) the main language support plugins for Eclipse
- [scala-ide/scalariform](https://github.com/scala-ide/scalariform) is a code formatter and also provides the parser for scala-ide
- [scala-ide/scala-refactoring](https://github.com/scala-ide/scala-refactoring) is a library providing different refactoring actions
  for scala-idea, e.g. renaming symbols.

## ScalaInterpreterPane

- [Sciss/ScalaInterpreterPane](https://github.com/Sciss/ScalaInterpreterPane/) is a simple desktop editor with Scala syntax highlight
  (based on JFlex and SyntaxPane) and integration with Scala interpreter/REPL. It's using the presentation compiler for code
  completion.

## scalameta

The [scalameta](http://scalameta.org/) project is all about Scala tooling and thus contains a number of relevant tools and libraries.

- [scalameta/scalameta](https://github.com/scalameta/scalameta) is the foundational project that includes syntax parser and semantic-db.
- [scalameta/scalafmt](https://github.com/scalameta/scalafmt) and [scalacenter/scalafix](https://github.com/scalacenter/scalafix) are two
  tools based on scalameta / semantic-db.
- [scalameta/metals](https://github.com/scalameta/metals) is an LSP language-server implementation for Scala based on scalameta. 

## scaled

- [scaled/scaled](https://github.com/scaled/scaled) is a powerful desktop editor / mini-IDE based on JavaFX and written in Scala. It is
  modelled after Emacs, with language-specific "modes" supplied by other projects, such as
  [scaled/scala-mode](https://github.com/scaled/scala-mode). Some are implemented as an LSP _client_ which could be useful to
  inspect: [scaled/project-service](https://github.com/scaled/project-service)

## ToyIDE

- [pavelfatin/toyide](https://github.com/pavelfatin/toyide) is a proof-of-concept project for building a simple self-contained mini-IDE for
  the desktop. It has an editor component with several features such as inspection and error highlighting. It comes a number of toy languages
  it supports, so Scala support would need to be added. Fork: [Sciss/toyide](https://github.com/Sciss/toyide/).  

-------------------

## Projects not reviewed yet

A place to collect potentially interesting projects without having reviewed them yet:

- [buntec/scalavista-server](https://github.com/buntec/scalavista-server) alternative language server with backends for vim and VS code.
- [tindzk/seed](https://github.com/tindzk/seed) alternative build tool that can produce bloop project files
- [FXMisc/RichTextFX](https://github.com/FXMisc/RichTextFX) JavaFX based editor, supporting variable fonts and font sizes
- [bobbylight/RSyntaxTextArea](https://github.com/bobbylight/RSyntaxTextArea) has a few whistles we could use such as code folding

-------------------

## videos

- [ScalaSphere](https://www.youtube.com/channel/UC2D5QYMoclw4fz8YWFgC4sg/videos) is a conference on Scala tooling. The YouTube channel
  contains serveral videos on scalameta, Scala compiler internals, etc.
