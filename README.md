# map_native

A flutter package to view a map widget on mobile apps. Supports Android and iOS.


![MapView Screenshot](https://github.com/xclud/flutter_native_map/raw/master/screenshots/map01.png)


## Usage
To use this plugin, add `map_native` as a [dependency in your pubspec.yaml file](https://flutter.io/platform-plugins/).

### Example

``` dart

import 'package:flutter/material.dart';
import 'package:map_native/map_native.dart';

void main() => runApp(new MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final theme = Theme.of(context);

    return new MaterialApp(
      title: 'MapView Demo',
      theme: new ThemeData(
        primarySwatch: Colors.purple,
      ),
      home: new Scaffold(
          appBar: new AppBar(
            title: const Text("MapView Demo"),
          ),
          body: new Stack(
            children: [
              new MapView(),
              new Align(
                  alignment: Alignment.bottomRight,
                  child: new Padding(
                      padding: const EdgeInsets.all(16.0),
                      child: new FloatingActionButton(
                          backgroundColor: theme.cardColor,
                          onPressed: () {},
                          child: new Icon(Icons.my_location,
                              color: Theme.of(context).primaryColor))))
            ],
          )),
    );
  }
}

```