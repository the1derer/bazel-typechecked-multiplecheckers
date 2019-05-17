package(default_visibility = ["//visibility:public"])

java_plugin(
    name = "nullness-checker",
    processor_class = "org.checkerframework.checker.nullness.NullnessChecker",
    deps = [
        '@checker//jar',
    ],
    visibility = ["//visibility:public"],
)

java_plugin(
    name = "signedness-checker",
    processor_class = "org.checkerframework.checker.signedness.SignednessChecker",
    deps = [
        '@checker//jar',
    ],
    visibility = ["//visibility:public"],
)

java_library(
    name = 'multiple_checkers',
    exported_plugins = [ # Add all your checkers here
        ':nullness-checker',
        ':signedness-checker',
    ],
    exports = [
        '@checker_qual//jar',
    ],
    # javacopts = [
    #     '-Xmaxerrs:10000',
    #     '-Xmaxwarns:10000',
    #     # '-Awarns',  # -Awarns turns Checker Framework errors into warnings
    #     '-AcheckPurityAnnotations',
    #     '-Xbootclasspath/p:@annotatedjdk8//jar' # org.checkerframework:jdk8:jar
    # ],
)