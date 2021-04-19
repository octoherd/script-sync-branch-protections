# sync branch protections

> An [octoherd](https://github.com/octoherd) script to apply branch protection settings from oneand apply it others

## Usage

```
$ npx @octoherd/script-sync-branch-protections \
  --template "octoherd/cli"
```

Pass all options as CLI flags to avoid user prompts

```
$ npx @octoherd/script-sync-branch-protections \
  --template "octoherd/cli" \
  -T ghp_0123456789abcdefghjklmnopqrstuvwxyzA \
  -R "octoherd/repository-with-script-folders"
```

## Options

| option                       | type             | description                                                                                                                                                                                                                                 |
| ---------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `--template`                 | string           | **Required.** Repository name from where to copy the branch protection settings. Example: `--template "octoherd/cli"`                                                                                                                       |
| `--octoherd-token`, `-T`     | string           | A personal access token ([create](https://github.com/settings/tokens/new?scopes=repo)). Script will create one if option is not set                                                                                                         |
| `--octoherd-repos`, `-R`     | array of strings | One or multiple space-separated repositories in the form of `repo-owner/repo-name`. `repo-owner/*` will find all repositories for one owner. `*` will find all repositories the user has access to. Will prompt for repositories if not set |
| `--octoherd-bypass-confirms` | boolean          | Bypass prompts to confirm mutating requests                                                                                                                                                                                                 |

## License

[ISC](LICENSE.md)
