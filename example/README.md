# KenBurns example

The Ken Burns effect is a type of panning and zooming effect used in video production from still imagery.

First add to your dependencies:

```
dependencies:
  kenburns_nullsafety: 
```

Then import:

```
  import 'package:kenburns_nullsafety/kenburns_nullsafety.dart';
```


Wrap your image with a KenBurns widget
```dart
Container(
      height: 300,
      child: KenBurns(
        child: Image.network("https://lemag.nikonclub.fr/wp-content/uploads/2017/07/08.jpg", fit: BoxFit.cover,),
      ),
),
```

[![screen](https://raw.githubusercontent.com/florent37/Flutter-KenBurns/master/medias/kenburns_slow.gif)](https://github.com/the-Jinxist/kenburns_nullsafety.git)

# Configuration

You can configure KenBurns Widget

```
KenBurns(
    minAnimationDuration : Duration(milliseconds: 3000),
    maxAnimationDuration : Duration(milliseconds: 10000),
    maxScale : 8,
    child: ...
  });
```

## Getting Started with Flutter

For help getting started with Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
