# mapbox-gl-building-shadows
Experiments with building shadows

## Motivation

Mapbox GL JS version 3 added building shadows to Mapbox maps. The implementation has a few short-comings:

1. Unable to set the shadow color to red/green/etc
2. Not backwards compatible with Mapbox GL JS version 2
3. No feature parity with [Maplibre GL](https://maplibre.org/maplibre-gl-js/docs/) since projects forked

## Approach

Use a heightmap + ray-tracing technique to generate realistic building shadows. This differs from Mapbox GL JS version 3 shadow mapping approach but is more flexible. For example, you can calculate annual sunlight for just one building relatively quickly.

## Related

- https://github.com/mapbox/mapbox-gl-js/issues/7976
- [shademap.app](shademap.app)
