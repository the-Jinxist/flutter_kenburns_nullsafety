# KenBurns

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

# Multiple images

You can display multiple child in KenBurns with a CrossFade animation

```dart
Container(
    height: 300,
    child: KenBurns.multiple(
      childLoop: 3,
      children: [
        Image.network(
          "https://www.photo-paysage.com/?file=pic_download_link/picture&pid=3100",
          fit: BoxFit.cover,
        ),
        Image.network(
          "https://cdn.getyourguide.com/img/location_img-59-1969619245-148.jpg",
          fit: BoxFit.cover,
        ),
        Image.network(
          "https://www.theglobeandmail.com/resizer/vq3O7LI3hvsjTP2N0m9NwU4W3Eg=/1500x0/filters:quality(80)/arc-anglerfish-tgam-prod-tgam.s3.amazonaws.com/public/4ETF3GZR3NA3RDDW23XDRBKKCI",
          fit: BoxFit.cover,
        ),
      ],
    ),
),
```
