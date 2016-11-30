<!-- BEGIN MUNGE: UNVERSIONED_WARNING -->

<!-- BEGIN STRIP_FOR_RELEASE -->

![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)
![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)
![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)

<h1>PLEASE NOTE: This document applies to the HEAD of the source
tree only. If you are using a released version of Kubernetes, you almost
certainly want the docs that go with that version.</h1>

<strong>Documentation for specific releases can be found at
[releases.k8s.io](http://releases.k8s.io).</strong>

![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)
![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)
![WARNING](http://releases.k8s.io/HEAD/docs/warning.png)

<!-- END STRIP_FOR_RELEASE -->

<!-- END MUNGE: UNVERSIONED_WARNING -->
# Getting Kubernetes Builds

You can use [hack/get-build.sh](../../hack/get-build.sh) to or use as a reference on how to get the most recent builds with curl. With `get-build.sh` you can grab the most recent stable build, the most recent release candidate, or the most recent build to pass our ci and gce e2e tests (essentially a nightly build).

```
usage:
  ./hack/get-build.sh [stable|release|latest|latest-green]

        stable:        latest stable version
        release:       latest release candidate
        latest:        latest ci build
        latest-green:  latest ci build to pass gce e2e
```

You can also use the gsutil tool to explore the Google Cloud Storage release bucket. Here are some examples:
```
gsutil cat gs://kubernetes-release/ci/latest.txt          # output the latest ci version number
gsutil cat gs://kubernetes-release/ci/latest-green.txt    # output the latest ci version number that passed gce e2e
gsutil ls gs://kubernetes-release/ci/v0.20.0-29-g29a55cc/ # list the contents of a ci release
gsutil ls gs://kubernetes-release/release                 # list all official releases and rcs
```


<!-- BEGIN MUNGE: GENERATED_ANALYTICS -->
[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/docs/devel/getting-builds.md?pixel)]()
<!-- END MUNGE: GENERATED_ANALYTICS -->
