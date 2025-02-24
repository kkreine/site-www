---
title: "dart: The Dart command-line tool"
description: "The reference page for using 'dart' in a terminal window."
toc: false
---

The `dart` tool (`bin/dart`)
is a command-line interface to the [Dart SDK](/tools/sdk).
The tool is available no matter how you get the Dart SDK —
whether you download the Dart SDK explicitly or download only
the [Flutter SDK.]({{site.flutter}})

Here's how you might use the `dart` tool
to create, analyze, test, and run an app:

```terminal
$ dart create -t console-full my_app
$ cd my_app
$ dart analyze
$ dart test
$ dart run bin/my_app.dart
```

You can also run [`pub` commands][pub] using the `dart` tool:

```terminal
$ dart pub get
$ dart pub outdated
$ dart pub upgrade
```

{{site.alert.version-note}}
  Before Dart 2.10, the `dart` tool was used only to run the
  Dart VM.
  In 2.10, new `dart` commands such as `analyze` and `test` were added
  to replace functionality that was
  previously provided by standalone command-line tools.
  Those standalone tools—for example,
  `dartanalyzer` and `pub`—are
  now being [discontinued gradually][].
{{site.alert.end}}

[discontinued gradually]: https://github.com/dart-lang/sdk/issues/46100

The following table shows which commands you can use with the `dart` tool.
If you're developing for Flutter,
you might use the [`flutter` tool][] instead.

[`flutter` tool]: {{site.flutter_docs}}/reference/flutter-cli

|-----------+-----------------------------------------+-----------------------------------|
| Command   | Example of use                          | More information                  |
|-----------|-----------------------------------------|-----------------------------------|
| `analyze` | `dart analyze [<DIRECTORY|DART_FILE>]`  | Analyzes the project's Dart source code.<br>Use instead of `dartanalyzer`.<br>[Learn more.][analyze] |
| `compile` | `dart compile exe <DART_FILE>`          | Compiles Dart to various formats.<br>Use instead of `dart2js` and `dart2native`.<br>[Learn more.][compile] | 
| `create`  | `dart create <DIRECTORY>`               | Creates a new project.<br>Use instead of [`stagehand`][].<br>[Learn more.][create] | 
| `fix`     | `dart fix <DIRECTORY|DART_FILE>`        | Applies automated fixes to Dart source code.<br>Use instead of [`dartfix`][].<br>[Learn more.][fix] | 
| `format`  | `dart format <DIRECTORY|DART_FILE>`     | Formats Dart source code.<br>Use instead of `dartfmt`.<br>[Learn more.][format] |
| `migrate` | `dart migrate`                          | Supports migration to [null safety][].<br>[Learn more.][migrate] |
| `pub`     | `dart pub <PUB_COMMAND>`                | Works with packages.<br>Use instead of `pub`.<br>[Learn more.][pub] | 
| `run`     | `dart run <DART_FILE>`                  | Runs a Dart program. <br>Use instead of the pre-existing Dart VM command (`dart` with no command).<br>[Learn more.][run] | 
| `test`    | `dart test [<DIRECTORY|DART_FILE>]`     | Runs tests in this package.<br>Use instead of `pub run test`.<br>[Learn more.][test] |
| _(none)_  | `dart <DART_FILE>`                      | Runs a Dart program; identical to the pre-existing Dart VM command.<br>Prefer [`dart run`][run]. |
{:.table .table-striped .nowrap}

[analyze]: /tools/dart-analyze
[compile]: /tools/dart-compile
[create]: /tools/dart-create
[fix]: /tools/dart-fix
[format]: /tools/dart-format
[pub]: /tools/pub/cmd
[run]: /tools/dart-run
[test]: /tools/dart-test
[migrate]: /null-safety/migration-guide#migration-tool

For additional help on any of the commands, enter `dart help <command>`
or follow the links in the **More information** column.
You can also get details on `pub` commands — for example,
`dart help pub outdated`.

[`dartaotruntime`]: /tools/dartaotruntime
[`dartdoc`]: https://github.com/dart-lang/dartdoc#dartdoc
[`dartfix`]: {{site.pub-pkg}}/dartfix
[null safety]: /null-safety
[`stagehand`]: {{site.pub-pkg}}/stagehand
