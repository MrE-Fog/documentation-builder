Ubuntu documentation builder
===

A tool for building a set of documentation files in HTML format,
from a remote git repository containing markdown files.

Installation
---

``` bash
pip3 install ubuntudesign.documentation-builder
```

Usage
---

The basic usage will build the markdown files from a remote repository in the standard format into the local directory:

``` bash
$ documentation-builder  # Build markdown documentation from the current directory
# or
$ documentation-builder --repository git@github.com:juju/docs.git  # Build documentation from remote repository
```

Optional arguments:

``` bash
$ documentation-builder \
    --repository {repository-url}     `# A source repository. If provided, all source paths will be relative to this repository root`
    --branch {branch-name}            `# Pull from an alternative branch to the default (only valid with --repository)`
    --source-path {dirpath}           `# Path to the folder containing markdown files (default: .)`
    --source-media-dir {dirpath}      `# Path to the folder containing media files (default: ./media)`
    --source-context-file {filepath}  `# A file containing the context object for building the templates (default: ./context.yaml)`
    --output-path {dirpath}           `# Destination path for the built HTML files (default: .)`
    --output-media-dir {dirpath}      `# Where to put media files (default: ./media)`
    --template-path {filepath}        `# Path to an alternate wrapping template for the built HTML files`
    --media-url {prefix}              `# Prefix for linking to media inside the built HTML files (default: Relative path to built media location, e.g.: ../media)`
    --no-link-extensions              `# Don't include '.html' extension in internal links`
```
