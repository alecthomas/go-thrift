load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "grammar.peg.go",
        "parser.go",
        "types.go",
    ],
    importpath = "github.com/UrbanCompass/go-thrift/parser",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_stretchr_testify//mock:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "parser_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_stretchr_testify//require:go_default_library",
        "@com_github_stretchr_testify//suite:go_default_library",
    ],
)
