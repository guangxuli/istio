load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "config.go",
        "service.go",
    ],
    visibility = ["//visibility:public"],
    deps = [
        "//pilot/model:go_default_library",
        "//pilot/model/test:go_default_library",
        "//pilot/proxy:go_default_library",
        "//pilot/test/util:go_default_library",
        "@com_github_golang_glog//:go_default_library",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@io_istio_api//mixer/v1:go_default_library",
        "@io_istio_api//mixer/v1/config/client:go_default_library",
        "@io_istio_api//proxy/v1/config:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    size = "small",
    srcs = ["service_test.go"],
    library = ":go_default_library",
    deps = ["@io_istio_api//proxy/v1/config:go_default_library"],
)
