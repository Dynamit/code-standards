# Contributing

At [Dynamit](http://dynamit.com) we like to jam on ideas and move forward together. This is how our code evolves, so our standards should as well. Here are the guidelines for contributing to the coding standards.

## Team-think

Any standard should be at least mostly agreed upon by the team(s) that it affects. No rogue developers. If you have an idea for a new standard or update to an existing standard, solicit feedback and work with the team to get alignment.

**These standards are meant to be a baseline for development** - to smooth the friction of multiple developers context-switching between projects. Agreement amongst the team is key.

**These standards are not meant to be rigid**. Resist the urge to overly-prescribe development practices, as that will inhibit autonomy and innovation.

## Setup

We use [Gitbook](https://www.npmjs.com/package/gitbook) to publish our standards. The various build steps are scripted for convenience.

Initial setup (run once locally):

```
npm run prepare
```

Run local server and recompile changes on the fly (for local devlopment):

```
npm run serve
```

Building the documentation (to just produce build artifacts):

```
npm run build
```

Publish (build + deploy):

```
npm run publish
```
