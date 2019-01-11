# Guidelines

This document describes the general guidelines for code style, code organisation, and build setup. These guidelines are for now:

- all projects should use [semantic versioning](https://semver.org/) inspired versioning. However, we follow Scala practice,
  where we have `<epoch>.<major>.<minor>`, where `<epoch>` is zero in alpha phase, becomes `1` when stable, and `<major>`
  is incremented whenever the API is not binary compatible, as indicated by running the
  [mima plugin](https://github.com/typesafehub/migration-manager/wiki/Sbt-plugin). For any binary compatible change, we
  increment minor versions.
- in upstream, there are always two branches: `master` and `work`. Ongoing work happens in `work`; here the project
  version is typically `-SNAPSHOT`. Whenever a stable version is completed, it is merged into `master`, so that `master`
  always corresponds to the last published version.
- stable versions are published to [Sonatype](http://sonatype.org/) maven central. We have to figure out the group-id still.
- we use sbt 1.x for building, with `build.sbt` defining the build using multi-module syntax (`project.in(file(...))`).
  We do not use `project/Build.scala` type of syntax.
- default Scala version should be 2.12.x, and cross-build Scala versions are 2.11.x and 2.12.x.
  When Scala 2.13.0 is released, we should try to include that as soon as possible.
- `.gitignore` contains all IDE specific files which should not be shared, such as IntelliJ's `*.iml` and `.idea`.
- Scala style should be standard format of IntelliJ or defaults of [scalafmt](https://scalameta.org/scalafmt/docs/configuration.html),
  until further notice. Two-spaces indent, no tab characters, UTF-8 encoding, Unix line endings.
- Fully nested standard source directories, e.g. `src/main/scala/the/package/TheClass.scala`, if possible one source code
  file per class/trait. Package objects are defined in a file called `package.scala`.
- Style rules generally follow InelliJ defaults, e.g. explicit return type for implicit values. Also: all public and
  `protected` members should have explicit return type. No procedure syntax.
- Testing framework is [ScalaTest](http://www.scalatest.org/). Whenever code moves from experimental phase to stabilisation,
  we should strife to include unit tests for all functionality.
- all public API should be documented using [scaladoc](https://docs.scala-lang.org/style/scaladoc.html) notation. Private and
  internal API should be documented using single line (`//`) comments.

## Process

The development and thought process of code repositories should be documented in markdown files in respective `notes` directories.
For general, diary-type of files, include the date in the name using `YYMMHH`, e.g. `Notes190112.md`. For thematic files, just
use a simple name, e.g. `related.md`.
