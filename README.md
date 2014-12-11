# Open Color Directory (.ocd)

An open source color palette format to make the world a more colorful and happier place.

![Image of Yaktocat](ocd.png)


## Specification

View the [.ocd specification](ocd-spec.md) for information on the file format.

## Use Cases and Goals

### Sharing

Store your palettes in npm prefixed with `ocd-` to easily share and find new palettes.

### Tooling

Bring better color palette and just color management tooling to Node and the web. It was designed to use *JSON* for a reason.

### Palette Conventions

If there is a convention for creating palettes, then it would be easy to swap out palettes and see what different themes would look like in your project if the.

### Management

This allows for better management of palettes through versioning. If you are maintaining a color palette and want to make a drastic change, bump the major version. That way, nobody will freak out that you broke everything when you want the package to take a new direction for its future.

### Cohesion

Use a single palette package throughout your projects to keep consistent branding. Update the package easily when changes are made upstream.
