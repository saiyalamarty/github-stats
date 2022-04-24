# Git Stats

Command line tool to get number of PRs reviewed by a user.

## Usage
Use `--help` to see all options.
```
$ gitstats --help
Usage: gitstats [OPTIONS]

  This script will print the number of PRs reviewed by the user in the last
  two weeks.

Options:
  -t, --token TEXT     Github token
  -u, --username TEXT  Github username
  -o, --org TEXT       Github org
  -r, --repos TEXT     ',' separated github repos
  --help               Show this message and exit.
```

The script can by default attempts to read the options from the environment variables. Set the following environment variables:

* `GITHUB_TOKEN` - GitHub token
* `GITHUB_USERNAME` - GitHub username
* `GITHUB_ORGANIZATION` - GitHub organization
* `GITHUB_REPOS` - Comma separated list of GitHub repositories

If the environment variables are not set, the script will prompt for the values.

When the script is run, it will print the number of PRs reviewed by the user in the last two weeks.

```
$ gitstats
PRs reviewed this week: 2
╭───┬────────────┬─────────────────────────────────────────────────────────────────────┬───────╮
│   │ Repo       │ PR Title                                                            │ PR ID │
├───┼────────────┼─────────────────────────────────────────────────────────────────────┼───────┤
│ 0 │ git_repo_1 │ Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiu │ 101   │
│ 1 │ git_repo_2 │ Lorem ipsum dolor sit amet, consectetur adipiscing elit,            │ 100   │
╰───┴────────────┴─────────────────────────────────────────────────────────────────────┴───────╯
```
