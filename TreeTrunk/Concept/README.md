
***

# TreeTrunks

## Concept

### 2021 August 31st

TreeTrunks is a tool that defines the root of a repository and prevents the repository from trying to define a point outside of itself.

For example, an image labeled `/Example.svg` would normally go for `///<systemPath>/<originFolder(s)>/<repoName>/Example.svg` and would fail to load the image

With this, `/Example.svg` is located at `/Example.svg` and nowhere deeper. This applies to all other files in the repository that have a `:treeTrunks` enabler script set to `on` `1` or `true`

It can be used for far more than just image files. Its purpose is to let you link to any file within a repository without it escaping. There is a TreeTrunks enabler script that must go into the header of each file you use. It is a boolean, and can be written 3 ways:

`:treeTrunks = on`

or:

`:treeTrunks = off`

alternatively:

`:treeTrunks = 1`

or:

`:treeTrunks = 0`

and:

`:treeTrunks = true`

or:

`:treeTrunks = false`

**Concept from: 2021, Tuesday August 31st** by [seanpm2001](https://github.com/seanpm2001/)

***
