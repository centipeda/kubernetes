package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "cap.go",
        "config.go",
        "container_id.go",
        "doc.go",
        "image.go",
        "log.go",
        "rkt.go",
        "systemd.go",
        "version.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/credentialprovider:go_default_library",
        "//pkg/kubelet/container:go_default_library",
        "//pkg/kubelet/events:go_default_library",
        "//pkg/kubelet/images:go_default_library",
        "//pkg/kubelet/leaky:go_default_library",
        "//pkg/kubelet/lifecycle:go_default_library",
        "//pkg/kubelet/network:go_default_library",
        "//pkg/kubelet/network/hairpin:go_default_library",
        "//pkg/kubelet/prober/results:go_default_library",
        "//pkg/kubelet/types:go_default_library",
        "//pkg/kubelet/util/format:go_default_library",
        "//pkg/securitycontext:go_default_library",
        "//pkg/util/exec:go_default_library",
        "//pkg/util/parsers:go_default_library",
        "//pkg/util/selinux:go_default_library",
        "//pkg/util/strings:go_default_library",
        "//pkg/util/version:go_default_library",
        "//vendor/github.com/appc/spec/schema:go_default_library",
        "//vendor/github.com/appc/spec/schema/types:go_default_library",
        "//vendor/github.com/coreos/go-systemd/dbus:go_default_library",
        "//vendor/github.com/coreos/go-systemd/unit:go_default_library",
        "//vendor/github.com/coreos/rkt/api/v1alpha:go_default_library",
        "//vendor/github.com/docker/docker/pkg/term:go_default_library",
        "//vendor/github.com/docker/engine-api/types:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/google.golang.org/grpc:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/uuid:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/client-go/tools/remotecommand:go_default_library",
        "//vendor/k8s.io/client-go/util/flowcontrol:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "fake_rkt_interface_test.go",
        "rkt_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/kubelet/container:go_default_library",
        "//pkg/kubelet/container/testing:go_default_library",
        "//pkg/kubelet/lifecycle:go_default_library",
        "//pkg/kubelet/network:go_default_library",
        "//pkg/kubelet/network/kubenet:go_default_library",
        "//pkg/kubelet/network/testing:go_default_library",
        "//pkg/kubelet/types:go_default_library",
        "//pkg/util/exec:go_default_library",
        "//vendor/github.com/appc/spec/schema:go_default_library",
        "//vendor/github.com/appc/spec/schema/types:go_default_library",
        "//vendor/github.com/coreos/go-systemd/dbus:go_default_library",
        "//vendor/github.com/coreos/go-systemd/unit:go_default_library",
        "//vendor/github.com/coreos/rkt/api/v1alpha:go_default_library",
        "//vendor/github.com/golang/mock/gomock:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
        "//vendor/golang.org/x/net/context:go_default_library",
        "//vendor/google.golang.org/grpc:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/errors:go_default_library",
        "//vendor/k8s.io/client-go/util/testing:go_default_library",
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
)
