# llvm-windows-builds
LLVM Windows builds for CI

## Creating a new build
Create a new release on Github, with a git tag equal to one of the official LLVM repo's tags (https://github.com/llvm/llvm-project/tags), e.g. `llvmorg-15.0.4`.
A Github Actions trigger will build the package and attach it to the release.

### In case of an issue or error
If a release went wrong and you want to start over by deleting the release, first delete the actual release in Github, and then use these commands on your local machine on this repository to delete the tag:
```
git pull
git tag --delete llvmorg-15.0.4
git push --delete origin llvmorg-15.0.4
```
Be sure to replace `llvmorg-15.0.4` with the actual tag you want to remove.
