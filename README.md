# Shimmer Skeleton

A Flutter widget that provides a customizable shimmer effect, ideal for displaying loading states
while fetching data from an API. This package allows you to wrap any widget and display a shimmer
skeleton, enhancing the user experience during loading.

## Features

- Simple integration with any widget.
- Customizable shimmer colors, directions, and animation loops.
- Lightweight and performant.
- Follows Flutter Material design guidelines.

## Installing

Add `shimmer_skeleton` to your pubspec.yaml file:

```yaml
dependencies:
  shimmer_skeleton:
```

## Usage

To use the `SShimmerSkeleton` widget, wrap your child widget with `SShimmerSkeleton` and control the
loading state with the `isLoading` parameter.

```dart
import 'package:shimmer_skeleton/shimmer_skeleton.dart';
```

```dart
class HomePage extends StatelessWidget {
  const HomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Shimmer Skeleton Example')),
      body: Center(
        child: CustomShimmer(
          isLoading: true, // Set to false when data is loaded
          child: Container(
            width: 300,
            height: 150,
            // Actual content area
          ),
        ),
      ),
    );
  }
}

```

## Parameters

- **child**: The widget that will be displayed while loading.
- **isLoading**: A boolean to control whether the shimmer effect should be shown.
- **baseColor**: The base color of the shimmer effect (defaults to the theme's secondary color).
- **highlightColor**: The highlight color of the shimmer effect (defaults to the theme's primary
  color).
- **direction**: The direction of the shimmer effect (defaults to `ShimmerDirection.ltr`).
- **loop**: The number of animation loops; set to `0` for infinite animation (defaults to `0`).
- **enabled**: A boolean to enable or disable the shimmer effect (defaults to `true`).

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This package is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes.