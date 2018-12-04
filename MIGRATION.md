## Migration Guide

### Migrating from 2.X.X to 3.X.X

V3 changes the internal structure of `o-loading`.

These mixins have been privatised and are no longer meant to be used within a product.
```diff
- oLoadingColor
+ _oLoadingColor
- oLoadingSize
+ _oLoadingSize
```

In order to output styles, the available mixin is now:
```scss
@include oLoading($opts: (
	'colors': ('dark'),
	'sizes': ('small')
))
```

In order to add styles to a specific element, you can use:
```scss
.small-dark-loading {
	@include oLoadingContent($opts: (
		'color': ('dark'),
		'size': ('small')
	));
}
```

### Migrating from 1.X.X to 2.X.X

V1 -> V2 introduces the new majors of o-colors. Updating to this new version will mean updating any other components that you have which are using o-colors. There are no other breaking changes in this release.
