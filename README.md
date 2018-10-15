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

### Editor Configurations
- [Sublime](https://www.sublimetext.com/3)
- [Visual Studio Code](https://code.visualstudio.com/download)
- [Atom](#atom)

### Sublime
Follow the steps below to config Sublime text with all of the KevinBacon support linters and configs.
1. Clone this repo with `git clone https://github.com/gateway-church/kevinbacon-ci-config.git`
2. Install SublimeLint Package `CMD + SHIFT + P - SublimeLint`
3. Install the following SublimeLint packages using the package manager like above
  - SublimeLinter-haml-lint
  - SublimeLinter-contrib-scss-lint
  - SublimeLinter-jshint
  - SublimeLinter-coffeelint
  - SublimeLinter-rubocop
4. Once those are installed navigate to `Sublime Text -> Preferences -> Package Settings -> SublimeLinter -> Settings`
5. Replace the config with the one below _Note: Be sure to swap out the {path-to-repo} with the place you cloned the repo to_

#### Config
```
{
  "debug": true,
  "delay": 0,
  "error_color": "D02000",
  "gutter_theme": "",
  "gutter_theme_excludes": [],
  "lint_mode": "load_save",
  "linters": {
    "coffeelint": {
      "@disable": false,
      "args": [
        "--config",
        "{path-to-repo}/coffeescript/.coffee-lint.json"
      ],
      "excludes": []
    },
    "haml": {
      "@disable": false,
      "args": [
        "--config",
        "{path-to-repo}/haml/.haml-lint.yml"
      ],
      "excludes": []
    },
    "hamllint": {
      "@disable": false,
      "args": [
        "--config",
        "{path-to-repo}/haml/.haml-lint.yml"
      ],
      "excludes": []
    },
    "jshint": {
      "@disable": false,
      "args": [
        "--config",
        "~{path-to-repo}/javascript/.jshintrc"
      ],
      "excludes": []
    },
    "rubocop": {
      "@disable": false,
      "args": [
        "--config",
        "{path-to-repo}/ruby/.rubocop.yml"
      ],
      "excludes": []
    },
    "scss": {
      "@disable": false,
      "args": [
        "--config",
        "{path-to-repo}/scss/.scss-lint.yml"
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
```

### Visual Studio Code
Follow the steps below to config KevinBacon Linters in Visual Studio Code
1. Clone this repo with `git clone https://github.com/gateway-church/kevinbacon-ci-config.git`
2. Install the extensions below
    - [scss-lint](https://marketplace.visualstudio.com/items?itemName=adamwalzer.scss-lint)
    - [jshint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.jshint)
    - [coffeelint](https://marketplace.visualstudio.com/items?itemName=lkytal.coffeelinter)
    - [ruby-rubocop](https://marketplace.visualstudio.com/items?itemName=misogi.ruby-rubocop)

_Note: Haml Lint isn't support by Visual Studio Code quite yet_

3. Navigate to your user settings `Code -> Preferences -> Settings` or `CMD + ,`
4. Add the settings below to your user config _Note: Be sure to swap out the paths with the place you cloned the repo to_

#### Config
```
"jshint.config": "/path/to/where/you/cloned/kevinbacon-ci-config/javascript/.jshintrc",
"jshint.excludePath": "/path/to/where/you/cloned/kevinbacon-ci-config/javascript/.jshintignore",
"scssLint.showHighlights": false,
"scssLint.errorBackgroundColor": "rgba(200, 0, 0, .8)",
"scssLint.warningBackgroundColor": "rgba(200, 120, 0, .8)",
"scssLint.languages": [
    "css",
    "scss"
],
"scssLint.statusBarText": "`$(telescope) scss-lint  ${errors.length} $(x)  ${warnings.length} $(alert)`",
"scssLint.configDir": "/path/to/where/you/cloned/kevinbacon-ci-config/scss/.scss-lint.yml",
"ruby.rubocop.configFilePath": "/path/to/where/you/cloned/kevinbacon-ci-config/ruby/.rubocop.yml",
"coffeelinter.defaultRules": "/path/to/where/you/cloned/kevinbacon-ci-config/coffeescript/.coffee-lint.json"

```


### Atom
If you have not installed Atom, follow the instructions below for [Installing Atom](installing-atom).

Then go through the instructions below for [Installing and Configuring Atom Linters](installing-and-configuring-atom-linters).
Use the instructions for [Installing Atom Plugins](#installing-atom-plugins), anytime you are asked to install a plugin.

#### Installing Atom
Download it from, https://atom.io/.  For Mac, unzip, and copy app to Applications folder. Double click file to run.

__Verify Basic Editor Settings__
From the menu bar, Click (select) "Atom" -> "Preferences" to open the settings page, and then click on "Editor" located in
the left column.
Make sure that:
 - The following are checked: "Atomic Soft Tabs", "Auto Indent", "Auto Indent on Paste", "Confirm Checkout HEAD revision".
 - The "Preferred line length" is set to "120".
 - That "Soft tabs" is checked.
 - That "Tab length" is "2".  That should be the editor's default value.
 - "Tab type" is set to "Soft"

Other settings you may want enabled: "Show Cursor on Selection", "Show Indent Guide", "Show Invisibles", "Show Line Numbers".

Then click on the Packages tab, and search for "Whitespace". Click "Settings" under the "Whitespace" plugin, and make sure
the following are checked: "Ensure Single Trailing New Line", "Keep Markdown Line Break Whitespace", and "Removing Trailing Whitespace".
Make sure the following are not checked: "Ignore Whitespace on Current Line", and "Ignore Whitespace Only Lines".


#### Installing Atom plugins
As you go through the "Installing and Configuring linters" section, you will need to reference these instructions.
1. In the menu click (select) "Atom" -> "Preferences". This should open the setting page.
2. On the settings page, click (select) "Install" from the left column.
3. Search for the plugin to install, and click the install button for that plugin.
4. Click on Settings to modify settings.

   In the instructions below you will be asked to install and configure plugins.
   When a plugin configuration has {path-to-repo} you will need to replace that with the path to kevinbacon-ci-config.
   For Mac an easy way to find this is to open finder and locate the folder, right click, then click "get info". Then
   copy the path from the "Where" field, and add '/kevinbacon-ci-config'.

#### Installing and Configuring Atom Linters.
1. Clone this repo with `git clone https://github.com/gateway-church/kevinbacon-ci-config.git`.
2. Make sure you have installed the following ruby gems.  If not install them.

   - rubocop *( Is it installed: `gem list rubocop`. To install: `gem install rubocop` )*
   - scss_lint *( Is it installed: `gem list scss_lint`. To install: `gem install scss_lint` )*

3. Install the following Atom plugins (see [Installing Atom Plugins](#installing-atom-plugins))
   - __linter-ui-default__

   - __linter__  
     Settings: verify the following are enabled: "lint preview tabs", "lint on open", "lint on change".

   - __linter-haml__  
     Settings: set "the coffeelint.json path" to "{path-to-repo}/coffeescript/.coffee-lint.json"

   - __linter-jshint__  
     Settings: set "Global Haml lint yml file" to {path-to-repo}/haml/.haml-lint.yml.

   - __linter-rubocop__  
     Settings: set "Command" to
     "{path-to-rubocop-gem} --config path-to-repo}/ruby/.rubocop.yml"

     *"{path-to-rubocop-gem}" should be replaced with the actual path to the gem file. To get that go to a command prompt and run `which rubocop`*

   - __linter-scss-lint__  
     Settings: set "Config Name" to "{path-to-repo}/scss/.scss-lint.yml", and "Executable Path" to the path to the lint-scss ruby gem.

     *To get the path to your lint-scss gem, go to a command prompt and run `which scss-lint`.*

   - __linter-coffeelint__  
     Settings: set "coffeelint.json Path" to "{path-to-repo}/coffeescript/.coffee-lint.json"
