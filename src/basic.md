# Creating a basic SpanDeX project

There are two ways of creating a SpanDeX project:
  - either you want to create it in a new directory, in which case you can run
    ``` bash
    spandex init <project_name>
    ```

  - or you already have in directory that you want to setup for a SpanDeX
    project, in which case you can simply run
    ``` bash
    spandex init
    ```

This will generate the default configuration file `spandex.toml` and an initial
`main.dex` file.

To compile your files into a PDF, you can simply run

``` bash
spandex build
```

