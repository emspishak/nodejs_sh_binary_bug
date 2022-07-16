load("@build_bazel_rules_nodejs//:index.bzl", "nodejs_binary")

nodejs_binary(
    name = "NodeHello",
    entry_point = "node-hello.js",
)

sh_binary(
    name = "RunNode",
    srcs = ["run_node.sh"],
    data = [":NodeHello"],
)
