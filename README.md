# resume.py

A python script reading data from a YAML file and generating a resume or CV in ODT or HTML format.

The script executes the following steps:

- Load the specified YAML data file.
- Load the jinja2 template file (`-t <template>` option).
- Execute the jinja2 template engine with the YAML data as an input.
- If the output format is ODT (`-f odt` option), postprocess the result.
- Save the output (`-o <output>` option).

## Examples

The folder `examples/` contains YAML data files and `templates/` contains the jinja2 files.

Export in ODT format:

```bash
python3 resume.py examples/charly-lersteau.yml -f odt -t templates/resume.odt.yml.j2 -o resume.odt
```

Export in HTML format:

```bash
python3 resume.py examples/charly-lersteau.yml -f html -t templates/resume.html.j2 -o resume.html
```

## Dependencies

`resume.py` requires following python packages:

- `Jinja2`
- `odfpy`
- `pybtex`
- `pybtex-apa-style`
- `python-dateutil`
- `python-docx`

## License

This software is licensed under the GPLv3.
Please see the `LICENSE` file for further information.