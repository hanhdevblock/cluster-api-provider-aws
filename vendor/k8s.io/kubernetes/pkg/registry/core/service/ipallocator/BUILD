package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["allocator.go"],
    importmap = "sigs.k8s.io/cluster-api-provider-aws/vendor/k8s.io/kubernetes/pkg/registry/core/service/ipallocator",
    importpath = "k8s.io/kubernetes/pkg/registry/core/service/ipallocator",
    deps = [
        "//vendor/k8s.io/kubernetes/pkg/apis/core:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/registry/core/service/allocator:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/registry/core/service/ipallocator/controller:all-srcs",
        "//pkg/registry/core/service/ipallocator/storage:all-srcs",
    ],
    tags = ["automanaged"],
)
