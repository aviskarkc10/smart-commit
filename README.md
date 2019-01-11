# Smart Commit

Create a commit prefixed with the current branch name.

## Installation

Run this command on terminal.

```shell
curl https://raw.githubusercontent.com/sbimochan/smart-commit/master/commit -o /usr/local/bin/commit && chmod +x /usr/local/bin/commit
```

## Usage

* If your current branch name is `EF-803`

```shell
$ commit "New feature"

# translates to
git commit -m "EF-803: New feature"
```

* If your current branch is either of `dev`, `uat`, `qa`, `staging` or `master`

```shell
$ commit "New feature"

# translates to
git commit -m "New feature"
```

## Skip Branches

To add a custom branch that you would like to skip, create a `.smart-commit-ignore` file in your top level directory. A `.smart-commit-ignore` file looks like [this](https://github.com/sbimochan/smart-commit/blob/master/.smart-commit-ignore).

Also, you might want to add `.smart-commit-ignore` to your `.gitignore` file.

## License

[MIT](LICENSE)
