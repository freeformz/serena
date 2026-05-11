# Developer Instructions

## Python Environment & Development Tools

See [the contributing guide](CONTRIBUTING.md) for instructions on setting up your development environment
and tools for formatting and type checking.

## Release Process

1. Ensure clean git status.
2. Set the version for release, e.g.
   
       python scripts/bump_version.py --patch
       python scripts/bump_version.py --minor

   This also creates the git tag.
3. Push to GitHub:

       git push
       git push --tags

   Pushing the tag triggers the `create-release` workflow, which creates a
   **candidate release** (pre-release) on GitHub.
4. Review the candidate release on the
   [GitHub Releases page](https://github.com/oraios/serena/releases).
   When ready, edit the release and promote it to a full release
   (uncheck *Set as a pre-release* and publish).
   This triggers the `publish` workflow, which builds and publishes the
   package to PyPI.