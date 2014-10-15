
This is a version of the official Android openssl sources, but it is meant to be built as a standalone library to be embedded into app.

### Building the code

To build:

cd openssl-android
ndk-build

### Updating the upstream code

This repository tracks the Android openssl repository: https://android.googlesource.com/platform/external/openssl.git 

To use this, add it as a remote called 'upstream'

```shell
git remote add upstream git://android.git.kernel.org/platform/external/openssl.git
```

Then here's how you get the updated code:

```
git fetch upstream                       # Get newest code from Android, but don't merge)
git checkout dev                         # Checkout the dev branch
git merge upstream/kitkat-mr2.2-release  # Merge the latest Android release into this branch)
git push origin master                   # Push the updated merge
```

