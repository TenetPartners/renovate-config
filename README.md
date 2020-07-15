# renovate-config

This is a base Renovate config file to use with any of our sites we want hook up to Renovate.

## How to use

At Tenet the prefered way to add this config file is to include a renovate option in package.json, like this:

    "renovate": {
        "extends": ["github>TenetPartners/renovate-config"],
        "assignees": ["add-github-name-here"]
    }

You can, however, include the above lines in any of the acceptable renovate config files. renovate.json, .renovaterc, etc...

The extends line is what will pull this config file, and the assignees line will allow you to assign those pull requests to a specific Github user on our team.

## Overriding

You can override anything in the base config by just adding it in the renovate option. For instance if you wanted to change the timezone for a particular repo, you could do the following:

    "renovate": {
        "extends": ["github>TenetPartners/renovate-config"],
        "assignees": ["add-github-name-here"],
        "timezone": "Americas/Los_Angeles"
    }

Any of the renovate config options can be overridden at the repo level.