# nodejs_sh_binary_bug

Demonstrates a bug in Bazel Node support. To repro:

```
bazel run //my_project:RunNode
```

Results in the error message:

```
ERROR: cannot find build_bazel_rules_nodejs/third_party/github.com/bazelbuild/bazel/tools/bash/runfiles/runfiles.bash
```
