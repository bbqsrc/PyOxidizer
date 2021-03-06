.. py:currentmodule:: starlark_pyoxidizer

.. _config_global_state:

=======================================
Functions for Manipulating Global State
=======================================

.. py:function:: set_build_path(path: str)

    Configure the directory where build artifacts will be written.

    Build artifacts include Rust build state, files generated by PyOxidizer,
    staging areas for built binaries, etc.

    If a relative path is passed, it is interpreted as relative to the
    directory containing the configuration file.

    The default value is ``$CWD/build``.

    .. important::

       This needs to be called before functionality that utilizes the build path,
       otherwise the default value will be used.
