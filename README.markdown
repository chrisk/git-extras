# Git extras

These are some useful git porcelain scripts I've been using. They attempt to
work on both git and git-svn repos.


## Installation

1. Clone this repository somewhere
2. Add the new `git-extras` directory to your `PATH`
3. You can now use the included git commands without the dash, since `git`
   defers its first argument to `git-` scripts you've installed.


## Usage

### git notpushed

Lists commits you haven't pushed to your remote yet, in a quick one-line
format. Optionally accepts same arguments as `git-log`. Assumes "origin" is
the remote if no `branch.<current>.remote` configuration exists (or "trunk"
for repositories that seem to have git-svn remotes).

### git test-notpushed [command]

Runs `command` against a checkout of each commit you haven't pushed to the
remote yet. Handy for running an automated test suite against each of your
changes. Stops early if the command returns a non-zero status code.
