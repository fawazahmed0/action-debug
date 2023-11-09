# action-debug
Debug your GitHub Actions by Accessing Terminal via Web Browser.
Built using [ttyd](https://github.com/tsl0922/ttyd) and [Cloudflare tunnel](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/trycloudflare/)

## Features

- Debug your GitHub Actions by using SSH or Web shell
- Continue your Workflows afterwards


## Supported Operating Systems

- Linux
- macOS
- Windows


## Getting Started

```yaml
steps:
- uses: fawazahmed0/action-debug@main
```

The url to access the terminal will be printed in Github Actions log.
The default credentials are:
User: admin
Password: admin

## Set Credentials

Set credentials in "user:pass" format

```yaml
steps:
- uses: fawazahmed0/action-debug@main
  with:
      credentials: "user:pass"
```


## Continue a workflow

If you want to continue a workflow, just create a empty file with the name `continue` in the project directory by running `touch continue`.