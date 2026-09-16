# leakdown

Shared [pkgdown](https://pkgdown.r-lib.org) theme for the **guardedverse**
packages: [splitGraph](https://selcukorkmaz.github.io/splitGraph/),
[bioLeak](https://selcukorkmaz.github.io/bioLeak/) and
[fastml](https://selcukorkmaz.github.io/fastml/).

It contains no user-facing functions. It exists so that the three documentation
sites share one palette, one type system, and one footer without three copies of
the same YAML drifting apart.

## Using it

In a package's `_pkgdown.yml`:

```yaml
template:
  package: leakdown
  bslib:
    primary: "#4C78A8"   # this package's accent -- the only colour to set
```

and in its `DESCRIPTION`, so CI installs the theme before building:

```
Config/Needs/website: selcukorkmaz/leakdown
```

## What each package still owns

The theme deliberately does **not** set `navbar` or `reference`. Those are
package-specific, and silently inheriting someone else's navigation is worse
than repeating four lines. Each package declares its own navbar (including the
`guardedverse` link back to the hub) and its own reference index.

## Palette

| Package    | Accent    |
|------------|-----------|
| splitGraph | `#4C78A8` |
| bioLeak    | `#2A7F62` |
| fastml     | `#B85C2E` |

Change the type scale, spacing, callouts, or footer here and rebuild the three
sites; change a colour in the package that owns it.

## Installation

```r
# install.packages("pak")
pak::pak("selcukorkmaz/leakdown")
```
