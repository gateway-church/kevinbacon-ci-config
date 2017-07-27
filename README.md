# kevinbacon-ci-config
Global Linter Config's for KevinBacon-CI.

_If you wish to modify one of the configs below is a list of where all of the docs are for each of the linters_

### Current Linters
- [Coffeescript](http://www.coffeelint.org/)
- [HAML](https://github.com/brigade/haml-lint)
- [Javascript](http://jshint.com/)
- [Ruby](https://github.com/bbatsov/rubocop)
- [SCSS](https://github.com/brigade/scss-lint)
- [Swift (Currently Unconfigured)](https://github.com/realm/SwiftLint)

### SublimeLint Configuration
1. Clone this repo with `git clone https://github.com/gateway-church/kevinbacon-ci-config.git`
2. Install SublimeLint Package `CMD + SHIFT + P - SublimeLint`
3. Install the following SublimeLint packages using the package manager like above
  - SublimeLinter-contrib-haml-lint
  - SublimeLinter-contrib-scss-lint
  - SublimeLinter-jshint
  - SublimeLinter-coffeelint
  - SublimeLinter-rubocop
4. Once those are installed navigate to `Sublime Text -> Preferences -> Package Settings -> SublimeLinter -> Settings User`
5. Replace the config with the one below _Note: Be sure to swap out the paths with the place you cloned the repo to_

#### SublimeLint Config
```
{
    "user": {
        "debug": true,
        "delay": 0,
        "error_color": "D02000",
        "gutter_theme": "",
        "gutter_theme_excludes": [],
        "lint_mode": "load/save",
        "linters": {
            "coffeelint": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/coffeescript/.coffee-lint.json"
                ],
                "excludes": []
            },
            "haml": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/haml/.haml-lint.yml"
                ],
                "excludes": []
            },
            "hamllint": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/haml/.haml-lint.yml"
                ],
                "excludes": []
            },
            "jshint": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/javascript/.jshintrc"
                ],
                "excludes": []
            },
            "rubocop": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/ruby/.rubocop.yml"
                ],
                "excludes": []
            },
            "scss": {
                "@disable": false,
                "args": [
                    "--config",
                    "/path/to/repokevinbacon-ci-config/scss/.scss-lint.yml"
                ],
                "exclude-linter": "",
                "excludes": [],
                "include-linter": ""
            }
        },
        "mark_style": "outline",
        "no_column_highlights_line": false,
        "passive_warnings": false,
        "paths": {
            "linux": [],
            "osx": [
                "~/.rbenv/shims/"
            ],
            "windows": []
        },
        "python_paths": {
            "linux": [],
            "osx": [],
            "windows": []
        },
        "rc_search_limit": 3,
        "shell_timeout": 10,
        "show_errors_on_save": true,
        "show_marks_in_minimap": true,
        "syntax_map": {
            "html (django)": "html",
            "html (rails)": "html",
            "html 5": "html",
            "javascript (babel)": "javascript",
            "magicpython": "python",
            "php": "html",
            "python django": "python",
            "pythonimproved": "python"
        },
        "tooltip_fontsize": "1rem",
        "tooltip_theme": "Packages/SublimeLinter/tooltip-themes/Default/Default.tooltip-theme",
        "tooltip_theme_excludes": [],
        "tooltips": true,
        "warning_color": "DDB700",
        "wrap_find": true
    }
}
```
