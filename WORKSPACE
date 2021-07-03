workspace(name = "go_thrift")

# Anvil dependencies
# gazelle:repo bazel_gazelle

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "anvil",
    sha256 = "97fcf364f9dd2a2f55e9e5984f3170e9288ade864b3c82771512b4b23bc76a8f",
    strip_prefix = "anvil-1.1.0",
    urls = ["https://urbancompass.jfrog.io/urbancompass/vcs-remote-cache/UrbanCompass/anvil/tags/v1.1.0/anvil-v1.1.0.tar.gz"],
)

load(
    "@anvil//:deps.bzl",
    "anvil_core_dependencies",
    "anvil_go_dependencies",
)

anvil_core_dependencies()

anvil_go_dependencies()

load(
    "@io_bazel_rules_go//go:deps.bzl",
    "go_register_toolchains",
    "go_rules_dependencies",
)

go_rules_dependencies()

go_register_toolchains()

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()
