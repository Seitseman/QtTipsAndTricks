# QtTipsAndTricks
Some random things that are hard to find on stack overflow or else


# Copy files from one place to the "shadow folder" using cross-platform qmake command and parse slashes of path in platform-dependant way

    copydata.commands = $(COPY_DIR) $$shell_path($$PWD/3rdparty) $$shell_path($$OUT_PWD/3rdparty)
    first.depends = $(first) copydata
    export(first.depends)
    export(copydata.commands)
    QMAKE_EXTRA_TARGETS += first copydata
