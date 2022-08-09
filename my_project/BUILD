load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")
load("//my_project:nodejs_binary_with_runfiles.bzl", "nodejs_binary_with_runfiles")

nodejs_binary(
    name = "NodeHello",
    entry_point = "node-hello.js",
)

nodejs_binary_with_runfiles(
    name="NodeHelloWorking",
    bin=":NodeHello"
)

sh_binary(
    name = "RunNode",
    srcs = ["run_node.sh"],
    data = [":NodeHelloWorking"],
)

sh_test(
    name="RunNode_test",
    srcs = ["run_node.sh"],
    data = [":NodeHelloWorking"],
)
