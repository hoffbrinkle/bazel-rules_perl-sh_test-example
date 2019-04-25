genrule(
    name = "shell_runtest",
    outs = ["shell_runtest.sh"],
    cmd = "echo -n '#!/bin/bash\nset -x\nexec $$@' > $@",
)

sh_test(
    name = "some-test",
    srcs = [":shell_runtest"],
    data = ["//perl_util:perl_tool"],
    args = ["$(location //perl_util:perl_tool)"],
)
