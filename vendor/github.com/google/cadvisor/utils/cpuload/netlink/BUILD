load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "conn.go",
        "defs.go",
        "netlink.go",
        "reader.go",
    ],
    cgo = True,
    importmap = "k8s.io/kubernetes/vendor/github.com/google/cadvisor/utils/cpuload/netlink",
    importpath = "github.com/google/cadvisor/utils/cpuload/netlink",
    visibility = ["//visibility:public"],
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/google/cadvisor/info/v1:go_default_library",
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
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
