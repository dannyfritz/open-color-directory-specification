# `.ocd` Specification

This specification describes the *OCD* format. *OCD* files are intended to be used for managing and sharing color palettes.

This is intentionally similar to [`package.json`](https://docs.npmjs.com/files/package.json) and [`bower.json`](https://github.com/bower/bower.json-spec) files.

## File Format

*OCD* is a plain utf-8 text file consisting of *JSON*.

## JSON Properties

### `name` *string*

### `description` *string*

### `homepage` *string*

### `version` *string*

The version of the color directory. Follows [semantic versioning](http://semver.org/).

### `authors` *[author](#author) or [[author](#author)]*

### `license` *string*

### `repo` *string*

URL to the color directory's source control.

### `directories` *[directory](#directory) or [[directory](#directory)]*

### `ocd` *string*

Version of the *OCD* specification to use.

## Additional JSON Types

### `author` *{}*

#### `author.name` *string*

#### `author.email` *string*

#### `author.url` *string*

#### `directory` *{}*

##### `directory.name` *string*

##### `directory.description` *description*

##### `directory.colors` *[[color](#color)]*

### `color` *{}*

Ex. for red in *RGB*:
```JSON
	color: {
		"format": "HSL",
		"data": {
			"red": 255,
			"green": 0,
			"blue": 0
		},
		"alpha": 1.0
	}
```

Ex. for red in *HSL*:
```JSON
	color: {
		"format": "HSL",
		"data": {
			"hue": 0,
			"saturation": 1.0,
			"lightness": 0.5
		},
		"alpha": 1.0
	}
```

#### `color.name` *string*

#### `color.id` *string*

#### `color.description` *string*

#### `color.format` *string*

The color format specification. Most likely "`HSL`" or "`RGB`".

#### `color.data` *{}*

The value of this property depends on `color.format`.
Ex. [HSL](#HSL) or [RGB](#RGB)

#### `color.alpha` *number*

A value between `0.0` and `1.0` inclusive.

#### `color.placement` *[placement](#placement)*

### `HSL` *{}*

#### `HSL.hue` *number*

#### `HSL.saturation` *number*

#### `HSL.lightness` *number*

### `RGB` *{}*

#### `RGB.red` *number*

#### `RGB.green` *number*

#### `RGB.blue` *number*

### `placement` *{}*

#### `placement.x` *number*

#### `placement.y` *number*
