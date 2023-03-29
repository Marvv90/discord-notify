# Discord Notify #

Post GitHub Actions Status to Discord.

![Example Picture](https://github.com/Marvv90/discord-notify/blob/master/screenshots/example.png "Example Picture")

## Usage

### Minimum

```yaml
- name: Discord Notifications
  uses: marvv90/discord-notify@master
  with:
    github-token: ${{ secrets.github_token}}
    discord-webhook: ${{ secrets.webhook }}
```

### Full Options Currently

```yaml
- name: Discord Notifications
  uses: marvv90/discord-notify@master
  with:
    github-token: ${{ secrets.github_token}}
    discord-webhook: ${{ secrets.webhook }}
    discord-username: GitHub
    discord-avatar: https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png
    discord-title: ${{ github.workflow }}
    discord-clr-success: 17cf48
    discord-clr-failure: e72727
    discord-clr-cancelled: d3d3d3
```

> :warning: `secrets.github_token` is set from Github

> :warning: `secrets.github_token` needs Read and Write Permissions :warning:

> Go to your Repo -> Settings -> Actions -> Workflow Permissions -> Read and Write Permission
