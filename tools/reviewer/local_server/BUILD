# THIS FILE IS AUTO-GENERATED

package(default_visibility = ["//visibility:public"])

load("//tools/checkstyle:checkstyle.bzl", "checkstyle_test")

java_library(
    name = "local_http_gateway",
    srcs = ["LocalHttpGateway.java"],
    deps = [
        ":local_http_gateway_grpc_client",
        "//third_party/maven/com/google/flogger",
        "//third_party/maven/com/google/guava",
        "//third_party/maven/org/json",
        "//tools/reviewer/local_server/service:code_review_java_proto",
    ],
)

checkstyle_test(
    name = "local_http_gateway-checkstyle",
    target = ":local_http_gateway",
)

java_library(
    name = "local_http_gateway_grpc_client",
    srcs = ["LocalHttpGatewayGrpcClient.java"],
    deps = [
        "//third_party/maven/io/grpc:grpc_core",
        "//tools/reviewer/local_server/service:auth_service_java_grpc",
        "//tools/reviewer/local_server/service:auth_service_java_proto",
        "//tools/reviewer/local_server/service:code_review_java_grpc",
        "//tools/reviewer/local_server/service:code_review_java_proto",
    ],
)

checkstyle_test(
    name = "local_http_gateway_grpc_client-checkstyle",
    target = ":local_http_gateway_grpc_client",
)

java_binary(
    name = "local_server",
    srcs = ["LocalServer.java"],
    main_class = "com.google.startupos.tools.reviewer.local_server.LocalServer",
    deps = [
        ":local_http_gateway",
        "//common",
        "//common:dagger_with_annotation_processor",
        "//common/flags",
        "//common/repo",
        "//third_party/maven/com/google/flogger",
        "//third_party/maven/com/google/flogger:flogger_system_backend",
        "//third_party/maven/io/grpc:grpc_core",
        "//third_party/maven/io/grpc:grpc_services",
        "//third_party/maven/javax/inject:javax_inject",
        "//tools/reviewer/aa:aa_module",
        "//tools/reviewer/local_server/service:auth_service",
        "//tools/reviewer/local_server/service:code_review_service",
    ],
)

checkstyle_test(
    name = "local_server-checkstyle",
    target = ":local_server",
)
