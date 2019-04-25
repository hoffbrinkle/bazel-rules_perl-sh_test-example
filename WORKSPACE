load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
git_repository(
    name = "rules_perl",
    remote = "http://github.com/bazelbuild/rules_perl.git",
    commit = "6074944df42a0e056b778efefabbdc880d106fe4",
    patches = ["//:perl_rule.patch"],
)
