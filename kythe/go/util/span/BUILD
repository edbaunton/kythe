load("//tools:build_rules/shims.bzl", "go_test", "go_library")

package(default_visibility = ["//kythe:default_visibility"])

go_library(
    name = "span",
    srcs = ["span.go"],
    deps = [
        "//kythe/proto:common_go_proto",
        "//kythe/proto:xref_go_proto",
        "@com_github_sergi_go_diff//diffmatchpatch:go_default_library",
    ],
)

go_test(
    name = "span_test",
    size = "small",
    srcs = ["span_test.go"],
    library = "span",
    visibility = ["//visibility:private"],
    deps = ["@com_github_golang_protobuf//proto:go_default_library"],
)
