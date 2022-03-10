
(config/reference)=
# Configuration reference

This page lists the configuration options that are available to control MyST-NB.
For more detailed explanation of when to use each option, see the other sections in the documentation.

## MyST Parser configuration

The MyST-NB parser derives from {ref}`the base MyST-Parser <myst:intro/get-started>`, and so all the same configuration options are available.
See the {ref}`MyST configuration options <myst:sphinx/config-options>` for the full set of options.

## Notebook execution configuration

This configuration is used to control how Jupyter Notebooks are executed at build-time.

`````{list-table}
:header-rows: 1

* - Option
  - Default
  - Description
* - `jupyter_cache`
  - ""
  - Path to jupyter_cache, [see here](execute/cache) for details.
* - `execution_excludepatterns`
  - ()
  - Exclude certain file patterns from execution, [see here](execute/config) for details.
* - `jupyter_execute_notebooks`
  - "auto"
  - The logic for executing notebooks, [see here](execute/config) for details.
* - `execution_in_temp`
  - `False`
  - If `True`, then a temporary directory will be created and used as the command working directory (cwd), if `False` then the notebook's parent directory will be the cwd.
* - `execution_allow_errors`
  - `False`
  - If `False`, when a code cell raises an error the execution is stopped, if `True` then all cells are always run.
    This can also be overridden by metadata in a notebook, [see here](execute/allow_errors) for details.
* - `execution_timeout`
  - 30
  - The maximum time (in seconds) each notebook cell is allowed to run.
    This can also be overridden by metadata in a notebook, [see here](execute/timeout) for details.
* - `execution_show_tb`
  - `False`
  - Show failed notebook tracebacks in stdout (in addition to writing to file).
`````

## Notebook parsing and output rendering

These configuration options affect the look and feel of notebook parsing and output rendering.

`````{list-table}
:header-rows: 1

* - Option
  - Default
  - Description
* - `nb_custom_formats`
  - `{}`
  - Define custom functions for conversion of files to notebooks, [see here](examples/custom_formats) for details.
* - `nb_render_priority`
  - `{}`
  - Dict override for MIME type render priority, [see here](use/format/priority) for details.
* - `nb_render_plugin`
  - `default`
  - Entry point pointing toward a code cell output renderer, [see here](use/format/cutomise) for details.
* - `nb_render_text_lexer`
  - `myst-ansi`
  - pygments lexer for rendering text outputs, [see here](use/format/ansi) for details.
* - `nb_render_key`
  - `render`
  - The top-level cell metadata key, to store render control data, [see here](use/format/images) for examples.
* - `nb_output_stderr`
  - `show`
  - One of 'show', 'remove', 'warn', 'error' or 'severe', [see here](use/format/stderr) for details.
* - `nb_merge_streams`
  - `False`
  - If `True`, ensure all stdout / stderr output streams are merged into single outputs. This ensures deterministic outputs.
`````
