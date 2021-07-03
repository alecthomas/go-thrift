load("@bazel_gazelle//:def.bzl", "gazelle")
load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

# gazelle:prefix github.com/UrbanCompass/go-thrift
# gazelle:build_file_name BUILD,BUILD.bazel
gazelle(name = "gazelle")

go_library(
    name = "go_default_library",
    srcs = [
    ],
    importpath = "github.com/UrbanCompass/go-thrift",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_stretchr_testify//mock:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_stretchr_testify//require:go_default_library",
        "@com_github_stretchr_testify//suite:go_default_library",
    ],
)
