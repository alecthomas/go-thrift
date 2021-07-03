load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "bitset.go",
        "client.go",
        "decoder.go",
        "encoder.go",
        "framed.go",
        "helpers.go",
        "protocol.go",
        "protocol_binary.go",
        "protocol_compact.go",
        "protocol_text.go",
        "server.go",
        "tags.go",
        "thrift.go",
        "transport.go",
        "util.go",
    ],
    importpath = "github.com/UrbanCompass/go-thrift/thrift",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_stretchr_testify//mock:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "bitset_test.go",
        "client_test.go",
        "encoder_test.go",
        "framed_test.go",
        "helpers.go",
        "protocol.go",
        "protocol_binary_test.go",
        "protocol_compact_test.go",
        "protocol_fuzz_test.go",
        "server_test.go",
        "tags_test.go",
        "thrift_test.go",
        "util_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "@com_github_stretchr_testify//require:go_default_library",
        "@com_github_stretchr_testify//suite:go_default_library",
    ],
)
