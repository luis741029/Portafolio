# check-linters-confg

`check-linters-config` is a Bash script to compare local files against the files on the main branch of this repository. It will check that files exist and that they are **identical** to the ones here.

## Installation

1. Copy the [`check-linters-conf.sh`](check-linters-conf.sh) file into someplace in the `$PATH` of your machine, for example `/usr/local/bin`:

```
sudo wget -O /usr/local/bin/check-linters-config https://raw.githubusercontent.com/TheDevMBA/linters-config/main/scripts/check-linters-conf.sh
```

2. Make it executable:

```
sudo chmod +x /usr/local/bin/check-linters-config
```

## Usage

Run the command `check-linters-config` on the root of the repository you want to check. It takes as an argument the name of the directory you want to check against.

```
$ check-linters-config ruby
Files main/ruby/.rubocop.yml and .rubocop.yml are identical
```

If you notice differ in your terminal as the following 


```
$ check-linters-config ruby
Files main/ruby/.rubocop.yml and .rubocop.yml differ
```
please do not forget to check the contents in the specific linter config files.

The possible directories/options included are:

- [html-css](https://github.com/TheDevMBA/linters-config/tree/main/html-css)
- [javascript](https://github.com/TheDevMBA/linters-config/tree/main/javascript)
- [react-redux](https://github.com/TheDevMBA/linters-config/tree/main/react-redux)
- [ror](https://github.com/TheDevMBA/linters-config/tree/main/ror)
- [ruby](https://github.com/TheDevMBA/linters-config/tree/main/ruby)
