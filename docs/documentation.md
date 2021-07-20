# Documenting the ComputePods Project

All of the ComputePod projects based on Python use the [mkdocs]()
documentation generation tool.

To install `mkdocs` type:

```
  pipx install mkdocs
```

## Plugins

To help manage the automatic creation of mkdocs pages we use the **[Awesome
Pages](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin)**

To install this plugin type:

```
  pipx runpip mkdocs install mkdocs-awesome-pages-plugin
```

We use the **[mkdocs Material
theme](https://github.com/squidfunk/mkdocs-material)**

To install this theme type:

```
  pipx runpip mkdocs install mkdocs-material
```

Finally, to document the python source code we use the
**[mkdocstrings](https://github.com/mkdocstrings/mkdocstrings)**

To install this plugin type:

```
  pipx runpip mkdocs install mkdocstrings
```

## Configuration

We use the following `mkdocs.yml` configuration:

```yaml
site_name: <<the side name>>

plugins:
  - search
  - awesome-pages
  - mkdocstrings

theme:
  name: material

nav:
  - ...
```
