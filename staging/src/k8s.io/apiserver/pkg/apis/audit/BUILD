package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "helpers.go",
        "register.go",
        "types.go",
        "zz_generated.deepcopy.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/apiserver/pkg/apis/audit",
    importpath = "k8s.io/apiserver/pkg/apis/audit",
    deps = [
        "//staging/src/k8s.io/api/authentication/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
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
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/fuzzer:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/install:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/v1:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/v1alpha1:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/v1beta1:all-srcs",
        "//staging/src/k8s.io/apiserver/pkg/apis/audit/validation:all-srcs",
    ],
    tags = ["automanaged"],
)
