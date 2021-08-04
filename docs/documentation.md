All of the ComputePod projects based on Python use the [mkdocs]()
documentation generation tool.

To install `mkdocs` type:

```
  pipx install mkdocs
```

## Plugins

We use the **[mkdocs Material
theme](https://github.com/squidfunk/mkdocs-material)**

To install this theme type:

```
  pipx runpip mkdocs install mkdocs-material
```

To provide a uniform configuration of the [Material for
MkDocs](https://squidfunk.github.io/mkdocs-material/) theme, we use the
**[mkdocs-computePods-plugin](https://github.com/computePods/mkdocs-computePods-plugin/)**

To install this plugin type:

```
  pipx runpip mkdocs install git+https://github.com/computePods/mkdocs-computePods-plugin/

```

To help manage the automatic creation of mkdocs pages we use the **[Awesome
Pages](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin)**

To install this plugin type:

```
  pipx runpip mkdocs install mkdocs-awesome-pages-plugin
```

To document the python source code we use the
**[mkdocstrings](https://github.com/mkdocstrings/mkdocstrings)**

To install this plugin type:

```
  pipx runpip mkdocs install mkdocstrings
```

To be able to draw diagrams using
[mermaid](https://mermaid-js.github.io/mermaid) we use the
**[mkdocs-mermaid2-plugin](https://github.com/fralau/mkdocs-mermaid2-plugin)**

To install this plugin type:

```
  pipx runpip mkdocs install mkdocs-mermaid2-plugin
```

## Configuration

We use the following `mkdocs.yml` configuration:

```yaml
site_name: <<the site name>>

site_url: <<the site url>>

repo_url: <<the repository url>>

plugins:
  - search
  - compute-pods
  - awesome-pages
  - mermaid2
  - mkdocstrings
      watch:
        - <<one or more source code directories to watch>>

theme:
  name: material
```
