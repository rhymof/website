---
title: Null safety in Flutter
description: Find out how to use non-nullable types in your Flutter code.
---

Null safety is available in the Flutter beta channel,
starting with build `1.24.0-10.2.pre`.
You can now migrate your Flutter packages to use non-nullable types like this:

<?code-excerpt "../null_safety_examples/basics/lib/main.dart (MyApp)"?>
```dart
class MyApp extends StatelessWidget {
  final int anInt = 3; // Cannot be null.
  final int? aNullableInt = null; // Can be null.

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Nullable Fields Demo',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Nullable Fields Demo'),
        ),
        body: Center(
          child: Column(
            children: [
              Text('anInt is $anInt.'),
              Text('aNullableInt is $aNullableInt.'),
            ],
          ),
        ),
      ),
    );
  }
}
```

To learn about null safety,
read these pages:

* [Sound null safety][]:
  The null safety homepage.
  Has basic information, with links to everything else you might need.
* [Understanding null safety][]:
  A deep dive into null safety, written by Dart engineer Bob Nystrom.

When you're ready to start migrating your packages to null safety,
check out these pages:

* [Migrating to null safety][]:
  Instructions for converting your packages to null safety.
* [Unsound null safety][]:
  Conceptual and practical information about mixed-mode programs,
  in which only some libraries are null safe.
* [FAQ][]:
  Questions that have come up during migration to null safety.

[Migrating to null safety]: {{site.dart-site}}/null-safety/migration-guide
[FAQ]: {{site.dart-site}}/null-safety/faq
[Sound null safety]: {{site.dart-site}}/null-safety
[Understanding null safety]: {{site.dart-site}}/null-safety/understanding-null-safety
[Unsound null safety]: {{site.dart-site}}/null-safety/unsound-null-safety
