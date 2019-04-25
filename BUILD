load("@rules_perl//perl:perl.bzl", "perl_binary")

perl_binary(
    name = "perl_tool",
    srcs = ["perl_tool.pl"],
)

genrule(
    name = "shell_runtest",
    outs = ["shell_runtest.sh"],
    cmd = "echo -n '#!/bin/bash\nset -x\nexec $$@' > $@",
)

sh_test(
    name = "some-test",
    srcs = [":shell_runtest"],
    data = [":perl_tool"],
    args = ["$(location //:perl_tool)"],
)
