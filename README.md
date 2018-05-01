# map_native

A flutter package to view a map widget on mobile apps. Supports Android and iOS.

## Usage
To use this plugin, add `map_native` as a [dependency in your pubspec.yaml file](https://flutter.io/platform-plugins/).

``` yml

map_native: "0.0.1"

```

### Example

``` dart
import 'package:flutter/material.dart';
import 'package:map_native/map_native.dart';

void main() {
  runApp(new Scaffold(
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
    );
  ));
}

```