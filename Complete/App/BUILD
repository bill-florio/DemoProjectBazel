load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

swift_library(
    name = "App_Classes",
    srcs = glob([
        "*.swift"
    ]),
    data = [
    ],
    deps = [
        "//Lib/Logging:TLLogging"
    ]
)

ios_application(
    name = "ios_app",
    bundle_id = "com.thanhvu.test",
    infoplists = ["Info.plist"],
    families = ["iphone"],
    minimum_os_version = "15.0",
    deps = [
        ":App_Classes",
    ]
)