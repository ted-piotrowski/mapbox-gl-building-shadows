# mapbox-gl-building-shadows
Experiment with building shadows

[Try the Demo](https://ted-piotrowski.github.io/mapbox-gl-building-shadows/index.html)

[![Mapbox GL Building Shadows demo](/screen.png)](https://ted-piotrowski.github.io/mapbox-gl-building-shadows/index.html)

## Motivation

Mapbox GL JS version 3 added building shadows to Mapbox maps. The implementation has a few short-comings:

1. Unable to set the shadow color to red/green/etc
2. Not backwards compatible with Mapbox GL JS version 2
3. No feature parity with [Maplibre GL](https://maplibre.org/maplibre-gl-js/docs/) since projects forked
4. Approach may be useful to others

## Approach

Use a heightmap + ray-tracing technique to generate realistic building shadows. This differs from Mapbox GL JS version 3 shadow mapping approach but is more flexible. For example, you can calculate annual sunlight for just one building relatively quickly.

## Shortcomings

- Shadow acne (precision issues)
- Shadows near roofs are incorrect

## Related

- https://github.com/mapbox/mapbox-gl-js/issues/7976
- [shademap.app](shademap.app)
