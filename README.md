modified version of https://github.com/deepakputhraya/action-pr-title/tree/v1.0.0

# PR title validator action
Github action to enforce Pull Request title conventions

## Usage

See [action.yml](./action.yml)

```yaml
steps:
- uses: robin-thomas-e1391/PR-title-validator@master
  with:
    regex: '([a-z])+\/([a-z])+' # Regex the title should match.
    regex_options: 'i' # Regex should be case insensitive.
    custom_non_match_error: 'valid title options are ...' # Custom error message if regex fails.
    allowed_prefixes: 'fix,feat,chore' # title should start with the given prefix
    prefix_case_sensitive: false # title prefix are case insensitive
    min_length: 5 # Min length of the title
    max_length: 20 # Max length of the title
```

## License
The scripts and documentation in this project are released under the [MIT License](./LICENSE)
