# download-file
Github action to download a file with wget that works on a multi-platform runners

```yaml
inputs:
  url:
    description: 'The url to download the file from'
    required: true
  target:
    description: 'The target location to output the file to'
    required: false
```

## Usage:

```yaml
steps:
- uses: peternied/download-file@v2
  with:
    url: https://raw.githubusercontent.com/peternied/download-file/main/README.md
    target: path/to/README.md

- name: Use downloaded file
  run: cat README.md
```

# Changelog

## v2
- Reduce the verbosity of the progress bars output to the console
- Adds logging for errors if choco install fails

## v1
- Initial Release